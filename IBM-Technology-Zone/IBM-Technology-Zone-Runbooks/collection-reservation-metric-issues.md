# Collection reservation metrics not displaying

Use cases related to 'Reservations' metrics not displaying the 'Reservations' option or metrics are not displaying when 'Reservations' option is selected. 


## **FAQ 1: Why doesn't the 'Reservations' option display on my collection options list?**

![reservations option mission](https://github.com/IBM/dte-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/reservations%20not%20displaying.png)

Answer: 'Reservations' option will only display if there is an environment catalogued on your collection. 

Steps to check:
1. Select the collection edit button

![edit collection button](https://github.com/IBM/dte-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/edit%20collection%20button.png)

2. Scroll down to the Environments section to see if there are any environments catalogued on this collection. 

![add an environment](https://github.com/IBM/dte-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/add%20an%20environment.png)

3. Next steps...

- If there are no environments catalogued on this collection that need to be, please use the 'Create an environment' runbook for next steps on how to add an environment to your collection.

- If there is an environment catalogued on this collection, then please contact support with the collection URL so we can create an issue and further investigate this issue.



## **FAQ 2: Why are no reservation metrics displaying after selecting the 'Reservations' option?**

![Reservation metrics not available](https://github.com/IBM/dte-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/reservation%20metrics%20not%20available%20message.png)

Answer: Reservation metrics are captured from environments that are catalogued on a collection and the provisioning pipeline has to be one that IBM Technology Zone team currently supports. If you have an environment catalogued on your collection that is of infrastructure type: VMware Private Cloud (TEC EMEA), Systems Redirect, or Hosted Redirect then please note that these environment options are merely a redirect to another site where then the reservation is to be provisioned from. As we consolidate additional environments from CECC, ISCEP, SCS, TEC EMEA, and more these metrics will start to display on your collections once they are reserved directly from an IBM Technology Zone collection. 

Steps to check:
1. Select the collection edit button

![edit collection button](https://github.com/IBM/dte-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/edit%20collection%20button.png)

2. Scroll down to the Environments section

![add an environment](https://github.com/IBM/dte-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/add%20an%20environment.png)

3. Select an Environment to see the 'Infrastructure' field. 

![infrastructure type](https://github.com/IBM/dte-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/Infrastructure%20type.png)

**IMPORTANT: As stated above, Infrastructure types that are currently setup as redirects will not display reservation metrics.** 

This infrastructure redirect list includes types: VMware Private Cloud (TEC EMEA), Systems Redirect, or Hosted Redirect.

3. Next steps...

- If you have an environment catalogued as one of the infrastructure redirect types and would like to know when the environment is planned to be migrated, please contact brooke.jones@ibm.com. We are currently working with CECC, ISCEP, SCS, SBaaS, and TEC EMEA portals to consolidate environments to IBM Technology Zone.

- If you have an environment that is not of the infrastructure redirect types, as mentioned above, then please contact support as there might be an issue with how the environment is catalogued or there could be issues with the environment itself not taking reservations. 


## SME

brooke.jones@ibm.com
Slack support channel


