<h1 align="center">Requesting TechXchange Lab Migrations to TechZone</h1>


## Getting Started

You own an environment that was used at a TechXchange event and you would like to have migrated so others can make a reservation directly on TechZone. 



1. You need to have a Collection in order to migrate your environment. 
    -  - If you already have a existing **Collection** on TechZone, proceed to step 2. 
       - If you don't have a Collection, following these instructions below:
            - To create your own collection, first review TechZone [Guidance and Standards](https://github.com/IBM/itz-support-public/blob/fc85f09311284f164fd4b49979bd9a27e5a8000f/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/techzone-content.md#L4)
           - Create a Collection - see ["How to Create a Collection"](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/techzone-content.md#how-to-create-a-collection). 
           - Add **Resources**- [How to Create a Resource](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/techzone-content.md#how-to-create-a-resource-on-a-collection), explaining the lab guide and as a Resource Document type
           - Have the new Collection reviewed by mbawa@us.ibm.com before proceeding to step 2.

> **TechXchange Instructor Collection Creation Guidance:**
>
> * New collections to be created only for the recent TechXchange assets, are encouraged to title the collection the same name used for the session so that those that attended can easily find the assets on TechZone. 
>
>* Collections should include the environment used for the TechXchange lab session and the Lab Guide as a supporting resource to accompany the environment.
> 
> Contact mbawa@us.ibm.com to review new collection before proceeding to step 2.
     
2. Reach out to TechZone support team by [opening a case](https://ibmsf.force.com/ibminternalproducts/s/createrecord/NewCase?language=en_US) or by email [techzone.help@ibm.com](techzone.help@ibm.com) to request your lab to be migrated to TechZone. Provide the following details in your request: 
    -  -  The Collection name and direct URL link to the collection.
       -  The Session ID.

>  _**DISCLAIMER:** Please be aware of the following steps that are taken before the template transfer can proceed:_
> 
>  _* ISOs associated with the source template will be unmounted._
> 
> _* Snapshots associated with the source template will be deleted._
> 
> _The Aspera automation that does the template transfer tends to fail unless the above steps are taken._
> _If this process is disruptive to your template, please communicate with Support so we can determine other available options._

3. The TechZone support team will respond back with a text file and a link to Onboarding Environment to a Collection (next section) for you to take next steps for onboarding your environment onto TechZone.


## Onboard the Environment to a Collection

The text file the TechZone support team will provide you is the following: 

> Terraform Variables Overriding
> ------------------------------
> vm_template_id
> 
> vm_template_folder
> 
> vm_map_string - CONTENT AUTHOR TO UPDATE THE JSON STUB FILE PROVIDED BY TECHZONE SUPPORT
> 
> vm_subnet
> 
> vm_router_ip
> 
> vm_domain
> 

Follow guidance below to ensure that you copy and paste this information correctly into the environment entry. 

1. Navigate to your collection and select edit: https://techzone.ibm.com/my/collections?StatusFilter=%5B%22Active%22%2C%22Draft%22%2C%22Pending+Approval%22%5D

    - - Scroll down the collection edit form and locate the environment section

      - Select 'Add an environment' button

![xchange-add-an-environment](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/xchange-add-an-environment.png)

2. Provide a title for the environment and select IBM Cloud from the Infrastructure drop down list

   -  - Provide a description for the environment for users to identify what they are reserving 

      - Select 'vmware-template' from the GitOps Pattern drop down list

**NOTE: vmware-template is for VMware only**

![xchange-create-details](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/xchange-create-details.png)

3. Under the Settings section, follow the below steps to setup this section:

    - - Select 'itzvmware; from the dropdown menu under the Account Pool field 

      - Select 'itzvmware' from the dropdown menu under the the Cloud Account field

      - Select 'Any(preferred)' from the dropdown menu under the Geo field

      - Select 'Any(preferred)' from the dropdown menu the Region field

      - Select 'Any(preferred)' from the dropdown menu the Data Center field

**NOTE: Ensure that you press the "add" button, otherwise your inputted values will not be saved!**

![xchange-add-button](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/xchange-add-button.png)

![xchange-added](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/xchange-added.png)

4. Under the Terraform Variables Overriding section, follow the below steps to ensure each variable is setup correctly

    -  - Adding the VMWare template ID variable:

       - Name field, select from the drop-down menu list 'vmware_template_id'

![xchange-template-id](/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/xchange-template-id.png)

-  - Adding the VMWare Template Folder variable:

        - Select vm_template_folder add the New value and Click on the + icon

        - Select vm_map_string from pulldown and add the New value and Click on the + icon

            * Follow guidance on how to build out map string variable by referencing [Step 6 of Upload OVA to VMWare Runbook](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/upload-new-ova-to-vmware.md#6-to-test-your-migration-create-techzone-environment-please-create-your-own-collection-and-follow-the-exact-same-steps). 
            * Follow guidance on how to build out map string for an image by referencing the [Published Services runbook](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/VMwarePublishedServices.md). 



        - Select vm_subnet from pulldown and add the New value and Click on the + icon

        - Select vm_router_ip from pulldown and add the New value and Click on the + icon

        - Select vm_domain  from pulldown and add the New value and Click on the + icon
-   - Click the bottom blue Save button" to save the "Terraform Variables Overriding" for the Collection
