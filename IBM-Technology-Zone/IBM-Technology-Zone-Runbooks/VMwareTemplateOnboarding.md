# VMware template onboarding to Production

There are two ways to have your template onboarded to production
1. By Providing the vm_template_id name from your [Template to collection](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/template-an-ibm-cloud-classic-vm-for-your-collection.md) environment
2. By Providing template name in folder Template-Shared (Applicable only to Auhtors that completed Skytap to VMware migrations and have access to template-shared in vcenter)

  All templates need to be onboarded correctly to ensure user environment provisioning do not fail. Follow steps listed below.

## VMware template onboarding from "Template to collection"
Now that your Template has been successfully created it needs to be onboarded before you update your environment configuration setting follow steps to get this completed.

1. Send a VMware "template onboarding request"** to the TechZone Support Team
Complete a [webform](https://ibmsf.force.com/ibminternalproducts/s/createrecord/NewCase?language=en_US) or send an email to techzone.help@ibm.com

**Subject: VMware "template copy/onboarding request"**

a. Collection url/ name: 

b. Environment name:

C. vm_template_id: 

Note: To obtain **'vm_template_id'**, 
- click edit on the top right of your collection 
- scroll to Environment, click on edit environment
- scroll to Terraform Variables Overriding, under **name** 'vm_template_id' column **new value** you will find the associated 'vm_template_id'

It takes **2 to 3** business days to complete a template copy/onboarding request. You will be notified by the support agent when the template is available in all TechZone supported regions. 

Next Steps: Update your environment configuration settings and Terraform Variables Overriding

**Settings**

- Account Pool: itzmware
- Cloud Account: Any
- Geo: Select preferred geo (Americas,Europe or AP)
- Region: Any
- Datacenter: Any
- Click the + sign to enter your entry
  
Repeat steps to add additional Geo's

**Terraform Variables Overriding**
 
- vm_template_folder: **templates-user**
- vm_template_id: leave as is

- Save the environment on your collection and wait for the confirmation notification that the save was successful.
- Save the collection and wait for the confirmation notification that the save was successful.


## VMware template onboarding from "Template-shared"
1. Send a VMware "template onboarding request"** to the TechZone Support Team
Complete a [webform](https://ibmsf.force.com/ibminternalproducts/s/createrecord/NewCase?language=en_US) or send an email to techzone.help@ibm.com

**Subject: VMware "template copy/onboarding request"**

a. Collection url/ name: 

b. Environment name:

C. Template name in Folder **Template-shared**

It takes **2 to 3** business days to complete a template copy/onboarding request. You will be notified by the support agent when the template is available in all TechZone supported regions. 

Next Steps: Update your environment configuration settings and Terraform Variables Overriding

**Settings**

- Account Pool: itzmware
- Cloud Account: Any
- Geo: Select preferred geo (Americas,Europe or AP)
- Region: Any
- Datacenter: Any
- Click the + sign to enter your entry
  
Repeat steps to add additional Geo's

**Terraform Variables Overriding**
 
- vm_template_folder: **templates**
- vm_template_id:Template name in Folder **Template-shared**

- Save the environment on your collection and wait for the confirmation notification that the save was successful.
- Save the collection and wait for the confirmation notification that the save was successful.

**NOTES:** Only templates onboarded by the IBM Technology Zone Support Team is accepted as a Production Templates.

Production Templates are admin owned VMs for environments defined within an enabled collection and stored in folder named **Templates** or **Templates-user** 


For any questions, contact ITZ support - techzone.help@ibm.com



