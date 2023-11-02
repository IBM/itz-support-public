# Upload new OVA/OVF files to VMware in Techzone 
This will guide you through the steps to upload your new OVA/OVF files for your environment to the VMware on IBM Cloud infrastructure. <br>

## SUPPORT DETAILS:
TechZone Help:  https://techzone.ibm.com/help<br>
Under "How can we help?" on right side, look for:  "Site issues - Open a case or Email: techzone.help@ibm.com"<br>

Link to open Support Case:  https://ibmsf.my.site.com/ibminternalproducts/s/createrecord/NewCase?language=en_US  <br>

Procedure on how to open a Support Case:<br>
https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/open_case_web_internal.md <br>

## PREREQS: 
NOTE: User need (1) Template Builder Reservation created and (2) the OVA/OVF files and ISO files (If needed):

(1) User will need a Template Builder reservation provisioned beforehand which will be used to upload the OVA/OVF and ISO (if needed) files to VMware in TechZone.<br>
a. Create a Template Builder reservation<br>
https://techzone.ibm.com/collection/tech-zone-certified-base-images/journey-vmware-on-ibm-cloud-environments<br>
Scroll down and search for Template Builder.<br>

Click on "Reserve" <br>
![OVAa](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVAa.jpeg)

b. Select and enter the information. Click on "I agree" checkbox and "Submit for Approval" (right bottom blue button to create a reservation) <br>
![OVAb](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVAb.jpeg)

c. Wait for email or check status on TechZone website to see that Template Builder reservation is in "Ready" Status.<br>

(2) User need have the following ready for uploading to your Template Builder environment:<br>
a. OVA/OVF files (example Use VMware Fusion to export a VM image to OVA/OVF or use ovftool)<br>
  NOTES: OVA - a single compressed and zipped file and OVF - individual files<br>
b.ISO file (if needed with your OVA/OVF when prompted for uploading to TechZone) <br>
  
## REFERENCES:
Deploy and Export OVF and OVA Templates<br>
https://docs.vmware.com/en/VMware-vSphere/8.0/vsphere-vm-administration/GUID-AFEDC48B-C96F-4088-9C1F-4F0A30E965DE.html

## PROCEDURE:
### 1. In TechZone, access your Template Builder reservation 
https://techzone.ibm.com/dashboard<br>

Click on pulldown "My library" -> "My Reservations"<br>
![OVA1](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA1.jpeg)

Click on Blue box with Arrow to View<br>
![OVA2](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA2.jpeg)

Click on blue box "Open your IBM Cloud environment"<br>
![OVA3](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA3.jpeg)

### 2. **Login to your environment in VMware** 
-Click on "Remote Desktop" to access your environment in VMware<br>
![OVA4](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA4.jpeg)

- Log into vSphere using the credentials at the bottom of your Template Builder reservation.<br>
  Open Firefox Browser and open URL to vCenter Console URL (via VPN or Bastion) at the bottom of your Template Builder reservation.<br>
  
  Example: https://itzna-vc.na.cloud.techzone.ibm.com/ui
![OVA5](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA5.jpeg)

  
  NOTE: If Firefox browser's default vCenter Console URL does not match the Reservation's vCenter Console URL, change the Browser home settings<br>
        From Browser's hamburger menu on left:<br>
        Select Settings -> Click Home icon<br>
        Change "Homepage and new windows" to the correct vCenter Console URL<br>
 
 ![OVA6](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA6.jpeg)
 
 - Create your folder in vSphere under **templates-shared.** Short unique naming conventions advised<br>
  NOTE: If there are permission errors, notify VMware admin to check permissions for the templates-shared folder<br>
  ![OVA15](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA15.jpeg)
  
![OVA7](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA7.jpeg)

- Create Tag first and then Assign Tag to Template Folder (Tags are used to identify template owner)<br>
     a. Right click on template folder -> Select "Tags & Custom Attributes" -> Select "Assign Tag"<br>   
![OVA25](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA25.jpeg)

     b. Click on "ADD TAG" on Top left corner<br>  
![OVA26](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA26.jpeg)

     c.  Type in the information:<br>
       - Name:  Type First and Last name<br>
       - Description:  enter your IBM id email , vm_template_id name and Collection URL<br>
              -If you have mutiple Collections update your tags to include them<br>
       - Category:  Clear the text and Type in Owners<br>
       - Click "CREATE"<br>
![OVA27](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA27.jpeg)

    d. Your created Tag should appear in the list, use filter to find your tag, click the check box to select and click "ASSIGN"<br>
![OVA28](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA28.jpeg)


