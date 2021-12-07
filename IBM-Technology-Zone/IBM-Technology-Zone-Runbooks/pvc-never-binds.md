# PVC never binds

We've seen that occasionally a PVC provisioned using the `ibmc-file-gold` storage class gets stuck in the pending state.

If you do an `oc describe pvc` on the PVC in question you will likely see the following:
```
Events:
  Type     Reason                Age                     From                                                                                   Message
  ----     ------                ----                    ----                                                                                   -------
  Normal   ExternalProvisioning  175m (x43 over 3h5m)    persistentvolume-controller                                                            waiting for a volume to be created, either by external provisioner "ibm.io/ibmc-file" or manually created by system administrator
  Warning  ProvisioningFailed    109m                    ibm.io/ibmc-file_ibm-file-plugin-59b87bf57-thpzz_5dedf200-1a2f-439a-ae27-808a04904fc3  failed to provision volume with StorageClass "ibmc-file-gold": Storage creation failed with error: {Code:E0005, Description:Storage with the order ID 86478850 could not be created after retrying for 3600 seconds. Description: Storage Order Status/Transaction [Current:APPROVED/Storage_SelectServiceResource, Expected:APPROVED/COMPLETE] , Type:StorageProvisionTimeout, RC:408, Recommended Action(s):Delete your PVC, then re-create it. If the problem persists, open an IBM Cloud support case.}
  Normal   Provisioning          11m (x12 over 175m)     ibm.io/ibmc-file_ibm-file-plugin-59b87bf57-thpzz_5dedf200-1a2f-439a-ae27-808a04904fc3  External provisioner is provisioning volume for claim "openshift-image-registry/image-registry-storage"
  Warning  ProvisioningFailed    11m (x11 over 109m)     ibm.io/ibmc-file_ibm-file-plugin-59b87bf57-thpzz_5dedf200-1a2f-439a-ae27-808a04904fc3  failed to provision volume with StorageClass "ibmc-file-gold": pvc already has a failed provision status [ibm.io/provisioning-status:{"status":"failed","error":"Storage creation failed with error: {Code:E0005, Description:Storage with the order ID 86478850 could not be created after retrying for 3600 seconds. Description: Storage Order Status/Transaction [Current:APPROVED/Storage_SelectServiceResource, Expected:APPROVED/COMPLETE] , Type:StorageProvisionTimeout, RC:408, Recommended Action(s):Delete your PVC, then re-create it. If the problem persists, open an IBM Cloud support case.}","time":"2021-12-06T16:34:31Z","attempt":1,"retry":false,"pluginid":"ibm-file-plugin-1638804530","pvcid":"4f2e1071-2a80-469a-b5a1-32ac9f25de1d"}].Retry wont happen. kindly delete and re-create pvc
  Normal   ExternalProvisioning  3m40s (x699 over 173m)  persistentvolume-controller                                                            waiting for a volume to be created, either by external provisioner "ibm.io/ibmc-file" or manually created by system administrator
```

As stated in the event error message the resolution is to delete the PVC and recreate it.

## Resolution

- Get a command line to the cluster where the problem is occurring.
  - For a ROKS cluster, if you have appropriate access you can do:
    - `ic oc cluster config -c CLUSTER_NAME --admin`
  - Or get to the OCP console and get the `oc login` command from there.

- Get a copy of the YAML defining the PVC:
```
$ oc get pvc PVC_NAME -n PROJECT_NAME -o yaml > my-pvc.yaml
```
Example:
```
$ oc get pvc -o yaml -n openshift-image-registry image-registry-storage > openshift-image-registry-pvc-backup.yaml
```

- (Optional) Make a copy of the backup and edit out all the unnecessary content in the yaml
  - `cp openshift-image-registry-pvc-backup.yaml openshift-image-registry-pvc.yaml`
  - Under `metadata.annotations`
    - Delete the annotation: `ibm.io/provisioning-status`
    - Delete the annotation: `kubectl.kubernetes.io/last-applied-configuration`
    - Delete the `creationTimestamp`
  - Delete all of `metadata.managedFields`.
    - If using `vi` get the line number of `managedFields` using, `:.=`
    - Then scroll the last line of the manageFields content and get that line number (`:.=`).
    - Then do, `:firstLine,lastLined`, eg., `:13,53d` to delete all of the lines associated with managedFields
  - Delete `metadata.resourceVersion`
  - Delete `metadata.uid`
  - Delete the `status` content

- Delete the existing PVC that is stuck in the pending state.
```
$ oc delete pvc PVC_NAME -n PROJECT_NAME
```
For example:
```
$ oc delete pvc -n openshift-image-registry image-registry-storage
```

- Recreate the PVC:
If you want to use the original backup directly:
```
$ oc apply -f PVC_NAME_BACKUP.yaml
```

Or if you removed the unnecessary content from the backup:
```
$ oc apply -f PVC_NAME.yaml
```

### Support

For any questions, contact ITZ support - techzone.help@ibm.com
