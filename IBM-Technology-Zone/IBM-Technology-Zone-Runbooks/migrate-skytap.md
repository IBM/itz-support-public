# Migrate a Skytap environment to VMware in Techzone

This will guide yiu through the steps to migrate your Skytap environments to the VMware on IBM Cloud infrastructure.

1. Create a support request to export Skytap environment via Slack #ITZ-TECHZONE-SUPPORT or https://techzone.ibm.com/help

You will need to provide the template id from your Techzone collection (just one region is fine):
![find template](/Images/skytapmigrate1.png)

Your email request from https://techzone.ibm.com/help will look like:
![email support](/Images/skytapmigrate2.png)

Support will give you an FTP link and the Network information from your environment.  
![ftp link](/Images/skytapmigrate3.png)
You will use the network information when you catalog your new VMware environment in Techzone at the end.
![ftp link](/Images/skytapmigrate4.png)


2. Make reservations for Template Builder, and IBM Cloud Object Storage.
If your Template Builder reservation expires you lose everything except what you upload to COS!!!
- Make the reservations from https://techzone.ibm.com/collection/skytap-migration
- If you don't have access to this Collection, request it from Support.

![migrate5](/Images/skytapmigrate5.png)

- Your reservation details will be something like:
![migrate7](/Images/skytapmigrate6.png)
- Use the URL at top of Template Builder reservation to connect to the Template Builder VM. 

3. From within Template Builder VM

- The vSphere console login information is at the bottom of the reservation details.
![migrate7](/Images/skytapmigrate7.png)


`Open Chrome and use credentials for vSphere found at bottom of Template Builder reservation.
Best to use Chrome for clipboard access, or if you are using Firefox and unable to copy/paste in Remote Desktop Web Client, please enable clipboard See https://sudoedit.com/firefox-async-clipboard/.` 

4. Download exported VM
- Use the link provided by support and paste it into Filezilla within the Template Builder VM.
![migrate11b](/Images/skytapmigrate11b.png)
- Download the VM to the /home/techzone folder.
- Once downloaded you can extract the VM by double clicking it in the Files application.
![migrate12b](/Images/skytapmigrate12b.png)
- You will need to wait until the .vmx file shows up and this could take a long time since the unzip process runs in the background.

5. Edit the .vmx, remove floppy, and set power options to “soft”
![migrate14b](/Images/skytapmigrate14b.png)
![migrate13](/Images/skytapmigrate13.png)
![migrate12](/Images/skytapmigrate12.png)

6. Convert VM to OVA.  
- Run a Terminal window
```
cd ~
ovftool session.vmx mynewvm.ova
```
![migrate14](/Images/skytapmigrate14.png)


7. Backup your envoironment.   Upload to Cloud Object Storage

`Assuming you made a reservation for Cloud Object Storage, and accepted the invite to the ITZ-TECH account.`

  Log into cloud.ibm.com, navigate to Storage under resources and open the dte-cos instance.

![migrate15](/Images/skytapmigrate15.png)
Put images in the skytap-exports bucket.
![migrate16](/Images/skytapmigrate16.png)

8. Open Chrome, log into vSphere using the credentials at the bottom of your Template Builder reservation.  Create folder in vSphere under templates-shared.  

9. Right click to Deploy OVF.
![migrate17](/Images/skytapmigrate17.png)
![migrate19](/Images/skytapmigrate19.png)
- Select your default compute resource:
![migrate20](/Images/skytapmigrate20.png)
- Select the storage "datastore-shared":
![migrate21](/Images/skytapmigrate21.png)
- Select the network "gym-segment-shared":
![migrate22](/Images/skytapmigrate22.png)
- Finish
![migrate23](/Images/skytapmigrate23.png)
![migrate24](/Images/skytapmigrate24.png)

10. Upgrade vSphere compatibility
![migrate25](/Images/skytapmigrate25.png)
![migrate26](/Images/skytapmigrate26.png)


11. Clone to Template
![migrate27](/Images/skytapmigrate27.png)
![migrate28](/Images/skytapmigrate28.png)

12. Create Techzone environment in https://techzone.ibm.com/collection/skytap-test
![migrate30](/Images/skytapmigrate30.png)


13. Test reservation

14. Production rollout
- Support request to template VM to production
Infrastructure admin to template and provide env details


