## VMware template onboarding to Production

1. You need to Template to collection if you are working from a new reservation Template your reseervation to your collection by clicking [Template to collection](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/template-an-ibm-cloud-classic-vm-for-your-collection.md) from your dash board menu. Diregard step 1 if you have completed your Template to collection action.

2. Go to the new environment to get your **'vm_template_id'** and **'vm_template_folder'** this is required to onboard your template. 

To identify your environment **'vm_template_id'**, 
- click edit on the top right of your collection the environment within a collection and check the 'vm_template_id'
- scroll to Environment, click on edit environment
- scroll to Terraform Variables Overriding, Under **name** 'vm_template_id' column **new value** you will find the associated 'vm_template_id'

To identify your environment  **'vm_template_folder'**, 
- click edit on the top right of your collection the environment within a collection and check the 'vm_template_folder'
- scroll to Environment, click on edit environment
- scroll to Terraform Variables Overriding, Under **name** 'vm_template_folder' column **new value** you will find the associated 'vm_template_id'

3. Create a support case using the [Support webform](https://ibmsf.force.com/ibminternalproducts/s/createrecord/NewCase?language=en_US) or send a mail to techzone.help@ibm.com

**Subject: VMware "template onboarding request"**

a. Collection url/ name

b. Environment name

C. vm_template_id: (Template id)

D. vm_template_folder: template-shared, template-user or templates

It takes 2 to 3 business days to complete a template onboarding request. You will be notified once the template is now available in all regions. 

Next Steps

Update variables required  
- vm_template_folder = **templates**
- vm_template_id = leave as is or update if template folder name changes

**NOTES:** Only templates onboarded by the IBM Technology Zone Support Team is accepted as a Production Templates.

Production Templates are admind owned VMs for environments defined within an enabled collection and stored in folder named **Templates**. 






