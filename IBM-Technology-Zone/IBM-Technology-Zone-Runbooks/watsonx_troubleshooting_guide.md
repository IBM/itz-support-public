# watsonX Troubleshooting Guide

## Summary
Instructions and troubleshooting common problems with creating a project within a watson instance on SaaS.

## Steps to create a Project on a watsonx.ai instance on SaaS

1. On the IBM watsonx home, at the top left of the screen, select the menu button.

![watson-menu](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-menu.png)

2. Within the sidebar menu, select the "View all projects" option.

![sidebar-menu-options](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-sidebar-menu-options.png)

3. On the right side of the Projects page, select the "New project" button.

![new-project](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-new-project.png)

4. Select either Project creation option. 

![project-options](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-project-options.png)

5. Fill the project "Name" field. Optionally, fill the "Description" field. Then at the bottom right, press the "Create project" button.

![project-details](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-project-details.png)

6. Your project should be successfully created.

## Why can't I create a project on SaaS?
Why can't I create a watsonx.ai or watsonx project? Filter settings are stored as browser cookies and will continue to apply the filter on other pages including the "Creating a new project" page, preventing the user from creating a new project. Resources will not be displayed unless resource groups matching the resources are selected in the filter.

To resolve:
1. Firstly ensure that the user has permissions from the parent reservation owner (unless they are the reservation owner)
2. On the IBM watsonx Projects page, select any previous project.

![select-project](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-select-project.png)

3. Next, ensure that you are on the "Manage" tab.

![manage-tab](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-manage-tab.png)

4. Then, on the left menu bar, select "Services and Integrations"

![services-tab](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-services-tab.png)

5. On the right side of the page, click on the "Associate service" button.

![associate-service](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-associate-service.png)

6. Remove both the "resource group" filter and select the appropriate "region" filter. Region filter for COS (cloud object storage) is global, so region filter must be deselected, but WML (watson machine learning) is regional, so must match the region that the project was created in.

![filters](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-filters.png)

7. Once the filters have been adjusted, click the "Cancel" button at the bottom right to exit.

8. The user should now be able to create a new project.

## How to share my project?

The steps below are required in order to share a wastonx project you have created. 

1. Share reservation with user using share menu option on reservation card (not on reservation details page), you can see how to do that as illustrated in the image bellow
![reservations-card-share-watsonx](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/reservations-card-share-watsonx.png)
2. Log techzone support ticket to request IAM Viewer access policy
> Be sure to include your reservation ID and the email of the user you are attempting to share your instance with. It will be helpful to share this runbook with support and ask for the team to check on your permissions
3. Ensure shared user accepts cloud invitation
4. Ensure user initializes watsonx workspace in account and geo reservation was shared from
> Geo Locations direct URLs
- Dallas:  https://dataplatform.cloud.ibm.com/wx/home?context=wx
- Frankfurt: https://eu-de.dataplatform.cloud.ibm.com/wx/home?context=wx
- Tokyo: https://jp-tok.dataplatform.cloud.ibm.com/registration/steptwo?context=wx
- London: https://eu-gb.dataplatform.cloud.ibm.com/wx/home?context=wx
5. Add user to projects as needed

## Why can't I share my WatsonX project with a user?

If you are running into issues sharing a project or a user is not able to view a project that was shared with them, some permissions may be missing. To troubleshoot this:

1. Create a case with Techzone Support.

> Be sure to include your reservation ID and the email of the user you are attempting to share your instance with. It will be helpful to share this runbook with support and ask for the team to check on your permissions

2. Support will check if you have the access policy called "All Account Management Services".

*NOTE: Access to All Account Management Service access is IBM ONLY applicable*


3. If you are not already assigned to that group, the support team will add you, then you can attempt sharing again.

## I can't open watsonx.ai ('Get Started' button instead of 'Launch')

If you are getting stuck with the registration screen when attempting to access watsonx.ai via IBM Cloud please ensure to follow the steps below. 
1. Click 'Get started' button
2. On the tab that opens go to the URL tab and remove the contents of the URL after the slash "/" part of the URL. This is illustrated below. 
The url should look similar to the one in the photo, depending on the geolocation. Notice the highlighted part.
<img width="1725" alt="image" src="https://github.com/IBM/itz-support-public/assets/152641641/6ea4116b-b4d0-4c2d-8845-8abe812e518c">
3. Once you remove the part after the slash "/", the URL should look like this (depending on the geolocation): 

