# How to change self-signed SSL certs for CP4D on ROKS?

1. Log in to your cluster with your IBMid by using one of the following methods:

- Browse to the OpenShift Console. From the dropdown menu in the upper right of the page, click Copy Login Command. Paste the copied command in your local terminal.
- Browse to the oauth token request page. Follow the instructions on the page.

2. Switch to the Cloud Pak for Data project (`zen` by default):
```
oc project zen
```

3. Extract ROKS ingress certificates to your local folder:
```
oc extract secret/$(oc get route console -n openshift-console -o jsonpath="{.spec.host}" | awk -F'.' '{print $2}') -n ibm-cert-store --confirm --to=./
```

4. Create a new external-tls-secret from the extracted certs:
```
oc create secret generic external-tls-secret --from-file=cert.crt=./tls.crt  --from-file=cert.key=./tls.key
```

5. Restart all ibm-nginx pods:
```
oc delete pod -l component=ibm-nginx
```
Done. Check Cloud Pak for Data dashboard route. It should have valid ROKS SSL certificates.

### Support

For any questions, contact DTE support.

Business Partners - Contact DTE Support - itz@us.ibm.com

IBMers - Make a post on the [#itz-techzone-support](https://ibm-itz.slack.com/archives/C0124J683GW) slack channel.
