
# Troubleshoot Merlin and IBM i Developer application installation
    
When you try to install a new IBM i Developer application into a project, it fails at 99%.
This is a known issue, it has been raised to the Merlin developer team and it will be fixed in a future release of Merlin (Development team said with version 1.4.1 in February 2023).

Here is the workaround to get it installed and running:

1. Make sure you set an email address to the Merlin admin profile (if you do use the admin account). Open Merlin console, log in as `admin`, click Edit Profile on the top right of the page and set something like `admin@test.com`
2. Do the install as normal and wait a bit... you don't necessarily need to wait for the failure. You can look at the logs of the operator within the OpenShift project that you targeted during the install.
3. Open an SSH connection to your bastion node as `cecuser`
4. Login to the Openshift cluster using this command `oc login localhost:6443 -u cecuser -p 'CECUSER_PASSWORD' --insecure-skip-tls-verify` - replace `CECUSER_PASSWORD` with the right password
5. Run `oc label configmap merlin-https-cert config.openshift.io/inject-trusted-cabundle=false -n MY_PROJECT` - replace MY_PROJECT with the name of the Merlin project you targeted during the install
6. Get the operator pod name via `oc get pod -n MY_PROJECT` - replace MY_PROJECT with the name of the Merlin project you targeted during the install
7. Restart the crashed operator pod via `oc delete pod POD_NAME -n MY_PROJECT` - replace MY_PROJECT with the name of the Merlin project you targeted during the install and POD_NAME with the pod name (ie: ibmi-developer-workspaces-operator-748bc4f9c-w6vg5)
8. Wait a few minutes (5 to 10 minutes) until cheClusterRunning becomes Available via `oc get checluster ibmi-developer-workspaces -o yaml -n MY_PROJECT | grep cheClusterRunning`
```shell
$ oc get checluster ibmi-developer-workspaces -o yaml -n test | grep cheClusterRunning
  cheClusterRunning: Available
```
9. Run `oc label namespace MY_PROJECT InstalledApplications=IBM-i-developer --overwrite`
10. Get the IDE URL via `oc get checluster ibmi-developer-workspaces -o yaml -n MY_PROJECT | grep cheURL`


