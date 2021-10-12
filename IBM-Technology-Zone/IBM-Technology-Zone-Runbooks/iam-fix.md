# IAM fix

Sometimes users can not see their clusters in IBM Cloud web dashboard. Run the following commands:

1. Log in IBM Cloud via CLI:
```
ibmcloud login --sso
```

2. Select the problem account.

3. Switch to `itzroks` resource group.
```
ibmcloud target -g itzroks
```

4. List clusters:
```
ibmcloud ks cluster ls
```

Done. User should see his/her cluster in CLI and Web.

### Support

For any questions, contact DTE support.

Business Partners - Contact DTE Support - itz@us.ibm.com

IBMers - Make a post on the [#itz-techzone-support](https://ibm-itz.slack.com/archives/C0124J683GW) slack channel.
