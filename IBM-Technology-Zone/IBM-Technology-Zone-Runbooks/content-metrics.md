# Content Metrics

In this runbook, we will walk through the process for how a content author can access their to metrics regarding their content that they have contributed to IBM Technology Zone. 

_**Note:** This runbook is for IBMer use only._

## Table of Contents

### 1. Before Getting Started

- [General TechZone Content Definitions](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/content-metrics.md#general-techzone-content-definitions)

- [Content Metric Dashboard Definitions](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/content-metrics.md#content-metric-dashboard-definitions)

- [Main Dashboard Filters](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/content-metrics.md#content-metric-dashboard-definitions)

- [Additional Dashboard Filters](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/content-metrics.md#additional-dashboard-filters)

- [Digital Registry](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/content-metrics.md#digital-registry)

- [Getting Access](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/content-metrics.md#getting-access)

### 2. Reports

- [Page Views Report](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/content-metrics.md#page-views-report)

- [Collection Page View Report](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/content-metrics.md#collection-page-view-report)

- [Journey Page View Report](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/content-metrics.md#journey-page-view-report)

- [Click Events Report](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/content-metrics.md#click-events-report)

- [Journey Click Events Report](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/content-metrics.md#journey-click-events-report)

- [Resource Click Events Report](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/content-metrics.md#resource-click-events-report)

- [Reservations Report](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/content-metrics.md#reservations-report)

- [Collection Reservations Report](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/content-metrics.md#collection-reservations-report)

- [Environment Reservations Report](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/content-metrics.md#environment-reservations-report)

### 3. Troubleshooting

- [How to resolve error "We cant retrieve the data from the dataset csv?"](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/content-metrics.md#how-to-resolve-error-we-cant-retrieve-the-data-from-the-dataset-csv)

- [Why is my collection, journey, or resource name not showing in the Page Views or Click Events reports?](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/content-metrics.md#why-is-my-collection-journey-or-resource-name-not-showing-in-the-page-views-or-click-events-reports)

## Before Getting Started

This section will help get you started understanding the terminology of metrics that are captured for content and the filters that you can leverage today. Additionally, best practices to be aware of before loading the dashboard or while loading the dashboard to get the best performance. 

* Preferred browser for this content metrics dashboard that we recommend is Firefox. This browser option is the more performant browser than chrome at this time. 

* For your awareness: There are over 2 million page views, over 500K click events, and over 200K reservations captured today throughout the three reports that we are making available to you in this content metrics dashboard. Due to the volume of metrics that are captured on these reports, loading these reports can take up to 5 minutes.

* Best Practice is to clear filters before moving to another report. 

### General TechZone Content Definitions

Collection - A collection is a group of resources and environments all collected onto one page. A collection will generate a **pageview** metric every time a user navigates to your collection page.

Journey - A sequenced navigation implemented via tabs to better guide consumers through a collection into sections of resources or environments to reserve. A journey will generate a **click event** metric every time a user clicks on a journey tab. Additionally, journeys can generate a page view metric if the URL to the journey was shared with them directly. 

Resource - A resource is a discrete piece of content in a collection to accompany a environment. Resource types can include today, a video showing how to do a demo, a hands-on lab walking through step by step how to do the demo, architecture diagrams, and more. A resource will generate a **click event** metric every time a user clicks on a resource. 

Environment - An environment is a running infrastructure that can include pre-installed applications and services to interact with. An environment will generate a **reservation** metric every time a user reserves the environment successfully. 

* NOTE: If the environment failes, a metric will not be captured.  

![collection metrics all](https://github.ibm.com/dte-support/private/blob/master/New-Runbooks/images/collection-metrics-all.png)

### Content Metric Dashboard Definitions

This section will help you understand all the terminology used for sections and filters used on the content metric dashboard.

Pageview - An instance of a user visiting a particular page on a website. Pageviews metrics are captured today for every collection page.

Click event - An element receives a click event when a pointing device button (such as a mouse's primary mouse button) is both pressed and released while the pointer is located inside the element. Click events metrics are captured today for Journey tabs and Resource tiles on a collection. 

* NOTE: Total clicks - Represents total click events captured. Leverage the main filters to dive into the click event totals for your specific collection from the Click Events report. 

Unique users - Unique visitors refers to the number of distinct individuals visting your collection during the selected time frame selected. 

* NOTE: Adding up unqique users month on month will never add up to the total unique user count that displays for the entire year. Unique users, depending on the time frame that you are selecting will show the unique users during that time frame. If you select one month, you will see the total unique users that month. If you select unique users for all of 2023, the user that you counted individually in one particular month might have revisted in another month in that year. 

Persona - The persona of the user visiting your collection. Options include: IBMer, Business Partner, and User. 

* NOTE: User persona could be an IBMer or Business Partner that we legally cannot capture their persona based on their personal user cookie preferences.


### Main Dashboard Filters

There are three main filters that can be applied to each report. Find definitions of each below with guidance on how to find the informatoin to effectivly filter your content metrics.

* **NOTE** - Due to each report tab (Page views, Click Events, and Reservations) pulling from different data sources, leveraging these filters will have to be used one at a time. For example: When on the Page Views report tab, selecting a collection ID filter will not carry over if you then move to the Click Events report. This is a different data set so the filter will have to be reapplied. We simply provide these main filters at the top of all reports since there is a requirement to filter all reports by these three main data points. It is a best practice to remove the filter before navigating to the new report tab or by simply refreshing the page when you want to start over on a fresh report tab.

Collection name - Can be found as the first title on a collection page. For example: This collection name is '[Model Home]( Unique visitors refers to the number of distinct individuals visting your collection during the selected time frame selected.)'. 

Collection ID - Can be found by selecting edit as the owner or collaborator of the collection from your collection page, then find the ID in the address bar of your browser. 

* Here is an example of the URL from this edit page: https://techzone.ibm.com/collection/63bc8e0f9617a20018c02f2d.

* Here is an example of the collection ID that you need to leverage the collection ID filter: 63bc8e0f9617a20018c02f2d

Persona - The persona of the user visiting your collection. Options include: IBMer, Business Partner, or User. 

* NOTE: User persona can be an IBMer or Business Partner that we legally can not capture their persona based on their personal cookie preferences. 

GEO - The geo of the user visiting your collection. Options include: Americas, APAC, EMEA, Japan, or not-captured. 

* NOTE: not-captured is similar to user persona note above. This user can not be tracked based on their personal cookie preferences. Additionally, this GEO metrics is not a filterable option on the "Reservations" report tab. Only from the Click Events and Page Views Reports.

![main dashboard filters](https://github.ibm.com/dte-support/private/blob/master/New-Runbooks/images/w_GEO_metrics.png)

### Additional Dashboard Filters

The content metrics dashboard allows for additional filtering beyond the main filters provided in the top section of each report. Please read this section to understand additional filters that you set to drive additional data insights.

Filter by Year - Select the year directly on the report to show metrics for the entire year to date. Notice that the totals for page views, unique users, or click events for example will update based on the year that you selected.

Filter by Month - Select a specific month on the report to show metrics for that specific month. Notice that the totals for page views, unique users, or click events for example will update based on the specific month that you selected.

NEW - As of November 2023, Page View reports are broken out by 2022 report tab and a 2023 tab. This change was done to improve performance due to the high volume of page view events captured per year. To filter by page view metrics on 2022, select the 2022 Page Views report tab. To filter by 2023 Page Views, select the 2023 Page Views report tab. 

![additional filters](https://github.ibm.com/dte-support/private/blob/master/New-Runbooks/images/additional-filters.png)


### Digital Registry

IBM Technology Zone leverages Segment for page view and click event metrics. Every collection URL and Journey URL must be submitted to Digitial Registry in order to enable tracking through Segment. If you have just created a new collection or journey, please wait up to two weeks for our team to manually batch upload all new the URLs into Digital Registry to enable tracking of pageviews and click events. We appreciate your patience while we do a batch upload.


### Getting Access

As of now, access is provided for IBMers directly on the Help page. We can not provide the link directly on this runbook as it should only be shared and accessible to IBMers at this time. 

![help metrics](https://github.ibm.com/dte-support/private/blob/master/New-Runbooks/images/help-content-metrics.png)

## Reports

### Page Views Report

To get started reporting on page views for your collection page, select the 2022 Page Views report tab or the 2023 Page Views report tab. By default opening up either of these reports will display metrics for all IBM Technology Zone collection page views for that reports year. 

![page views report](https://github.ibm.com/dte-support/private/blob/master/New-Runbooks/images/pageviews_reports_yearly.png)


### Collection Page View Report

This report can be found from the "2022 Page Views" or "2023 Page Views" report tab.

To see your specific collections page view metrics, navigate to the collection ID or collection name filter in the top right hand banner of this page to find your collection. Once the collection name or collection ID filter is applied, the Total Page Views count and Unique Users count will be updated to show the metrics associated for your collection. Additionally the Journey Name section will be updated automatically to pull in the journeys that you have associated with this collection.

* NOTE: Need help finding your collection ID or collection name, scroll back up to the getting started section of this runbook to learn about the terminology and how to find the information we are requesting in these filters. 

### **Journey Page View Report**

This report can be found from the "Page Views" report tab.

Once you have applied your collection filter to see overall collection page view metrics, select the specific Journey Name from the Journey Name section to further filter on Journey page views. Once you select the Journey name in the list, the total page view count and unique user count will be updated to show the metrics associated to the specific journey you have selected. 

Find the collection ID filter in the top right hand banner to display collection page view metrics as shown in screenshot below. Then select the Journey name to further filter on page views by journey on the collection initially filtered. 

![journey page views report](https://github.ibm.com/dte-support/private/blob/master/New-Runbooks/images/journey-pageviews-report.png)


### Click Events Report

To get started reporting on click events associated with the Journeys and Resources on your collection page, select the Clieck Events report tab. By default opening up this report will display metrics for all IBM Technology Zone collection page click events. 

![click events report](https://github.ibm.com/dte-support/private/blob/master/New-Runbooks/images/click-events-report.png)

### **Journey Click Events Report**

This report can be found from the "Click Events" report tab.

To see your specific Journey click events associated to your collection page, navigate to the collection ID or collection name filter in the top right hand banner of this page to find your collection. Once the collection name or collection ID filter is applied, the Total Clicks count and Unique Users count will be updated to show the click event metrics associated with your collection. Additionally the Journey Name section will be updated automatically to pull in the journeys names associated with this collection.

Find the collection ID filter in the top right hand banner to display collection specific click event metrics as shown in screenshot below. Then select the Journey name to further filter on the click events associated with the specific journey selected.

![journey click events](https://github.ibm.com/dte-support/private/blob/master/New-Runbooks/images/journey-click-events-report.png)

* NOTE: Fewer clicks on Journeys compared to Journey page views might indicate users are being shared the URL directly and not clicking the Journey tab on the collection page. 

### **Resource Click Events Report**

This report will be made available from the "Click Events" report tab.

To see specific resource click events associated to your collection page, navigate to the collection ID or collection name filter in the top right hand banner of the metrics report page. Once the collection name or collection ID filter is applied, then you can choose to filter by Journey or go straight to the resource section (scroll down the page in the report) to filter by Resource name. Filtering by resource name will update the metrics dashboard to show you the Resource click events associated with this collection. 

![resource click events report](https://github.ibm.com/dte-support/private/blob/master/New-Runbooks/images/resourceclicksreport.png)

### Reservations Report

To get started reporting on reservations associated with the environments on your collection page, select the Reservations report tab. By default opening up this report will display metrics for all IBM Technology Zone reservations. 

![reservations report](https://github.ibm.com/dte-support/private/blob/master/New-Runbooks/images/reservations-report.png)

### **Collection Reservations Report** 

This report can be found from the "Reservations" report tab.

To see all reservations associated with your the environments on your collection, filter by collection ID or collection name to start. Once this filter is applied all reservations associated with environments on your collection will be applied.

### **Environment Reservations Report**

This report can be found from the "Reservations" report tab.

To see all reservations made on a specific environment on your collection, filter by collection ID or collection name to start. Once this filter is applied, further select the environment name from the list that you would like to see reservations for a specific environment. 

![environment reservations report](https://github.ibm.com/dte-support/private/blob/master/New-Runbooks/images/environment-reservations-report.png)

## Troubleshooting Guide

This section is to provide guidance to troubleshoot why certain metrics are not showing up in the dashboard as you would expect. 

### How to resolve error "We cant retrieve the data from the dataset csv."?

![metrics-datacsv-error](images/metrics-datacsv-error.png)

* We recommend Firefox as the preferred browser so if you are not using this browser please switch

* Refresh the page

* Clear history and cache

* Open the content metrics dashboard in an incognito window on Firefox browser

* If the issue persists, please log a support case with TechZone support.

### Why is my collection, journey, or resource name not showing in the Page Views or Click Events reports?

* Reminder: If you just created the Collection or the individual Journey tab, then please allow up to two weeks for the IBM Technology Zone team to do the batch upload of URLs to Digital Registry. We appreciate your patience as this is a manual process today with Digital Registry. 

If your collection or journey has been published and the resource was made available on the collection or Journey page for more than two weeks, follow these steps to further troubleshoot:

* Navigate to [Digital Registry](https://digitalregistry.wdc1a.cirrus.ibm.com/#about/overview) site to check that the URL has been submitted. Digitial Registry site is an IBMer ONLY accessible.

* Navigate to the [Explore URLs](https://digitalregistry.wdc1a.cirrus.ibm.com/#explore_urls/check_urls) tab and enter the full URL of the collection URL or specific journey URL into the **Paste URLS here, one per line:** field. Then click the 'Submit' button.

![digital registry url check](https://github.ibm.com/dte-support/private/blob/master/New-Runbooks/images/digital-registry-url-check.png)

* If results display below the Submit button with the URL that you entered and the Site ID IBM_DTE, then your URL has been successfully added to Digital Registry. Open a Support case with the IBM Technology Zone team to further investigate why metrics are not displaying correctly on the Content Metrics Dashboard. 

* If results do not display then this URL must be submitted to Digital Registry and metrics will not be captured until it has been submitted. Open a Support case with the IBM Technology Zone team and provide the collection URL and/or the journey URL to be submitted to Digital Registry. Please allow up to one week as this is a manual process to submit URLs to Digital Registry. 


## ADMIN - Support team

Users that open a support case providing a collection URL or journey URL to be added to digital registry, open a git issue in the support escalation repostiory and assign label "Metrics Squad" and assign Siah. 

Follow up with the user that the request has been sent to our metrics owner and that we will notify them when the URL has been added. Please allow up to 5 business days for a URL to be submitted as this is a manual process to upload URLs to Digital Registry. 

If content owners are asking for the URL to the content metrics dashboard, ensure they are an IBMer and then share the following link with this runbook. 

IBMer ONLY Content Metrics Dashboard URL - https://ibm.biz/itz-content-metrics

Another option is to navigate them to the support page as described above in this runbook on how to get access. 
