# How to change self-signed SSL certs for CP4I on ROKS?

1. Log in to your cluster with your IBMid by using one of the following methods:

- Browse to the OpenShift Console. From the dropdown menu in the upper right of the page, click Copy Login Command. Paste the copied command in your local terminal.
- Browse to the oauth token request page. Follow the instructions on the page.

2. Switch to the Cloud Pak for Integration project (`cp4i` by default):
```
oc project cp4i
```

3. Extract ROKS ingress certificates to your local folder:
```
oc extract secret/$(oc get route console -n openshift-console -o jsonpath="{.spec.host}" | awk -F'.' '{print $2}') -n ibm-cert-store --confirm --to=./
```

4. Spit CA and cert:
```
split -p "-----BEGIN CERTIFICATE-----" tls.crt cert-
```

5. Delete the IBM Common Services route certificate:
```
oc -n ibm-common-services delete certificate route-cert
```

6. Delete the IBM Common Services route secret:
```
oc -n ibm-common-services delete secret route-tls-secret
```

7. Create a new route-tls-secret from the extracted certs:
```
oc -n ibm-common-services create secret generic route-tls-secret --from-file=ca.crt=./cert-ab  --from-file=tls.crt=./cert-aa  --from-file=tls.key=./tls.key
```

8. Patch the Automation UI config:
```
oc patch AutomationUIConfig iaf-system --type merge --patch '{"spec":{"tls":{"issuerRef":{"name":""}}}}' 
```

9. Delete the IAF CA certificate:
```
oc delete certificate iaf-system-automationui-aui-zen-ca
```

10. Delete the IAF certificate:
```
oc delete certificate iaf-system-automationui-aui-zen-cert
```

11. Delete the external TLS secret:
```
oc delete secret external-tls-secret
```

12. Create a new external TLS secret from the extracted certs:
```
oc create secret generic external-tls-secret --from-file=cert.crt=./tls.crt  --from-file=cert.key=./tls.key
```

13. Restart all auth-idp pods:
```
oc -n ibm-common-services delete pod -l app=auth-idp
```

14. Restart all ibm-nginx pods:
```
oc delete pod -l component=ibm-nginx
```

Done. Check Cloud Pak for Integration dashboard route. It should have valid ROKS SSL certificates.

### Support

For any questions, contact DTE support.

Business Partners - Contact DTE Support - dte@us.ibm.com

IBMers - Make a post on the [#dte-techzone-support](https://ibm-dte.slack.com/archives/C0124J683GW) slack channel.
