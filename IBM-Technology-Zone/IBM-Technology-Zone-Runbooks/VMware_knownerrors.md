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

**Problem:**

_"error"_

**Fix:**
