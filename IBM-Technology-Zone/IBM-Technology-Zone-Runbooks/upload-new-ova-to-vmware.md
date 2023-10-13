# Upload new OVA/OVF files to VMware in Techzone 
This will guide you through the steps to upload your new OVA/OVF files for your environment to the VMware on IBM Cloud infrastructure. <br>

# SUPPORT DETAILS:
TechZone Help:  https://techzone.ibm.com/help<br>
Under "How can we help?" on right side, look for:  "Site issues - Open a case or Email: techzone.help@ibm.com"<br>

Link to open Support Case:  https://ibmsf.my.site.com/ibminternalproducts/s/createrecord/NewCase?language=en_US  <br>

Procedure on how to open a Support Case:<br>
https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/open_case_web_internal.md <br>

# PREREQS: 
NOTE: User need (1) Template Builder Reservation created and (2) the OVA/OVF files and ISO files (If needed):

(1) User will need a Template Builder reservation provisioned beforehand which will be used to upload the OVA/OVF and ISO (if needed) files to VMware in TechZone.<br>
a. Create a Template Builder reservation<br>
https://techzone.ibm.com/collection/tech-zone-certified-base-images/journey-vmware-on-ibm-cloud-environments<br>
Scroll down and search for Template Builder.<br>

Click on "Reserve" <br>
![OVAa](https://media.github.ibm.com/user/334015/files/469e76f9-4c64-4d4b-83d0-b0d03b720bc4)

b. Select and enter the information. Click on "I agree" checkbox and "Submit for Approval" (right bottom blue button to create a reservation) <br>
![OVAb](https://media.github.ibm.com/user/334015/files/b38daa4b-0419-404e-aaaa-a4801198f20d)

c. Wait for email or check status on TechZone website to see that Template Builder reservation is in "Ready" Status.<br>

(2) User need have the following ready for uploading to your Template Builder environment:<br>
a. OVA/OVF files (example Use VMware Fusion to export a VM image to OVA/OVF or use ovftool)<br>
  NOTES: OVA - a single compressed and zipped file and OVF - individual files<br>
b.ISO file (if needed with your OVA/OVF when prompted for uploading to TechZone) <br>
  
# REFERENCES:
Deploy and Export OVF and OVA Templates<br>
https://docs.vmware.com/en/VMware-vSphere/8.0/vsphere-vm-administration/GUID-AFEDC48B-C96F-4088-9C1F-4F0A30E965DE.html

# PROCEDURE:
## 1. In TechZone, access your Template Builder reservation 
https://techzone.ibm.com/dashboard<br>

Click on pulldown "My library" -> "My Reservations"<br>
![OVA1](https://media.github.ibm.com/user/334015/files/622b4c52-4b4f-4c4f-b2a8-057bf4b523c0)

Click on Blue box with Arrow to View<br>
![OVA2](https://media.github.ibm.com/user/334015/files/40437525-57c2-4221-93d0-ff4469bbfde8)

Click on blue box "Open your IBM Cloud environment"<br>
![OVA3](https://media.github.ibm.com/user/334015/files/c27fd9de-0267-481f-a393-c1273dd02d80)

## 2. **Login to your environment in VMware** 
-Click on "Remote Desktop" to access your environment in VMware<br>
![OVA4](https://media.github.ibm.com/user/334015/files/efda8356-24db-46b4-abe0-574e6c18f793)

- Log into vSphere using the credentials at the bottom of your Template Builder reservation.<br>
  Open Firefox Browser and open URL to vCenter Console URL (via VPN or Bastion) at the bottom of your Template Builder reservation.<br>
  
  Example: https://itzna-vc.na.cloud.techzone.ibm.com/ui
![OVA5](https://media.github.ibm.com/user/334015/files/1f9e8ec6-5011-426e-8e73-88398c14ca72)

  
  NOTE: If Firefox browser's default vCenter Console URL does not match the Reservation's vCenter Console URL, change the Browser home settings<br>
        From Browser's hamburger menu on left:<br>
        Select Settings -> Click Home icon<br>
        Change "Homepage and new windows" to the correct vCenter Console URL<br>
 
 ![OVA6](https://media.github.ibm.com/user/334015/files/970d63b0-518a-4f62-a060-c23bc287cbc9)
 
 - Create your folder in vSphere under **templates-shared.** Short unique naming conventions advised<br>
  NOTE: If there are permission errors, notify VMware admin to check permissions for the templates-shared folder<br>
  ![OVA15](https://media.github.ibm.com/user/334015/files/0223773a-92ce-4082-86e5-2c91fe72b2fc)
  
![OVA7](https://media.github.ibm.com/user/334015/files/c2a2d684-63ea-4298-93fe-ddcbad5d004b)

- Create Tag first and then Assign Tag to Template Folder (Tags are used to identify template owner)<br>
     a. Right click on template folder -> Select "Tags & Custom Attributes" -> Select "Assign Tag"<br>   
![OVA25](https://media.github.ibm.com/user/334015/files/49c4b960-332a-48b5-885b-b2e98768abd5)

     b. Click on "ADD TAG" on Top left corner<br>  
![OVA26](https://media.github.ibm.com/user/334015/files/e661fef4-538b-44f3-82d4-e4680d12eb55)

     c.  Type in the information:<br>
       - Name:  Type First and Last name<br>
       - Description:  enter your IBM id email , vm_template_id name and Collection URL<br>
              -If you have mutiple Collections update your tags to include them<br>
       - Category:  Clear the text and Type in Owners<br>
       - Click "CREATE"<br>
![OVA27](https://media.github.ibm.com/user/334015/files/2e8bef4f-ff0e-4193-93cc-4d9ec2a9b247)

    d. Your created Tag should appear in the list, use filter to find your tag, click the check box to select and click "ASSIGN"<br>
![OVA28](https://media.github.ibm.com/user/334015/files/7f19891f-c626-4e65-88db-c7b2d57981c5)


## 3. **Upload the OVA/OVF files to vSphere**
- Right click on template folder, Select "Deploy OVF Template"<br>
![OVA9](https://media.github.ibm.com/user/334015/files/4b13319c-63c4-4edd-ba13-c14e5559e143)

- In "Select an OVF Template" screen, Select "Local File" and Click "UPLOAD FILES"<br>
NOTE: The OVF/OVA and ISO file (if required with your OVA/OVF) need to downloaded to the Template Builder VM beforehand<br>
(For example, From the Template Builder VM, Open your BOX URL link where the OVF/OVA and ISO files are stored and download from BOX URL to local "Downloads" folder)<br>
![OVA10](https://media.github.ibm.com/user/334015/files/98eb05eb-7fea-4ab9-bfff-706a3046d5b7)

- Select all the OVA/OVF template files and ISO file (if required) and Click "Open"<br>
NOTE: The tool will warn you if there are missing required files <br>
![OVA13](https://media.github.ibm.com/user/334015/files/511e4196-f38e-4afa-9a90-fb009f2a7bda)

NOTE: If ISO file not selected, will see this error <br>
![OVA12](https://media.github.ibm.com/user/334015/files/c9f99696-ab04-4cdf-ad49-253931e1c654)

See the number of files selected and Click "NEXT"<br>
![OVA14](https://media.github.ibm.com/user/334015/files/a5c05393-fef0-430b-abd9-d303295cb618)

- Select your local Template Builder compute resource and Click "NEXT"<br>
NOTE: If get permission errors, notify VMware Admin to check permission.<br>
![OVA16](https://media.github.ibm.com/user/334015/files/5e1d6b96-2b8c-4b0b-a8f3-97d6011ce77f)

![OVA20](https://media.github.ibm.com/user/334015/files/23e3f3ef-28cd-47a5-a341-98cd1e83362c)

See "Review Details" screen and Click "NEXT" <br>
![OVA21](https://media.github.ibm.com/user/334015/files/4b51ccd3-f265-4cfe-913a-3f4650996aba)

- Select the storage and Click "NEXT" (Select datastore with the word template in it and with enough free space to store template)  (Example - "datastore-wdc04-templates"):<br>
NOTE: If get permission errors, notify VMware Admin to check permissions.<br>
![OVA17](https://media.github.ibm.com/user/334015/files/46748b80-9126-4ab9-a7e4-bd6a5b15b18f)

![OVA22](https://media.github.ibm.com/user/334015/files/48bc5714-49c2-4d5f-a808-f23280e2b37d)

- Select the network "gym-segment-shared" and Click "NEXT" <br>
NOTE: If get permission errors, notify VMware Admin to check permissions.<br>
![OVA18](https://media.github.ibm.com/user/334015/files/8f063aca-a49f-4952-a635-0a397bc03481)

![OVA23](https://media.github.ibm.com/user/334015/files/f238c5c5-036e-4735-acb2-fd7207bc4afc)

- Click Finish, please wait for the recent task to complete before proceeding to next step<br>
![OVA24](https://media.github.ibm.com/user/334015/files/b5a37243-98c7-4256-b780-073882ea93df)


## 4. **Upgrade vSphere compatibility**
Right Click on the VM Template file, Select "Compatibility" -> Select "Upgrade VM Compatibility" <br>
![OVA29](https://media.github.ibm.com/user/334015/files/72f70516-69fa-4fce-9f06-6ee6923a8ac5)

Click "YES"
![OVA30](https://media.github.ibm.com/user/334015/files/9b7189d2-eb17-482d-aa69-a1a19e51654a)

- Configure for compatibility as seen below and Click "OK"<br>
![OVA31](https://media.github.ibm.com/user/334015/files/3c5ab5d0-8add-41d1-aeb8-184a69bb9de2)


## 5. **Clone your VM to Template, right click the vm, select Clone, clone to template**
Right Click on VM -> Select "Clone" -> Select "Clone to Template"<br>
![OVA32](https://media.github.ibm.com/user/334015/files/63d0ca8b-dcf8-4846-85d5-574614874628)

Type in VM template name -> Click "NEXT":<br>
![OVA33](https://media.github.ibm.com/user/334015/files/471ff2ef-a0c0-4586-ad11-b7f1e2910a39)

Expand POD folder (itz-wdc04) -> Select a Compute Resource -> Click "NEXT"<br>
![OVA34](https://media.github.ibm.com/user/334015/files/1f13959f-1438-4044-8840-44bdcad57ae5)

Select storage (Select storage with the template in the name) -> Click "NEXT"<br>
![OVA35](https://media.github.ibm.com/user/334015/files/0aa0abe0-105d-4a9f-9b00-52eb7fd9b50f)

Review and Click "FINISH"<br>
![OVA36](https://media.github.ibm.com/user/334015/files/fcc0104d-4038-4018-8a1a-1772393b17eb)


## 6. **To test your migration **Create Techzone environment**, please create your own collection and follow the exact same steps.
Edit Your Collection: https://techzone.ibm.com/collection/YOURCOLLECTION

Sample Settings for Account pool , Cloud Account, Geo , Region, Datacenter :<br>
![OVA37](https://media.github.ibm.com/user/334015/files/13fca72d-02cf-4af3-ab2d-8c23d052cd65)

Sample Network settings:<br>
![OVA38](https://media.github.ibm.com/user/334015/files/211270fd-12d2-44e8-8d6b-bf97cdb2fced)

Default Variables required:<br>
- Infrastructure - where to deployed. For example "IBM Cloud"<br>
- GitOps Patterns - Provisioning instructions - Select "vmware-template"<br>
- Account pool - Location - Select the different locations (itzvmware), Cloud Account (itzvmware), Geo (Americas), Region (us-east), Datacenter (wdc04)<br>
- vm_template_folder - parent folder name. For example "templates-shared"<br>
- vm_template_id- the template folder name for the VMs<br>
- vm_map_string - values for the VMs - make sure your VM Map string is correct, you can use any JSON validators like https://jsonlint.com/) <br>
- vm_domain - Network domain for the VM<br>
- vm_router_ip - Router for the VM<br>
- vm_subnet - Subnet for the VM<br>

Note: If you do not have custom Network requirements, use the defaults values below for the Network details:<br>
Default vm_domain value is ibmdte.net<br>
Default vm_router_ip value is 10.0.0.254<br>
Default vm_subnet value is 10.0.0.0/24<br>

Example of a vm_map_string: <br>
{ 	"GKLM41-20230105": { 		"ip": "10.0.0.1", 		"hostname": "host-1", 		"stage": 1 	} }<br>
"GKLM41-20230105" - Template file name<br>
"ip": "10.0.0.1" - IP address for the VM<br>
"hostname": "host-1" - Hostname for the VM<br>
"stage": 1 - create and launch first (order to create a VM which has no dependency)<br>
"stage": 2 - Optional if have more than 1 VM and there are dependencies: create and launch second (create after stage 1 has been created - dependent on stage 1 creation)<br>
"stage": 3 - Optional if have more than 1 VM and there are dependencies: create and launch third (create after stage 2 has been created - dependent on stage 2 creation)<br>

Published Services variables (if adding ports to be exposed as publish services, add port variable to the vm_map_string):<br>
https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/VMwarePublishedServices.md<br>

## 7. Once all these are completed create a **Test reservation**, if testing is successful next steps is production roll out
1. Go to https://techzone.ibm.com <br>
2. Find your collection<br>
3. Create a reservation to test your template<br>

## 8. For **Production rollout** your VM folder _(vm_template_id)_ in "templates-shared" needs to be copied to "templates" (production folder). This can only be completed by admins

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
