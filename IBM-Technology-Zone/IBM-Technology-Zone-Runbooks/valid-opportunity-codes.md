# Valid Opportunity Codes to Input on Reservation Form

This runbook will highligh what opportunity codes are valid and what systems/portals we work with to validate an opportunity code when users are making a reservation from IBM Technology Zone.

**IMPORTANT: We sync new IBM Sales Cloud and Gainsite opportunity codes and relationship IDs every three hours. If you input an opportunity code or relationship ID that was just created in ISC or Gainsite, then please wait approximately three hours for our automated sync to pull new values from each database.**

Example of Reservation form and the opportunity code field:

Selecting one of the following purposes will require a valid opportunity code: Customer Demo, Proof of Concept, Proof of Technology.

![opportunity code field](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/opportunity%20code%20field.png)

## What is a Valid Opportunity code? 

Technical Sellers - All IBM Sales Cloud opportunity codes that are not in a "lost" sales stage are considered valid opportunity codes.

Customer Success Managers using Gainsite - Relationship IDs that are open and active are considered valid opportunity codes. 

## IBM Sales Cloud (ISC) Opportunity codes

Reference [ISC Knowledge base](https://ibm.seismic.com/Link/Content/DCH8lALRujMky5k13vpI6KCg) for additional information on Sales Cloud. 

![ISC Opp code](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/ISC%20Opportunity%20number.png)

Opportunity Number:

In ISC the opportunity number is visible on the URL when you are on the Opportunity record.
The field "Opportunity Legacy ID" is visible on the 'All  Opportunities' view under the Opportunities tab. It contains the ISC  opportunity number except in the following cases:

* For opportunities migrated from other systems (e.g. Atlas ), you will see the original Opportunity Number on the Opportunity Legacy ID field. 
* For opportunities owned by BPs, you will see the BP Opportunity Number (BP xxx) on the Opportunity Legacy ID field.  

You can search by opportunity number using the Global Search bar at the top of the screen. See Finding an Opportunity. However, 

* For migrated opportunities, you will not find them by the new ISC number only by the original. 
* For opportunities owned by BPs, you  will not find them by the ISC number, only by the BP xxx number.

The ISC opportunity number consists of 18 characters but most down stream applications only use the first 15 characters.


## Gainsite Relationship ID (Customer Success Managers CRM)

IBMr ONLY - Reference [Gainsite Community](https://w3.ibm.com/w3publisher/gainsight-user-community/education/csm-enablement) for more information on Gainsite CRM.

You can now use the unique ID for any relationship to search, when trying to find a relationship to associate a draft email to, using the email to timeline feature.
There are two ways to find this unique ID.
  
1. Navigate to the dashboard Search: All Companies by Name. Using the dashboard search options, find the relationship you are looking for, and copy the value showing under GSID:

![gainsite search options](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/Gainsite%20search%20options.png)

 2. You can also take the unique ID from the end of the URL when you are on the relationship 360 page:
 
 ![relationship id example](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/relationship%20id%20example.png)
 
 3. You can now use this value to search and find your specific relationship.
 
![step 3 relationship id](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/step3relationship%20id.png)


## How to reserve if you do not have a valid opportunity created yet

If you are working with a customer and you do not yet have an opportunity logged in ISC or Gainsite CRM tool, then please proceed with the following:

1. Select one of the following purpose types on the reservation form: Self education or Testing

Note: These fields will not require an opportunity code or relationship ID and will still allow you to reserve the environment. 

**IMPORTANT: The reservation duration we allow might be less than the duration allowed with providing a valid opportunity code. Reference the reservation duration policy linked from the reservation form to understand reservation durations we allow per purpose and infrastructure. After making a reservation without an opportunity code, please take note of the reservation end date and contact support 2 days prior to the environment expiring so our team can work with you on getting approval for a possible extension of your environment reservation. If you have a valid oppotunity that you can now add to the reservation, contact support with your opportunity code and reservation ID so that they can update the reservation with this information.**

Reservation duration policies linked on reservation form:

![reservation duration policy link on form](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/reservation%20duration%20policy.png)

