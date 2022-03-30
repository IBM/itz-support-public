Requested Added ODF(OCS) for a ROKS cluster

**NOTE:**  ODF(OCS) can only be installed on ROKS on VPC clusters.  

Users must request ODF(OCS) to be installed by support after the cluster is deployed.
Provide the link to the reservation, or cluster name and the size of ODF(OCS) storage (500GB-2TB)

An ODF(OCS) install will take around 10-20 minutes to finish installing after being started.

Users can check on the status of their install themselves

- You can monitor the progress of the OCS installation by monitoring the OCS operator in the cluster console under "installed operators".

- You can also monitor the state of the pods, PVCs and PVs in the `openshift-storage` project in the cluster. If a PVC is stuck in a "pending" state, then you can do a describe on it to get information as to why it is pending.

- The logs for OCS operator in the `kube-system` project is a good place to monitor the ODF addon installation and get information about installation progress or lack there-of. The `ibmc` plugin pods are running in `kube-system` as well. The logs of the `ibmc` file plugin pod may be helpful in resolving issues. (Do an `oc get po -n kube-system | grep plugin` to get the actual pod names.)

- An `ocscluster` Custom Resource Definition (CRD) is created as part of the ODF/OCS installation. If you do an `oc get ocscluster` you will see an instance of the `ocscluster` likely named `ocscluster-auto` which will have the parameters of the OCS instance.  Both the `ocscluster` CRD and the `ocscluster-auto` instance are not part of any project/namespace.

### Support

For any questions, contact ITZ support - techzone.help@ibm.com
