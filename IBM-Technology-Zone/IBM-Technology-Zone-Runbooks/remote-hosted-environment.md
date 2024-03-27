# How to Create an Environment that Redirects to Another Portal(Power Systems, IBM z, and Storage Spectrum Environment)

Today there are multiple infrastructure portals that we are working with to consolidate to IBM Technology Zone. 

The following are all infrastructure options that will let you redirect to other portals as an environment catalog entry today.
- Power Systems
- IBM Z
- Storage/Spectrum
- VMWare Private Cloud TEC EMEA
- Hosted redirect.



## Catalog the environment

1. Edit your collection and find the 'Environment' section. Select **Add an environment**.

![Add environment](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/add%20environment.png)

2. Click the Infrastructure drop down field and select the option Power Systems, IBM Z, or Storage/Spectrum option.

![Select infrastructure drop down](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/select%20infrastructure%20drop%20down.png)

![Choose infrastructure](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/choose%20infrastructure.png)

**NOTE:** Choosing either of the three infrastructure options listed in this runbook will display the same fields: Title, Description, URL, Visibility, and Status.

![Create an environment form](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/Power%20environment%20form.png)

3. Provide a title and description for this environment. The title and description will display on the search environment tab. 

**NOTE:** It is a best practice to provide as much detail about the configuration of the environment as possible in the description. This will help the end user decide if this environment meets their specific use case need.

![example of environments search page](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/example%20environments%20search%20page%20description.png)

4. The URL field is the most important for this type of infrastructure environment entry on your collection.

If you are providing an environment that is catalogued in CECC or ISCEP, please navigate to the site and find the environment that you would like to catalog in IBM Technology Zone.

CECC Portal: https://www.ibm.com/it-infrastructure/services/cecc-portal/catalog

ISCEP Portal: https://www.ibm.com/it-infrastructure/services/client-experience-portal/

* For example: I would like to catalog a Power9 virtual server from the CECC portal as an environment on my collection in IBM Technology Zone. 

* Search for the environment catalogued on CECC portal.

![Power9 vs search](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/search%20power9%20vs.png)

* For purposes of my example, I will select the **IBM AIX** tile.

![AIX example](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/IBM%20AIX%20example.png)

* The URL, once on the reservation form for 'IBM AIX', is the important URL to copy from your browser.

AIX reservation URL: https://www.ibm.com/it-infrastructure/services/cecc-portal/details?pcode=8010100&imgCatId=4

![AIX url example](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/aix%20reservation%20url.png)

* Navigate back to your collection on IBM Technology Zone to paste the URL in the environment URL field. 

5. Select who should be able to view and have access to this environment: Business Partners, IBMers, or select both if applicable. 

6. Ensure that the Status field is set to enabled if you want this environment to display on your collection. You can come back and disable at any time. 

7. See the completed environment entry. This will be similar for Power Systems, IBM Z, and Storage/Spectrum environment entries. Select **Save** when you are done editing. 

![Finished environment entry](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/Finished%20environment%20entry.png)

**NOTE:** Feel free to add this environment to a journey at this time.

8. Navigate to the bottom of your collection form and select **Save** to save the whole collection of changes made. 

![Save collection](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/save%20the%20collection.png)

### Support

For any questions, contact DTE support.

Business Partners - Contact DTE Support - itz@us.ibm.com

IBMers - Make a post on the [#itz-techzone-support](https://ibm-itz.slack.com/archives/C0124J683GW) slack channel.








