## VMware Known Errors and next steps

**Problem:** User is getting the following message when creating a template:

"*error: expected scsi_type to be one of [pvscsi lsilogic lsilogic-sas], got buslogic*"

**Fix:** Please re-template VMs.

---

**Problem** User getting following message during failed reservation:

"_Error: vertex “vsphere_virtual_machine.stage1[\“isva_1004_template\“]” error: error cloning virtual machine: error cloning on datastore cluster “datastore-dal10-vm”: An error occurred during host configuration._"

**Fix** 
1. Create a New VM from this Template to the same folder 
2. change the Network adaptor
3. change the name on the old template
4. change the VM to template and rename to original name.  
5. Delete the old template. 

---

Problem: User getting the follow messaging during failed provision:

_"Error: vertex "local.bastion_ip (expand)" error: Error in function call"_

Fix: Ensure the vm_subnet variable override is typed correctly. Example user adding 10.0.0/24 should be 10.0.0.0/24.

---

**Problem:** User creates an OCP cluster using one of the offerings for CP4I and can't find the cluster

**Fix:** This reservation deploys OpenShift and deploys CP4I on a cluster through Red Hat GitOps, which does not use IBM Cloud catalog CP4I installer or give users access to it


---

**Problem:** User is wondering how to add Kubernetes support to a TZ based windows server template-able environment and what licensing conditions for the software components are needed.

**Fix:** Currently, we have a Windows VM pattern that users can use and install Kubernetes on (please search those and see if there are any that fit your uses the best!)
New patterns with Kubernetes on Windows and using multiple machines can be created but this is up to the user. Kubernetes has no licensing, so there is no impact that we would need to worry about. 
Any business justifcations for creating this can also be submitted as a custom request (https://custom-requests.ideas.aha.io/portal_session/new).