- Dallas:  https://dataplatform.cloud.ibm.com
- Frankfurt: https://eu-de.dataplatform.cloud.ibm.com
- Tokyo: https://jp-tok.dataplatform.cloud.ibm.com
- London: https://eu-gb.dataplatform.cloud.ibm.com

4. Click enter and that will take you to the watsonx.ai homepage. If you are first time user you will be prompted to select the cloud account from your reservation. Check the reservation page and select the same cloud account.


## Why can't I access IBM Cloud?

What Happens If I Do Not Accept the IBM Cloud Invitation? If you do not accept the IBM Cloud invitation, as specifically directed in the reservation details you will encounter an error.

![watsonx Cloud Error](https://github.com/IBM/itz-support-public/blob/1395e12dd3ca6461ec5d19f7feec469108bb6a0d/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watsonx-cloud-error.png)

![IBM Cloud Reservation Details](https://github.com/IBM/itz-support-public/blob/1395e12dd3ca6461ec5d19f7feec469108bb6a0d/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/ibmcloud-reservation-details.png)

To accept the invitation, either navigate to the email you should receive within 24 hours of creating your IBM Cloud account, or navigate to the bell notification icon on the top right of the IBM Cloud page, and on the right side of the screen you will see a notification that says "You are invited to join an account in IBM Cloud", click the blue hyperlink on the right of your screen that says "Join now."

![Bell Icon](https://github.com/IBM/itz-support-public/blob/1395e12dd3ca6461ec5d19f7feec469108bb6a0d/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/ibmcloud-notification.png)

## Why am I getting error "The AWS Access Key ID you provided does not exist in our records"?

![cos-error](https://github.com/IBM/itz-support-public/blob/cb24717ff45c577a2e12d96ff994791330ca81e1/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watsonx-cos-error.png)

The AWS access key error indicates that your COS instance was deleted. The COS instance is deleted either by reservation expiry or user deletion. To resolve, you must create a fresh reservation and re-associate the new COS instance with project.


## Why can't I create a COS instance?
I shared my reservation with a user but they cannot create a COS instance, how can a shared user create a COS instance? Shared users shouldn’t be creating a new COS instance, they should be using the COS instance that came with the reservation. 

This might occur if the COS instance has been deleted, the reservation becomes unusable because all the services might have been deleted. A new reservation must be created.

## Service is disabled, and I cannot select an option

If service is disabled and you are unable to select an option you should try entering the regional watsonx.ai URLs directly.

![watsonx-troubleshooting](https://media.github.ibm.com/user/358578/files/80ee0e90-50ee-4e37-af2f-7cb1c08fe746)

Enter the appropriate regional watsonx.ai URL directly, based on these options:

- Dallas:  https://dataplatform.cloud.ibm.com/wx/home?context=wx
- Frankfurt: https://eu-de.dataplatform.cloud.ibm.com/wx/home?context=wx
- Tokyo: https://jp-tok.dataplatform.cloud.ibm.com/registration/steptwo?context=wx
- London: https://eu-gb.dataplatform.cloud.ibm.com/wx/home?context=wx

## User Facing out of tokens error on watsonx.ai SaaS reservation
Often occurs when a user associates a personal WML instance to their created project. If they were to associate the correct WML, there would not be restrictions such as no tokens, so the user needs to reassociate the WML instance or create a new project with the correct WML.

I have an Out of Token error on my watsonx.ai SaaS reservation. This happens when you associate a personal WML instance to your created project. If you associate the correct WML, there would not be restrictions such as no tokens, so the user needs to reassociate the WML instance or create a new project with the correct WML.

## (Optional) Backing up a project
To back up projects before reservation expires so that you do not lose projects on a dedicated account, you must specify the value of the "_Default install of dedicated services (customer poc), or use shared services? Note that dedicated services include the COS instance that will get destroyed
with your project data upon expiry, so be sure to export your projects as needed when choosing dedicated._" field.

![backup-field](https://github.com/IBM/itz-support-public/blob/52c7807676a1394d1474c90bf6ad8bae0974b0b9/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-backup-field.png)

_Dedicated is an isolated environment. Shared is a shared environment access._

