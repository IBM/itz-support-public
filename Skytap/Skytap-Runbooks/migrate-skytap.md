# Migrate a Skytap environment to VMware in Techzone

This will guide you through the steps to migrate your Skytap environments to the VMware on IBM Cloud infrastructure. Support details **Slack #ITZ-TECHZONE-SUPPORT, https://techzone.ibm.com/help, or send an email to techzone.help@ibm.com**

Use **#skytap-migration-support** for any migration specific ask, this is a private channel request access #itz-techzone-support

1. **Create a support request to export Skytap environment**

- You will need to provide the template id from your Techzone collection (just one region is sufficient):

![find template](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate1.png)

- Your email request from https://techzone.ibm.com/help will look like:

![email support](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate2.png)

Once your request is completed Support will provide you an FTP link and the Network information from your environment. 

Sample FTP link

![ftp link](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate3.png)

Sample Network environment details, use the network information when you catalog your new VMware environment in Techzone at the end.

![ftp link](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate4.png)


2. **Make reservations for Template Builder** _(Vsphere access)_, and **Cloud Object Storage for exported VMs** _(Image Storage)_ from https://techzone.ibm.com/collection/skytap-migration

- If your Template Builder reservation expires you lose everything except what you upload to COS!!!
- If you don't have access to skytap-mgration Collection, request it from Support.

Sample Environment from https://techzone.ibm.com/collection/skytap-migration

![migrate5](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate5.png)

- Reservation details to access Bastion can be found in My reservation, use the Desktop URL at top of Template Builder reservation to connect to the Template Builder VM. 

![migrate7](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate6.png)

3. **From within Template Builder VM you can access the vSphere console login information is at the bottom of the reservation details.**

`Open Chrome and use credentials for vSphere found at bottom of Template Builder reservation.
Best to use Chrome for clipboard access, or if you are using Firefox and unable to copy/paste in Remote Desktop Web Client, please enable clipboard See https://sudoedit.com/firefox-async-clipboard/.` 

![migrate7](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate7.png)

4. **To download exported VM, use the ftp link provided by support and paste it into Filezilla within the Template Builder VM.**


![migrate11b](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate11b.png)

- Download the VM to the /home/techzone folder.
- Once downloaded you can extract the VM by double clicking it in the Files application.
- You will need to wait until the **.vmx** file shows up and this could take a long time since the unzip process runs in the background.

![migrate12b](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate12b.png)


5. **Edit the .vmx file to remove floppy and set the power options to "soft"**

![migrate14b](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate14b.png)

**View to remove floppy, and set power options to “soft”**

![migrate13](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate13.png)

![migrate12](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate12.png)

6. **Convert the VM to OVA** (this combines all the vms into one an image that can be run on VMware on IBM Cloud)
- In a Terminal window  run to convert the VM to ova
```
cd ~
ovftool session.vmx mynewvm.ova
```

![migrate14](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate14.png)

7. **Upload your vms to the COS (Cloud Object Storage)** bucket to Backup your images

`Assuming you made a reservation for Cloud Object Storage, and accepted the invite to the ITZ-TECH account.`

  Log into cloud.ibm.com, navigate to Storage under resources and open the cos-dte instance and make the uploads

![migrate15](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate15.png)

Ensure the images are placed in the skytap-exports bucket.

![migrate16](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate16.png)

To continue Migrations

8. **Open Chrome, log into vSphere using the credentials at the bottom of your Template Builder reservation.**
- Create your folder in vSphere under **templates-shared.** Short unique naming conventions advised
- Create and Assign Tag (Tags are used to identify template owner)
    Steps to create a Tag
     a. Right click folder "Tags & Custom Attributes" Select Assign Tag
     b. Click on Add Tag on Top left corner
       - Name Type First and Last name
       - Description enter your IBM id email , VM_template_id and collection url
              -If you have mutiple Collections update your tags to include them
       - Category use drop down select "Owners"  
       - click create
     c. Your Tag Name should appear on the list, use check box to select and Assign


9. **Upload the OVA file VM to vSphere**
- Right click to Deploy OVF and select the OVA file created

![migrate17](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate17.png)

- Select the OVF templates

![migrate19](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate19.png)

- Select your default compute resource:

![migrate20](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate20.png)

- Select the storage "datastore-dal10-templates":

![migrate21](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate21.png)

- Select the network "gym-segment-shared":

![migrate22](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate22.png)

- Click Finish, please wait for the recent task to complete before proceeding to next step

![migrate23](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate23.png)

![migrate24](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate24.png)

10. **Upgrade vSphere compatibility**

![migrate25](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate25.png)

- Configure for compatibility as seen below

![migrate26](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate26.png)


11. **Clone your VM to Template, right click the vm, select Clone, clone to template**

![migrate27](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate27.png)

![migrate28](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate28.png)

12. **To test your migration **Create Techzone environment**** in https://techzone.ibm.com/collection/skytap-test

Sample Network details
![migrate36](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate36.png)

Default Variables required
- Infrastructure - IBM Cloud
- GitOps Patterns (Select vmware-template)
- Account pool (itzvmware), Cloud Account (itzvmware), Geo (Americas), Region (us-south), Datacenter (dal10)
- vm_template_folder (parent folder example "templates-shared")
- vm_template_id (the vspehre folder name for the VMs)
- vm_map_string (make sure your VM Map string is correct, you can use any JSON validators like https://jsonlint.com/) 
- vm_domain
- vm_router_ip
- vm_subnet

Note: if you do not have Network details from Skytap use the default values

13. Once all these are completed create a **Test reservation**, if testing is successful next steps is production roll out
14. For **Production rollout** your VM folder _(vm_template_id)_ in "templates-shared" needs to be copied to "templates" (production folder). This can only be completed by admins

Send Folder name and Collection name/url to techzone.help@ibm.com or #itz-techzone-support to have this completed

Example mail

**Subject:** VMware Template to Production

**Collection name/url:**

**Folder name in "Templates-shared":**

**Required Region:**

Note: if you require access in other data centers please include it in your production request. Only DAL10, WDC04, FRA04, TOK02 are currently available.

Once completed 
- create your environment in your collection _please note:_ vm_template_folder name should be **"templates"** for production templates)
- update old Skytap environment status to "disabled"
- if you create a new collection, retire old collection