### 3. **Upload the OVA/OVF files to vSphere**
- Right click on template folder, Select "Deploy OVF Template"<br>
![OVA9](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA9.jpeg)

- In "Select an OVF Template" screen, Select "Local File" and Click "UPLOAD FILES"<br>
NOTE: The OVF/OVA and ISO file (if required with your OVA/OVF) need to downloaded to the Template Builder VM beforehand<br>
(For example, From the Template Builder VM, Open your BOX URL link where the OVF/OVA and ISO files are stored and download from BOX URL to local "Downloads" folder)<br>
![OVA10](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA10.jpeg)

- Select all the OVA/OVF template files and ISO file (if required) and Click "Open"<br>
NOTE: The tool will warn you if there are missing required files <br>
![OVA13](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA13.jpeg)

NOTE: If ISO file not selected, will see this error <br>
![OVA12](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA12.jpeg)

See the number of files selected and Click "NEXT"<br>
![OVA14](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA14.jpeg)

- Select your local Template Builder compute resource and Click "NEXT"<br>
NOTE: If get permission errors, notify VMware Admin to check permission.<br>
![OVA16](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA16.jpeg)

![OVA20](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA20.jpeg)

See "Review Details" screen and Click "NEXT" <br>
![OVA21](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA21.jpeg)

- Select the storage and Click "NEXT" (Select datastore with the word template in it and with enough free space to store template)  (Example - "datastore-wdc04-templates"):<br>
NOTE: If get permission errors, notify VMware Admin to check permissions.<br>
![OVA17](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA12.jpeg)

![OVA22](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA22.jpeg)

- Select the network "gym-segment-shared" and Click "NEXT" <br>
NOTE: If get permission errors, notify VMware Admin to check permissions.<br>
![OVA18](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA18.jpeg)

![OVA23](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA23.jpeg)

- Click Finish, please wait for the recent task to complete before proceeding to next step<br>
![OVA24](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA24.jpeg)


### 4. **Upgrade vSphere compatibility**
Right Click on the VM Template file, Select "Compatibility" -> Select "Upgrade VM Compatibility" <br>
![OVA29](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA29.jpeg)

Click "YES"
![OVA30](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA30.jpeg)

- Configure for compatibility as seen below and Click "OK"<br>
![OVA31](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA31.jpeg)


### 5. **Clone your VM to Template, right click the vm, select Clone, clone to template**
Right Click on VM -> Select "Clone" -> Select "Clone to Template"<br>
![OVA32](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA32.jpeg)

Type in VM template name -> Click "NEXT":<br>
![OVA33](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA33.jpeg)

Expand POD folder (itz-wdc04) -> Select a Compute Resource -> Click "NEXT"<br>
![OVA34](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA34.jpeg)

Select storage (Select storage with the template in the name) -> Click "NEXT"<br>
![OVA35](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA35.jpeg)

Review and Click "FINISH"<br>
![OVA36](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/OVA36.jpeg)

### 6. **To test your migration **Create Techzone environment**, please follow the steps in the VMwareSetupCollectionVars runbook.

To Add Environment variables/values to your Collection, please view the VMwareSetupCollectionVars runbook: https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/VMwareSetupCollectionVars.md#add-environment-variablesvalues-to-your-collection
### 7. Once all these are completed create a **Test reservation**, if testing is successful next steps is production roll out
1. Go to https://techzone.ibm.com <br>
2. Find your collection<br>
3. Create a reservation to test your template<br>

### 8. For **Production rollout** your VM folder _(vm_template_id)_ in "templates-shared" needs to be copied to "templates" (production folder). This can only be completed by admins

Procedure on how to create a collection:<br>
https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/techzone-content.md#how-to-create-a-collection
  
Procedure to template to collection:<br>
https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/template-an-ibm-cloud-classic-vm-for-your-collection.md
  
Procedure to onboard the Template:<br>
https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/VMwareTemplateOnboarding.md<br>

Send Folder name and Collection name/url to techzone.help@ibm.com or #itz-techzone-support to have this completed<br>

Example mail<br>

**Subject:** VMware Template to Production<br>

**Collection name/url:**<br>

**Folder name in "Templates-shared":**<br>

**Required Region:**<br>

Note: if you require access in other data centers please include it in your production request. Only WDC04, WDC06, FRA04, TOK02 are currently available.<br>

Once completed <br>
- create your environment in your collection _please note:_ vm_template_folder name should be **"templates"** for production templates)<br>
- update old Template Builder environment status to "disabled"<br>
- if you create a new collection, retire old collection<br>
