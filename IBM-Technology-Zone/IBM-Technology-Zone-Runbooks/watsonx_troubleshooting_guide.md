# watsonx Troubleshooting Guide

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

### Why can't I create a project on SaaS?
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

### (Optional) Backing up a project
To back up projects before reservation expires so that you do not lose projects on a dedicated account, you must specify the value of the "_Default install of dedicated services (customer poc), or use shared services? Note that dedicated services include the COS instance that will get destroyed
with your project data upon expiry, so be sure to export your projects as needed when choosing dedicated._" field.

![backup-field](https://github.com/IBM/itz-support-public/blob/52c7807676a1394d1474c90bf6ad8bae0974b0b9/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-backup-field.png)
