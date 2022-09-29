# New Environments Authoring Form

This runbook will explain how to use the NEW (as of 9/28/2022) Environments Authoring Form in a Collection.

## Body

**What's Changed**

* The "GitOps Pattern" field has moved to a new place on the form. This will be used for every Environment Deployment option.
* New Field "Account Pool". This allows us to organize accounts by purpose. In most cases this should be set to "shared".
* "Cloud Account" Field can be "Any" or a specific account. If "Any", any account in the Account Pool will be used, selected automatically at deploy time.
* New Field "Geo". The "Geo" field is used by the user to select with geography they would like to deploy to. Options are "Americas", "Europe", and "AP".
* Field "Region" is specific to Cloud regions (i.e. IBM Cloud us-south). In most cases this should be "Any".
* Field "Datacenter" also has an "Any" option and should be set to "Any" unless this Environment entry will only work in a specific Data Center. When set to "Any" an appropriate data center will be selected within the chosen Geo at deploy time.

**Why This Change**

These changes are in place to support what we call Dynamic Provisioning. Instead of the user having to guess at which location is has the most capacity, we will dynamically place their Environment in the most available location. We will always adhere to the selected Geography, but with Dynamic Provisioning we can change the Account, Region, and Data Center to best fit the Environment at the time of deployment. This will simplify the options for the user as well. All they will have to select is the Geography and we'll do the rest. For the author of these Environment entries, you have flexibility if you need it when an Environment can only be deployed in a certain account and/or Data Center. In most cases, selecting the Any options should be all you need.

**Detailed Instructions**

1. When Editing your Collection, you click "Add an Environment".
2. Provide an Environment Title and Infrastructure.
3. Add your Description.
4. In the "GitOps Pattern" field, select the pattern to use.

![gitops pattern field](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/gitops-pattern-select.png)

5. In the "Settings" section, update the following:
    1. "Account Pool" - Select "shared" for most cases. The shared pool uses our standard TechZone IBM Cloud Accounts for this Environment (i.e. ITZ Squad). If you select another Pool, you'll have different account options from there.

    ![account pool field](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/account-pool.png)

    2. "Cloud Account" - If using "shared" account pool, use the "Any" option unless you need a specific account to always be used. 

    ![account field](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/account-select.png)

    3. "Geo" - This should be "Any" unless this Environment option should only work in one of our Specific Geos. By selecting "Any" here, the user will be able to pick any of the 3 regions closest to them for deployment.

    ![geo field](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/geo-select.png)

    4. "Region" - This field should always be "Any" unless you need to select a specific Datacenter in the next field.
    5. "Datacenter" - Select "Any" unless you need this Environment to be only deployed to a specific Data Center.

    ![datacenter field](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/datacenter-select.png)

    6. Click the + button to add the entry.
6. In most cases the following entry "Account Pool: shared, Cloud Account: Any, Geo: Any, Region: Any, Datacenter: Any" should be all you need for most use cases. But if you need to customize this Environment to select specific locations, continue with step 5 again to add additional options until done.

![environment preferred](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/environment-preferred.png)

