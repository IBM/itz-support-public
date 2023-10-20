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

## Why can't I share my WatsonX project with a user?

If you are running into issues sharing a project or a user is not able to view a project that was shared with them, some permissions may be missing. To troubleshoot this:

1. Create a case with Techzone Support.

> Be sure to include your reservation ID and the email of the user you are attempting to share your instance with. It will be helpful to share this runbook with support and ask for the team to check on your permissions

2. Support will check if you have the access policy called "All Account Management Services".

*NOTE: Access to All Account Management Service access is IBM ONLY applicable*


3. If you are not already assigned to that group, the support team will add you, then you can attempt sharing again.

## Why can't I access IBM Cloud?

What Happens If I Do Not Accept the IBM Cloud Invitation? If you do not accept the IBM Cloud invitation, as specifically directed in the reservation details you will encounter an error.

![watsonx Cloud Error](https://github.com/IBM/itz-support-public/blob/1395e12dd3ca6461ec5d19f7feec469108bb6a0d/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watsonx-cloud-error.png)

![IBM Cloud Reservation Details](https://github.com/IBM/itz-support-public/blob/1395e12dd3ca6461ec5d19f7feec469108bb6a0d/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/ibmcloud-reservation-details.png)

To accept the invitation, either navigate to the email you should receive within 24 hours of creating your IBM Cloud account, or navigate to the bell notification icon on the top right of the IBM Cloud page, and on the right side of the screen you will see a notification that says "You are invited to join an account in IBM Cloud", click the blue hyperlink on the right of your screen that says "Join now."

![Bell Icon](https://github.com/IBM/itz-support-public/blob/1395e12dd3ca6461ec5d19f7feec469108bb6a0d/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/ibmcloud-notification.png)

## Why am I getting error "The AWS Access Key ID you provided does not exist in our records"?

![cos-error](https://github.com/IBM/itz-support-public/blob/cb24717ff45c577a2e12d96ff994791330ca81e1/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watsonx-cos-error.png)

The AWS access key error indicates that your COS instance was deleted. The COS instance is deleted either by reservation expiry or user deletion. To resolve, you must create a fresh reservation and re-associate the new COS instance with project.


## (Optional) Backing up a project
To back up projects before reservation expires so that you do not lose projects on a dedicated account, you must specify the value of the "_Default install of dedicated services (customer poc), or use shared services? Note that dedicated services include the COS instance that will get destroyed
with your project data upon expiry, so be sure to export your projects as needed when choosing dedicated._" field.

![backup-field](https://github.com/IBM/itz-support-public/blob/52c7807676a1394d1474c90bf6ad8bae0974b0b9/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-backup-field.png)

_Dedicated is an isolated environment. Shared is a shared environment access._

