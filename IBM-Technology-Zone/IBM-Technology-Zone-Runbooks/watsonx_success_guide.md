<h1 align="center">The watsonx Workshop Success Guide for Instructors</h1>


## Summary
This guide contains suggestions and ideas on how to run a successful workshop using Techzone's watsonx offerings. Please note that the outlined are ideas and suggestions based on instructor feedback and the team's recommendations, take into consideration the purpose and the content of the workshop while reviewing this. This guide is different from the [watsonx Troubleshooting Guide](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#watsonx-troubleshooting-guide) as it outlines possible workflows for a workshop delivery, rather than known issues.


## Table of Contents


### Determining the environment for the workshop
  * [How do I tell if an environment is available for a workshop?]()

  * [What environment should I use if my workshop is internal/with IBMers?]()

  * [What environment should I use if my workshop is external/with partners/clients?]()

  * [How do I make a workshop request?]()

  * [What region should my workshop be hosted in?]()

  * [What plans would the services under my environment be?]()


### Ensuring success during the workshop
              
   * [Will the instructor be able to access the student environments?]()

   * [Suggestions for workshop students who are not IBMers]()

   * [How can I get help during my workshop?]()

   * [What additional resources can I provide to my students for troubleshooting and help?]()


[Back to Top](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#watsonx-troubleshooting-guide)


## Determining the environment for the workshop


### How do I tell if an environment is available for a workshop?
The environments available for workshops are visible upon selecting a tile to make a reservation, they include an extra option to schedule a workshop/request multiple environments when completing the reservation form. An example of that is attached below:
![watsonx-workshop](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watsonx-workshop.png)
**It is recommended to reserve the environment as a single instance prior to the workshop to ensure that the expected capabilities are available as part of the research stage for your workshop to avoid issues during the live stage of the delivery. Most watsonx environments are available for reservation for Education purposes.**


### What environment should I use if my workshop is internal/with IBMers?
There are several elements that would need to be taken into consideration when planning an internal workshop with IBMers. Depending on the contents neeeded for the workshop there are common environments used for standard workshop delivery. These environments are listed inder the watsonx section of the [certified base images collection](https://techzone.ibm.com/collection/tech-zone-certified-base-images/journey-watsonx). Often, the environments requiring access via IBM Cloud also need an active IBM ID, therefore they would be better suited towards users who are existing IBMers or have an IBM ID.


Additionaly, there are common popular collections that have been contributed by recognised authors offering this option too. These offerings also leverage the need for an existing IBM ID. Ensure you have searched through Techzone using the search option to cover everything available on the Technology Zone platform. If the workshop carried out does not require an isolated ID and can be associated with an IBM ID, we recommend reserving the regular IBM ID environments. This means that once the workshop has started, the students will be required to use their own IBM ID and will receive a cloud account invite for their dedicated environment upon signing up using the student link.

The following diagram can also be used to determine the more suitable environment:
![diagram-watsonx-workshop](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/diagram-flow-workshops-watsonx.png)

Here is a list of popular and featured watsonx-related collections used by IBMers and patners:
* [IBM watsonx Code Assistant for Z](https://techzone.ibm.com/collection/653fee8bf2cbbb0017e126de)
* [Customer Care Technology Pattern](https://techzone.ibm.com/collection/643873efb9514600170ce650)
* [IBM watsonx Assistant for Z](https://techzone.ibm.com/collection/6633e75d979046001eea2b77)
* [Watson Applications](https://techzone.ibm.com/collection/6633e75d979046001eea2b77)


### What environment should I use if my workshop is external/with partners/clients?
Fpr users that do not have an existing IBM ID it is worth considering the use of our **Student ID environments**. The difference between the IBM ID and Student environments is outlined in [this runbook](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#what-is-student-id-environment). These environments offer a separate login option with an isolated IBM ID. Alternatively, the option of requesting the students to sign up for an IBM ID from [here](https://www.ibm.com/account/reg/us-en/signup?formid=urx-19776) works well too. 


Several offerings for Student ID are currently available in the [watsonx journery of certified base images collection](https://techzone.ibm.com/collection/tech-zone-certified-base-images/journey-watsonx). Advance testing is recommended to ensure that the available content options contain the necessesary services for the purposes of the workshop. An additional benefit to the isolated ID is that the instructor would also be able to access the student environments and could leverage multiple students/a team per environment as all the needed credentials are outputted in the details of the environment.


### How do I make a workshop request?
The steps required to make a workshop request are outlined in [this existing runbook](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/How-to-schedule-a-hosted-workshop.md). You can also review the duration policies and advance notice for wokrshops in [the duration policies runbook](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/reservation-duration-policy.md#workshop-manager-policies).


### What region should my workshop be hosted in?
Determining the region for the workshop can be decided based on the services/models/functionalities needed of the SaaS offerings and their availability in the general reservation form. This can be tested in advance by attempting a singular reservation of the particular environment, the same list of regions will appear in the workshop request too. Additionaly, an important factor is to review the IBM Cloud documentation and ensure where the specific service is available and in what region the desired capability is present. Regional availability for watsonx SaaS services and features on IBM Cloud can be found listed in [here](https://www.ibm.com/docs/en/watsonx/saas?topic=integrations-regional-availability-cloud).


### What plans would the services under my environment be?
Techzone Certified watsonx environments do not have token limitations and are under the paid plan offerings, however to ensure the exact plans under each service please review the tile of the environment for further details. Additionaly, you can reserve a test environment and review under the details under the resource list. Ensure when making the reservation to select the correct desired options as several reservations contain different options for including additonal services like DB2 or an option to select dedicated/shared service.


* [wastonx.data instance limits for engines and services](https://cloud.ibm.com/docs/watsonxdata?topic=watsonxdata-wxd_clust_limits)
* [Watson Machine Learning plans and compute usage](https://dataplatform.cloud.ibm.com/docs/content/wsj/getting-started/wml-plans.html?context=wx)
* [watsonx.governance offering plan options](https://dataplatform.cloud.ibm.com/docs/content/wsj/model/wos-plan-options.html?locale=ru&context=cpdaas)


NB: Users would not have the ability to create and add aditional services. **Any services created by the user would be under the free limited plan and will run out.**


## Ensuring success during the workshop


### Will the instructor be able to access the student environments?
If the selected option for the workshop is via an IBM ID environmet the instructor would not have direct access to the student environments, apart from the details of the specific environment. However, with the Student ID environment the instrictor would be able to log in and review these environments in advance since all the login information would be included in the reservation details. 

### Suggestions for workshop students who are not IBMers
It is recommended to have the participants of the workshop to create IBM ID to avoid issues with Cloud Account Invites and access permissions. Creating an IBM ID is free and can be done through [here](https://www.ibm.com/account/reg/us-en/signup?formid=urx-19776). Note that, creating and IBM ID is different from creating an IBM Cloud Account, do not create an IBM Cloud for each participant as that would require billing information.


If the participants are not known in advance and they are unable to create IBM IDs, for best results consider the use of the Student ID environments to avoid any issues related to onboarding users to IBM ID and getting access to the workshop environment.

### How can I get help during my workshop?
Live workshop issues can be reported to our support team as Severity 1. Please contact Techzone Support using this form to get assistance with provisioning issues and environment access issues. If the issue is specific to only a few environments include their numbers and replication steps for the issue with any error message present. The Support team will work accordingly to address the issue, ensure the workshop ID or URL is included in the support ticket for faster resolution of the problem.


### What additional resources can I provide to my students for troubleshooting and help?
The [watsonx Troubleshooting Guide](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#watsonx-troubleshooting-guide) contains list of known bugs and limitations that the team has received feedback on from common support cases and various users. This guide can be used to provide self-service and help during a live ongoing workshop.

