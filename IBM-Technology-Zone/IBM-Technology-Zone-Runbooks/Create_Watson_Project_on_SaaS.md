# Create Watson Project on SaaS

## Summary
Instructions and troubleshooting common problems with creating a project within a watson instance on SaaS.

## Steps to create a Project on a watsonx.ai instance on SaaS

1. On the IBM watsonx home, at the top left of the screen, select the menu button.

![watson-menu]()

2. Within the sidebar menu, select the "View all projects" option.

![sidebar-menu-options]()

3. On the right side of the Projects page, select the "New project" button.

![new-project]()

4. Select either Project creation option. 

![project-options]()

5. Fill the project "Name" field. Optionally, fill the "Description" field. Then at the bottom right, press the "Create project" button.

![project-details]()

6. Your project should be successfully created.

### Why can't I create a project on SaaS?
Filter settings are stored as browser cookies and will continue to apply the filter on other pages including the "Creating a new project" page, preventing the user from creating a new project. Resources will not be displayed unless resource groups matching the resources are selected in the filter.

To resolve:
1. Firstly ensure that the user has permissions from the parent reservation owner (unless they are the reservation owner)
2. On the IBM watsonx Projects page, select any previous project.

![select-project]()

3. Next, ensure that you are on the "Manage" tab.

![manage-tab]()

4. Then, on the left menu bar, select "Services and Integrations"

![services-tab]()

5. On the right side of the page, click on the "Associate service" button.

![associate-service]()

6. Remove both the "resource group" filter and select the appropriate "region" filter. Region filter for COS (cloud object storage) is global, so region filter must be deselected, but WML (watson machine learning) is regional, so must match the region that the project was created in.

![filters]()

7. Once the filters have been adjusted, click the "Cancel" button at the bottom right to exit.

8. The user should now be able to create a new project.

## Keywords

IBM watsonx, IBM watsonx.ai, watsonx SaaS, watsonx.ai SaaS
