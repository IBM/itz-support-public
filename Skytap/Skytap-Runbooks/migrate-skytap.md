# Migrate a Skytap environment to VMware in Techzone

This will guide you through the steps to migrate your Skytap environments to the VMware on IBM Cloud infrastructure.

1. Create a support request to export Skytap environment via Slack #ITZ-TECHZONE-SUPPORT, https://techzone.ibm.com/help, or send an email to techzone.help@ibm.com

- You will need to provide the template id from your Techzone collection (just one region is fine):

![find template](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate1.png)

- Your email request from https://techzone.ibm.com/help will look like:

![email support](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate2.png)

Once your request is completed Support will provide you an FTP link and the Network information from your environment. 

Sample FTP link
![ftp link](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate3.png)

Sample Network environment details, use the network information when you catalog your new VMware environment in Techzone at the end.
![ftp link](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate4.png)


2. Make reservations for Template Builder, and IBM Cloud Object Storage from https://techzone.ibm.com/collection/skytap-migration
- If your Template Builder reservation expires you lose everything except what you upload to COS!!!
- If you don't have access to this Collection, request it from Support.

Sample Environment from https://techzone.ibm.com/collection/skytap-migration
![migrate5](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate5.png)

- Reservation details to access Bastion, use the Desktop URL at top of Template Builder reservation to connect to the Template Builder VM. 

![migrate7](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate6.png)

3. From within Template Builder VM you can access the vSphere console login information is at the bottom of the reservation details.

`Open Chrome and use credentials for vSphere found at bottom of Template Builder reservation.
Best to use Chrome for clipboard access, or if you are using Firefox and unable to copy/paste in Remote Desktop Web Client, please enable clipboard See https://sudoedit.com/firefox-async-clipboard/.` 

![migrate7](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate7.png)



4. To download exported VM, use the link provided by support and paste it into Filezilla within the Template Builder VM.


![migrate11b](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate11b.png)

- Download the VM to the /home/techzone folder.
- Once downloaded you can extract the VM by double clicking it in the Files application.
- You will need to wait until the .vmx file shows up and this could take a long time since the unzip process runs in the background.

![migrate12b](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate12b.png)


5. Edit the .vmx file

![migrate14b](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate14b.png)

 5a. remove floppy, and set power options to “soft”

![migrate13](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate13.png)

![migrate12](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate12.png)

6. Convert the VM to OVA 
- Run a Terminal window
```
cd ~
ovftool session.vmx mynewvm.ova
```

![migrate14](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate14.png)

7. To Backup your environment, upload to Cloud Object Storage, 

`Assuming you made a reservation for Cloud Object Storage, and accepted the invite to the ITZ-TECH account.`

  Log into cloud.ibm.com, navigate to Storage under resources and open the cos-dte instance.

![migrate15](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate15.png)

Put images in the skytap-exports bucket.

![migrate16](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate16.png)

8. Open Chrome, log into vSphere using the credentials at the bottom of your Template Builder reservation.  Create folder in vSphere under **templates-shared.  
**
9. Right click to Deploy OVF.
![migrate17](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate17.png)

![migrate19](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate19.png)

- Select your default compute resource:

![migrate20](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate20.png)

- Select the storage "datastore-shared":

![migrate21](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate21.png)

- Select the network "gym-segment-shared":

![migrate22](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate22.png)

- Finish

![migrate23](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate23.png)
![migrate24](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate24.png)

10. Upgrade vSphere compatibility

![migrate25](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate25.png)
![migrate26](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate26.png)


11. Clone to Template

![migrate27](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate27.png)
![migrate28](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate28.png)

12. Create Techzone environment in https://techzone.ibm.com/collection/skytap-test

![migrate36](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/skytapmigrate36.png)


Default Variables required
- vm_template_folder
- vm_template_id
- vm_map_string (make sure your VM Map string is correct, you can use any JSON validators like https://jsonlint.com/) 
- vm_domain
- vm_router_ip
- vm_subnet

Note: if you do not have Network details from Skytap use the default values

13. Test reservation 

14. Production rollout

Once all testing is completed you need to send a note to techzone.help@ibm.com or #itz-techzone-support to have an admin move your from _template-shared_ to _templates _ (production)

Now you can update your environment with the correct  details


