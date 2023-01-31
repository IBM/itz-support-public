## VMware template onboarding to Production

Only templates onboarded by the IBM Technology Zone Support Team is accepted as a Production Templates.

Production Templates are admind owned VMs for environments defined within an enabled collection. 
Production templates are stored in folder named **Templates**. 

To identify your environment folder name, edit the environment within a collection and check the **'vm_template_folder'**, template-shared and template-user are temporary folders.

## Steps to request a VMware template onboarding

To have your template/ VM copied to production, send a note to techzone.help@ibm.com

**Subject: VMware "template onboarding request"**

a. Collection url/ name

b. Environment name

C. Template id: vm_template_id or Template name in "Template Shared" folder

d. regions additional copies are required for. Supported Regions (DAL10, WDC04, FRA04, TOK02)

You will be sent a response once move to production is completed.  Please note if you don't specify a region, your template will be onboarded only in Dal 10.

Next Steps Add/update your vmware environment to your collection. 

Update variables required  
- vm_template_folder = **templates**
- vm_template_id = leave as is or update if template folder name changes






