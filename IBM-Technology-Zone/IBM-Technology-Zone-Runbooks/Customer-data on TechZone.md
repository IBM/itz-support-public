
# Customer Data Enabled Environments on IBM Technology Zone

As of July 18th, IBM Technology Zone released a select set of environments that will support specific classifications of customer data. IBM Technology Zone's [Terms and Conditions](https://techzone.ibm.com/terms) have been updated per BISO and Legal guidance. Additionally, [End User Security Policies](https://techzone.ibm.com/terms/securitypolicy) have been added to the Terms and Conditions to maintain a compliant and secure platform for all users. Continue reading this runbook to understand the classifications of Customer Data that we do/do not support, new feature functionality added the site to support this iniatitive, and other updates regarding provisioning process updates and email template changes. 

Supported Customer Data Classifications:
- Publicly available (example of data available through the web is [BERKELEY SETI RESEARCH CENTER](https://seti.berkeley.edu/listen/data.html))
- Anonymized / Obfuscated / Masked
- Non-PI

NOT Supported Customer Data Classifications: 
- No regulated data allowed. Regulated - PI, SPI, PCI, PHI, Financial Data, Other.
- Governed by a plethora of global/federal/local regulations- GDPR, HIPAA, GLB, FTC, CCPA, Sarbanes-Oxley, + many others. Regulated data **requires** engaging Legal & BISO. 

### Customer Data Classification Support
If you need support classifying customer data or a risk assessment associated with your engagement, please contact the Corporate BISO team directly in Slack: #corporate-biso-help. 

## Regulated Customer Data Environment Requests

If you have an environment that needs regulated customer data or you need an environment on TechZone that does not support the customer data option, please submit a [TechZone Custom Request](https://ibm.biz/custom-techzone-requests) and select request type 'Customer Data Environment' to get started with this process. Provide the environment name and collection URL for the environment on TechZone that does not currently allow for customer data in your request. 

_**NOTE: Customer data environments need to go through Business Information Security Office (BISO) for legal approval before the IBM Technology Zone team can proceed with setting up your environment. Get started by submitting your custom request for the TechZone team to review and to begin this process and please be aware that this process can add an additional month for necessary legal reviews.**_

![Customer Data Type](https://github.com/IBM/itz-support-public/blob/2bb827675a967ac45c49644be1f421c40e12d57a/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/customerdatatype.png)

**IMPORTANT - Email your [legal "one-pager"](https://www.ibm.com/support/customer/csol/terms/internal/?id=Z126-9237&cc=us&lc=en#detail-document) to the client prior to working with their data. (*signature not required). If customer has any concerns with agreement, you must engage with legal. Legal is working w/ CIO office to create a “contract generator” which will supersede existing “one pager” at a future date.**

Additional information on IBM's PI/SPI Taxonomy can be found here: https://ibm.ent.box.com/s/pshzqj3lh38uqlwog6v602jea4tdc9qq

The following environments are enabled to allow for supported customer data classifications on TechZone: 

• [TechZone Certified VMWare Offerings](https://techzone.ibm.com/collection/tech-zone-certified-base-images/journey-vmware-on-ibm-cloud-environments) (*excludes Windows)

• [TechZone Certified Base Images](https://techzone.ibm.com/collection/tech-zone-certified-base-images/journey-watsonx) - watsonx Environments - Ensure to select 'Dedicated' account option on reservation form when reserving with customer data

• [Technology Patterns Customer Care Environments](https://techzone.ibm.com/collection/technology-patterns/journey-ai-assistants)

• [Data, AI & Automation Demobuilder Environment](https://techzone.ibm.com/collection/data-ai--automation-demobuilder/environments)



## Customer Data Experience Updates

1. **Terms and Conditions** - All IBM Technology Zone users, must re-accept the new [Terms and Conditions](https://techzone.ibm.com/terms) to sign into IBM Technology Zone. Along with the updated Terms page includes the addition of a new [End User Security Policies](https://techzone.ibm.com/terms/securitypolicy) page that users are agreeing to as part of overall Terms of Use. Not agreeing to the new Terms and Conditions and End User Security Policies will limit users from being able to login to the site. Agreeing to the new Terms and Conditions will immmidietly log the user into the site for continued use. 

![Terms and Conditions page](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/TermsConditions.png)
*Please note that content on this page may have been updated since this image was captured.*
*Find the most recently updated Terms and Conditions content here: https://techzone.ibm.com/terms*

2. **Reservation Form Updates** - For the selected set of customer data enabled environments on IBM Technology Zone, there are additional fields and logic when making a reservation in order to capture customer data datapoints for tracking purposes. Three fields are impacted on the reservation form as shown below in image: 1. Purpose, 2. Customer Data, and 3. Terms and Conditions. 

![additional customer data fields](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/Additional_customerdataFields.png)

- Purpose - To enable the Customer Data options on the reservation form, users must select one of the two purpose options: Customer Demo, Proof of Technology. Supported Customer Data classifications can be used on client facing purpose reservations only. Selecting Self Education and Test purpose options will not prompt the additional Customer Data field as NO customer data will be allowed on reservations with these purposes. 

- Customer Data - This new Customer Data field has been added to ensure that we can track which reservations are intending to use supporting customer data classifications on the environment, while also reiterating the types of Customer Data classifications that we do NOT allow. 

- Terms and Conditions - To ensure a compliant and secure platoform, every user making a reservation on IBM Technology Zone must adhere to the Terms and Conditions agreed upon to access the site and re-agreed on every reservation form. These changes were designed to protect Customer's Data, IBM Technology Zone, and IBM.  

*NOTE: Please ensure that you have filled out/agreed to the above three fields on the reservation form accurately as these datapoints can NOT be updated or changed after the reservation form has been submitted.* 

3. **Reservation Details Page** - To reference after a reservation has been created which Customer Data yes or no option was selected, users can navigate to their Reservations details page. To get to the Reservation Details page, select the My Library menu option in the top navigation bar and select My reservations in the drop down list. Then selecting a reservation tile will navigate you to the Reservation details page for that reserved environment. Find the Customer Data True or False data point in the Environment section as show below in image. 

- False = "No, I will not be using customer data." option was selected on the reservation form.
- True = "Yes, I will be using customer data that is NOT regulated. I understand that PI, SPI, PCI, PHI, financial, or other regulated data is NOT allowed." option was selected on the reservation form. 

![Reservation Details Page](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/reservationdetailspage.png)

4. **Transferring** - Reservations that have Customer Data set as true will not be transferrable. At this time, we capture Customer Data use on reservation and a re-agreement on every reservation form for the environments enabled for supported customer data classifications. The original reservation owner/creator agrees to these terms and classifys data on this reservation experience and this information can not be transferred or reclassified after creation. Since this data can not be updated/modified after creation, ownership of these reservations can NOT be transferred as well. An alert will display on the Transfer modal and the Transfer submit button will remain greyed out to show this action can not be completed. 

![No transfers](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/NOTransfer.png)

5. **Sharing** - Reservations that have Customer Data set as true can be shared to another active TechZone user. An active TechZone user is defined as a user that has agreed to TechZone's Terms and Conditions to access the site. Customers, Business Partners, and IBMers that have an IBMid can access TechZone today after agreeing to Terms and Conditions. When sharing a reservation that has Customer Data, please ensure that the user has logged into TechZone and agreed to the Terms and Conditions. Users that have not accepted TechZone Terms and Conditions are not permitted to access or use TechZone environments in any way. Provide the IBMid email of the active TechZone user that you would like to share the reserved environment with and click Share submit button. This will populate a copy of the reservation on this users reservation page for them to access the reserved environment.

![share customer data environment](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/Share_customer_data.png)

6. **Email updates** - All reservation email templates have been updated to remove environment access credentials. To access a TechZone reserved environment all users must login to TechZone and navigate to their My reservations page and select the reservation tile in which they would like to access. Access credentials can be found on the Reservation details page.

7. **Provisioning Updates** - Client facing reservations (purpose: Customer Demo, Proof of Technology) with customer data will be provisioned in dedicated infrastructure to ensure a secure environment for supported customer data classifications as listed at the top of this runbook document. Due to provisioning into these dedicated client facing pods, no reservation purpose field and/or customer data datapoint can be updated after the reservation has been created. For example: Self education and Test reservation purposes may not be updated after the reservation has been scheduled due to the deployment placing the environment in a non-client facing infrastructure. The same goes for a Customer Demo and Proof of Technology reservation, as no purpose can be updated after creation of the reservation due to the environment being scheduled for deployment on a dedicated client facing infrastructure.
