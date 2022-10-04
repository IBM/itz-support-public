
# OpenShift

## Single Node Deployments

Most, though not all, of the on-premise pre-installed deploys of OpenShift on Power and Z install a single node cluster, where the master node also hosts the worker role. This is NOT a Production configuration with proper high availability, and as such it should NOT be upgraded.

This configuration is useful for many educational and demo purposes, and is primarily used as there is fairly limited on-premise compute capacity. If full Production sized clusters were deployed we would only be able to support 1/4 of the number of total deploys we can with the single node configuration.

This single node configuration is also what we offer for Power Systems Virtual Server deploys as we have a much higher success rate with the automation to provision them. 
    
## Login Information

You can login via SSH to use the CLI client or via the web based management console.

If via SSH use the cecuser credentials in the project kit to login to the bastion node. Then run `sudo su -` to access the root account. As root the Kubernetes profile and credentials are located in the ~/auth subdirectory. You can view the `~/auth/kubeadmin-password` file to obtain the password for the kubeadmin account.

Note you can not login directly to any of the CoreOS nodes. But as root the SSH keypair is in place and you can SSH to them as the core user if you know what you are doing.

If logging in via the management console the URL can be found in the project kit in the offering section near the top. The console URL can also be displayed if you are SSH in as the root user by running the `oc whoami --show-console` command.

To login to the console it is best to choose the htpasswd authentication method and then use the cecuser credentials from the project kit.

## Console URL Access Issues

If you are experiencing connection issues you likely need to add some DNS suffixes to your resolver configuration. These suffixes should be added if missing:
```
 cecc.ihost.com
 pbm.ihost.com
 ibm.com
```
A few more details can be found here:

[Windows DNS Configuration](configure-dns.md)

## Rate Limiting

If users notice that they are unable to pull images from docker.io, please see the following guide:

[OpenShift Rate Limiting](openshift-rate-limit.md)
