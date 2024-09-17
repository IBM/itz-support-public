Question #1: Where can I find the VM login credentials?
Answer #1: VM credentials can be found by clicking the “keys” symbol on the VM. See "viewing saved credentials " some Demo assets have their VM credentials stored in lab guides and documentation provided.

Question #2: How do I reserve an environment?
Answer #2: We suggest you leverage the [Onboarding Collection](https://techzone.ibm.com/collection/onboarding) as there is a great self-help video outlining how to search and reserve an environment.

Question #3: How can I engage with the support team as an IBMer?
Answer #3: **IBMers** can log any issues or feedback via [Open a case](https://ibmsf.force.com/ibminternalproducts/s/createrecord/NewCase?language=en_US) or Email: [techzone.help@ibm.com](mailto:techzone.help@ibm.com) and the support team will address them according to our SLAs. If you have a requirement or enhancement request please log via the [IBM Technology Zone Enhancements](https://itz-enhancements.ideas.aha.io/portal_session/new) (accessible by IBMers only).

**Business Partners** should use [techzone.help@ibm.com](mailto:techzone.help@ibm.com) for all of their support requirements.

Question #4: Is there a roadmap that outlines future IBM Technology Zone program offerings?
Answer #4: Yes, you can leverage the IBM Technology Zone [roadmap](https://bigblue.aha.io/published/d35467795d322d4214378f1d168508f1?page=2) to view planned implementations for the remainder of 2021.

Question #5: Why can’t I see my cluster in IBM Cloud web dashboard?
Answer #5: Sometimes users can not see their clusters in IBM Cloud web dashboard, so before leveraging support, run the following commands:

1.  Log in IBM Cloud via CLI: `ibmcloud login --sso`
2.  Select the account with this problem.
3.  Switch to `itzroks` resource group: `ibmcloud target -g itzroks`
4.  List clusters: `ibmcloud ks cluster ls`

Now you should be able to see your cluster in the CLI and Web.

Follow the instructions in this [runbook](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/iam-fix.md) to see your cluster in CLI and Web.

For any questions, contact ITZ support.

*   Business Partners - Contact ITZ Support - [techzone.help@ibm.com](mailto:techzone.help@ibm.com)
*   IBMers - Make a post on [Open a case](https://ibmsf.force.com/ibminternalproducts/s/createrecord/NewCase?language=en_US) or Email: [techzone.help@ibm.com](mailto:techzone.help@ibm.com)

Question #6: How can I improve performance of my environment?
Answer #6: You can improve performance during Secure Remote Access (SRA) browser client session by

*   Using Google Chrome
*   Changing the display quality settings in the browser client toolbar
*   Reducing other connections that may be consuming bandwidth
*   Trying to improve your network connection.

See "Improving performance during a browser client session " for additional details

Question #7: What is a collection?
Answer #7: A collection is a group of related resources. It may include multiple collections and is owned by the contributor.

View [Introduction to Collections](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/techzone-content.md#introduction-to-collections----what-is-a-collection) runbook to learn more.

Question #8: How long can I reserve an environment for?
Answer #8: View [How Long Can I Reserve an Environment](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/reservation-duration-policy.md) runbook to know more about the specific duration of reservation of specific infrastructures.

Question #9: Is there an API I can leverage for my upload of content?
Answer #9: Yes. You can access the API swagger documentation here [https://api.techzone.ibm.com/swagger/](https://api.techzone.ibm.com/swagger/).

Most API interactions will require an API token. Your API token is tied to your current SSO session and it can be acquired from the [/my/profile](/my/profile) page.

Question #10: How do I know what permissions I have as an IBMer?
Answer #10: All IBMers have default permission to create a collection and view technical content on the site.

Question #11: Why don’t all my environments show up at once?
Answer #11: Often the workload of these templates is rather large. Workshop Manager staggers the deployment of these environments so that by the time you’ve reached the start time that you requested, you will have the number of environments that you requested.

Question #12: What is the difference between Bronze, Silver, Gold and Platinum Content?
Answer #12: Tiles are branded as Bronze, Silver, Gold or Platinum to differentiate content based on different quality standards. As you level-up, so does the quality of the content. **NOTE:** Bronze, Silver, and Gold allocations are part of the crowdsourcing model and can be allocated by the contributor with the below standards as guidance. Platinum content is currently only provided by Bob Kalka’s Product Squads and Eddie Daghelian’s Activation Kit teams. **_We are opening up the ability for crowdsourced content to become Platinum in September._**

**Bronze** - Buyer Beware (may not be current and/or supported), grouped resources facilitating experiential activity, may be IBMer only

**Silver** - Buyer Beware (shared ‘as is’ without any testing or vetting), author supported (best effort to respond), use case driven, may have a reservable environment, may have a defined journey, should be Business Partner accessible

**Gold** - Author or community supported (24 hours to acknowledge), guided demo script, FAQ and/or troubleshooting guide, reservable environment, defined journey, community reviewed & tested, must be Business Partner accessible

**Platinum** - Community supported via Slack (same day acknowledgement), lead-with or growth offering, IBM Cloud reservable environment, utilizes most recent version release, technical review & sign off by a product squad member, reviewed & updated every 30 days, approved by Technical Sales brand executive

Question #13: I got an IBM ID Sign in Error, can anyone help?
Answer #13: **Check to see if there is an IBMid outage:**

1.  Refer to the IBMid status page: [https://w3.ibm.com/w3publisher/ibmid-home/ibmid-service-status](https://w3.ibm.com/w3publisher/ibmid-home/ibmid-service-status)
2.  Additionally see the IBMid outage history page: [https://w3.ibm.com/w3publisher/ibmid-home/ibmid-outages-history](https://w3.ibm.com/w3publisher/ibmid-home/ibmid-outages-history)
3.  If there is an outage, create a ticket from the IBMid support page: [https://w3.ibm.com/help/#/article/ibmid/support?requestedTopicId=support](https://w3.ibm.com/help/#/article/ibmid/support?requestedTopicId=support)

**If you are still having issues signing in, c\*\*\*\*ontact the IBMid helpdesk for support:** [https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html](https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html)

Additional resource for IBMers to contact IBMid support team on slack: [https://ibm-cio.slack.com/archives/C0MBSS9SA](https://ibm-cio.slack.com/archives/C0MBSS9SA)

Question #14: How do I find collection resources related to an environment reservation?
Answer #14: There are three easy ways to navigate to an environments collection of resources:

1.  Finding collection of resources before reserving by navigating to the environment tab.
2.  Finding collection of resources when filling out reservation form by selecting "Related Collection" in the top right banner.
3.  Finding collection of resources after you have already reserved the environment by navigating to "My Reservations" page and clicking on the ellipsis of the reservation card and click "View Collection"

View the following runbook [Find collection resources related to an environment reservation](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/reservation-collection-linkage.md) for step-by-step instructions.

Question #15: Where can I find the existing GitOps patterns?
Answer #15: All IBMers can access our existing gitOps patterns [here](https://github.ibm.com/dte2-0/ccp-gitops-patterns).

Question #16: Who can create content on IBM Technology Zone?
Answer #16: IBMers & Business Partners can contribute content.

IBMers - Get started by visiting our [IBM Technology Zone Onboarding](https://techzone.ibm.com/collection/onboarding) page for helpful how-to videos and guidance.

Business Partners - Review the [Business Partner Contribution Terms and Conditions](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/bp-contribution-agreement.md) and contact the appropriate [Platinum squad leader](https://ibm.box.com/v/squad-leader) to start collaborating today.

Question #17: I have an opportunity code, but I did not capture it on the initial reservation form. How do I get an extension?
Answer #17: Send an email to [techzone.help@ibm.com](mailto:techzone.help@ibm.com) with the opportunity code and the name of the environment that you reserved and need the extension on.

Question #18: Where can I go to get support for an environment?
Answer #18: If the issue pertains to your particular environment, i.e., a particular program or command not working, then reach out directly to the content owner using the help icon located at the top of the IBM Technology Zone asset page. Whether IBMer or Business Partner, please contact us at [techzone.help@ibm.com](mailto:techzone.help@ibm.com) so that we can connect you to the correct individual for support.

Question #19: What are the IBM Technology Zone Programs?
Answer #19: The IBM Technology Zone has 2 programs currently: Branding Program and Rewards Program. The goal of these programs is to help distinguish, incent, and reward site contribution, consumption, and curation of best-of-breed content. You can find out more about these programs from the onboarding collection or going directly to this [link](https://ibm.box.com/s/5oc5vww7j5pf9w9r7e5tgvsrcev7t7x6).

Question #20: Can you use Workshop Manager to run a workshop for a client?
Answer #20: You can reserve multiple environments for internal or external workshop opportunity. External meaning for a  customer engagement. All we ask on the workshop request form is for the opportunity code and customer names associated with this request so that we can prioritize capacity accordingly. All customer will need to have an IBMid to access the student page once the workshop has been scheduled. The student page will allow customers to see the environment they are assigned to and other workshop details, like start date, end date, and description of the workshop.

Question #21: How do I extend my reservation?
Answer #21: Here are the simple steps to extend your reservation:

1.  Locate ‘My library’ on the top of the page > Click ‘My reservations’ in the dropdown options.
2.  Locate the reservation you want to extend and click on the 3 dots > Click 'Extend’.
3.  Select new date and time and click extend (Maximum extension: One week)

View [How To Extend Your Reservation](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/extend-a-reservation.md) runbook for screenshots of the step-by-step instructions.

If the “Extend” option is not available from the reservation tile options, you did not provide an opportunity number on the reservation. Edit your reservation to include a valid opportunity number.

For questions about the environment or support, reach out to the author of the collection.

Question #22: How do I fix an internal server error?
Answer #22: **Cause:** VMware on IBM Cloud-associated template has been retired or deleted.

**Resolution:** Verify the status of the resource/collection with ITZ Support.

Business Partners - Contact ITZ Support - [techzone.help@ibm.com](mailto:techzone.help@ibm.com)

IBMers - Make a post on the [Open a case](https://ibmsf.force.com/ibminternalproducts/s/createrecord/NewCase?language=en_US) or Email: [techzone.help@ibm.com](mailto:techzone.help@ibm.com)

View our [Internal Server Error](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Internal-server-error.md) runbook to double-check that the error message you are seeing corresponds to the one in our runbook.

Question #23: How can I benefit from leveraging the IBM Technology Zone?
Answer #23: *   **Option 1:** You can **build** your own demo using our hosted environments.
*   **Option 2:** You can engage in a conversation with your customer in the discovery phase ("show" them vs. "tell" them).
*   **Option 3:** You can **share** the newly created demo for others to leverage and earn points towards big rewards!

Question #24: How do I give feedback on a collection?
Answer #24: 1.  Use the star ratings option found at the top of each page to rate the collection.
2.  Add a comment at the bottom of the page for others reviewing this content to see.
3.  Email the Content Author directly by using the help icon at the top of the page.

Question #25: How can I request content to be added to a Platinum collection?
Answer #25: To request a demo be added to an existing Live Demos Platinum collection:

1.  Ensure your demo collection or resource(s) meet [Platinum standards](https://ibm.box.com/s/rw6lxuoor1q2vvrdy3r194a96bhwjt6u).
2.  Review the available Live Demo Collections to see if your resource and/or collection would help make that collection more robust.
3.  If yes, select the appropriate [Product Squad Leader](https://ibm.box.com/v/brand-squad-leads).
4.  Send the Product Squad leader an email with your request to add content to their Platinum collection.
5.  If approved, the Product Squad Leader will work with you to add your content to their Platinum collection.
6.  The Product Squad Leader will make you a Collaborator of that collection so that you can manage and maintain your resources. Your name will also show on the Live Demos Collection as a Collaborator.

Question #26: I found broken links in a collection. How do I get them fixed?
Answer #26: Use the Ask for Help icon at the top of the page and post your concerns. This will be directed to the Content Owner directly or a community monitored Slack channel for action. If you do not receive any response, you can try contacting the Collaborators listed on the page or escalate to the Content Owners Blue Pages manager.

Question #27: Where can I get help for “Content”, “Application” relating to my environments requested through Workshop Manager?
Answer #27: Reach out to the Content Author on IBM Technology for all inquiries related to the content, product, and application.

Question #28: How far in advance should I submit a Custom/ new VM template request?
Answer #28: If you need to go this route, do so well in advance of your workshop. We suggest at least 2 weeks out.

Question #29: How do I extend my workshop reservation?
Answer #29: For IBMers Make use of [Open a case](https://ibmsf.force.com/ibminternalproducts/s/createrecord/NewCase?language=en_US), for Business Partner Email: [techzone.help@ibm.com](mailto:techzone.help@ibm.com)to request extensions. When making an extension request please provide the following information

1.) Opportunity number 2.) Presale or postsale 3.) Your role (techsales, CSM, etc).

Note: extensions are granted based on resource availability and should be requested before the scheduled end date/time. Expired workshops cannot be extended.

Question #30: What opportunities are valid when making a reservation?
Answer #30: Sales Cloud, Atlas, ESA, and soon to be Gainsite relationship IDs in Q3 2021.

Question #31: What infrastructure does Workshop Manager support?
Answer #31: VMware, Hosted, and IBM Cloud environments today are an option to reserve multiple of for a workshop setting. If you have a workshop and need another template on another infrastructure, please fill out the custom request form with the dates that you need the environments for and how many. Our team will review the request based on capacity and budget to support this request and upon an approval can put aside capacity for your environments for your upcoming workshop. Please start with this [custom request form](https://ibm.biz/dte-environment-requests).

Question #32: I couldn’t get the requested template, can anyone help?
Answer #32: **Cause:** VMware on IBM Cloud associated template has been retired or deleted

**Resolution:** Verify the status of the environment with ITZ Support

Business Partners - Contact ITZ Support - [techzone.help@ibm.com](mailto:techzone.help@ibm.com)

IBMers - Can [Open a case](https://ibmsf.force.com/ibminternalproducts/s/createrecord/NewCase?language=en_US) or Email: [techzone.help@ibm.com](mailto:techzone.help@ibm.com)

Question #33: Is experience required to create an entry with GitOps? Terraform?
Answer #33: Having experience using GitOps or Terraform experience is **not required** to add environments to collections. This is only required if you need new patterns that don’t currently exist.

Question #34: When trying to submit the workshop request form I get this error: “Error submitting Form”. What should I do?
Answer #34: There are two common reasons why this error is showing:

*   Duplicate title – If you or someone else has already used the very same title of your workshop before, then the form will not submit. Add a unique identifier to your title (perhaps date, customer, etc.) to resolve this.
*   Not logged in - Make sure you are logged into the IBM Demos site. Try adding /logout to the end of the URL and log back in.

If none of these resolve the issue, IBMers should open a [Open a case](mailto:Open%20a%20case), and Business Partners can report the issue using Email: [techzone.help@ibm.com](mailto:techzone.help@ibm.com)  for support.

Question #35: How long can I request a workshop for?
Answer #35: The maximum durations for requesting multiple environments is 5 days. Some durations are shorter depending on the template size and resource availability.

Question #36: What cost do I pay to get access to the environments on IBM Technology Zone?
Answer #36: IBM Technology Zone team bears all the costs of the environments you reserve on the site. All we ask is that you provide the valid opportunity code when filling out the reservation form so that we can show the impact of engagements that these environments are being used for. Soon 3rd party cloud environments will have an additional approval step for GEO market leader approval. This will free up capacity of 3rd party cloud environments for only top priority client opportunities. If you have additional questions please contact: [brooke.jones@ibm.com](mailto:brooke.jones@ibm.com)

Question #37: What languages does IBM Technology Zone support?
Answer #37: *   English
*   Spanish
*   Portuguese
*   Japanese
*   German
*   French
*   Chinese
*   Korean

Question #38: Is there a mandated time to respond to content support inquiries?
Answer #38: Content Contributors are responsible for supporting and maintaining their assets in the portal. There is no mandated timeline for response. If you have not received a response within an acceptable timeframe, it is suggested that you escalate your concerns to their Blue Pages manager.

The portal is supported via a community moderated Slack channel where Subject Matter Experts (SMEs) are mandated to respond in a timely manner. The [Service Level Agreements](https://ibm.box.com/v/dte-support-slas) for support can be found under the Help page menu.

Question #39: How soon in advance should I make a Workshop request?
Answer #39: All workshop request needs to come in at least 7 days before the required start date and time.

Question #40: Does bandwidth and latency affect performance?
Answer #40: Yes, bandwidth and latency do affect performance. Run a quick "[Speed test now](http://speedtest.skytap.com/)" and learn about the results of your speed test by reviewing "[My VMs are running slow](https://ibm.box.com/s/38llr9rdxijhhloxc8hbv444uu2rdst5).” section for additional details.

Question #41: How does the Student get their environment?
Answer #41: Students make use of the student url sent to them by their instructor. They will need to enter their IBM ID (email) to claim an environment. Note: Instructors receive the “Student url” via email or can view it using the instructor url.

Question #42: Why was my workshop environment shutdown?
Answer #42: Environments are set to shut down when idle for 180 mins/3hours. This can only be selected when making a request

Question #43: When can we expect enhancement requests to be reviewed and implemented?
Answer #43: Enhancements requests submitted through our [IBM Technology Zone Enhancements](https://itz-enhancements.ideas.aha.io/portal_session/new) are reviewed weekly. Depending on the request and difficulty will depend on turnaround time. Our team will be putting an enhancements roadmap together in Q3 so that idea submitters can see when we plan to implement their request on the site. If you have questions about the process or want a status update on an idea you submitted, please contact [brooke.jones@ibm.com](mailto:brooke.jones@ibm.com).

Question #44: How can I get access to an environment and its related content?
Answer #44: From the **Environments** tab located in the top navigation bar, utilize the search to filter options that match your environment criteria. To see related content, select the title of the collection under the **Collection** column. This will take you to the content page where the environment and all related resources reside. If no additional resources are provided, you can use the **Ask for Help** icon at the top of the page to request further assistance from the Content Author.

Question #45: What is a resource?
Answer #45: A resource is a discrete piece of content used in a collection. A collection is made up of multiple resources.

Question #46: What is the difference between an Activation Kit and a TechDemos collection?
Answer #46: Activation Kits are collections with a journey not limited to lead-with or growth offerings and are owned by the Contributor. TechDemos are collections with a journey that are aligned to lead-with or growth offerings and are owned by Product Squad leaders who have role-based privileges to create Platinum collections.

Question #47: Who do I contact if something is broken on the site?
Answer #47: You should initially check the [System Status site](https://w3.ibm.com/w3publisher/dte-cms-guidance/dte-platform-support) to ensure there isn’t a planned outage. If not, Business Partners can report it using [techzone.help@ibm.com](mailto:techzone.help@ibm.com).

Question #48: How do I change self-signed SSL certs for **CP4I** on ROKS?
Answer #48: Here are the steps to change your self-signed SSL certs for CP4I:

1.  Log in to your cluster with your IBMid.
2.  Switch to the Cloud Pak for Integration project (`cp4i` by default).
3.  Extract ROKS ingress certificates to your local folder.
4.  Split CA and cert.
5.  Delete the IBM Common Services route certificate.
6.  Delete the IBM Common Services route secret.
7.  Create a new route-tls-secret from the extracted certs.
8.  Patch the Automation UI config.
9.  Delete the IAF CA certificate.
10.  Delete the IAF certificate.
11.  Delete the external TLS secret:
12.  Create a new external TLS secret from the extracted certs.
13.  Restart all auth-idp pods.
14.  Restart all ibm-nginx pods.

Now check if you check your Cloud Pak for Integration dashboard route, you should see valid ROKS SSL certificates.

The command lines for each step can be found in our [How to Change Self-Signed SSL certs for **CP4I** on ROKS](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/cp4i-certs.md) runbook.

Question #49: How can I view the metrics of my collection?
Answer #49: View this [runbook]( https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/content-metrics.md) to learn how to view environment reservation metrics tied to a collection on IBM Technology Zone.

Question #50: How do I change my preferences GDPR sign off (i.e participate in notifications)?
Answer #50: To change your preferences:

1.  Select your profile icon located at the top of your navigation bar to the far right, then select 'Profile’.
2.  Select the ‘My opt-ins’ tab.
3.  Change your opt-in settings and click 'Save’.

To learn how you can change your preferences, view the following [document](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/ibmer-bp-gdpr-runbook.md).

Question #51: How do I fix a network error when attempting to fetch resource?
Answer #51: **Cause:** A timeout or a failure to communicate with the back-end servers like reservations, database, auth, or even the DTE2 api server

**Resolution:** Clear cache and retry the reservation

View our [Network Error when Attempting to Fetch Resource](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/NetworkError-when-attempting-to-fetch-resource.md) runbook to see if the error you saw corresponds with the screenshot in our runbook to properly diagnose the issue.

Question #52: What is the min/max number of multiple environments allowed?
Answer #52: The min number of environment's is 5 (Five) while max number of environments depends on the template size and resource availability.

Example: Template less than 1 TB maximum 70 environments, greater than 1TB maximum 20 environments, greater than 4TB maximum 8 environment and greater than 10TB maximum 5 environments.

Question #53: How do I change my preferences GDPR sign off (i.e participate in notifications)?
Answer #53: To change your preferences:

1.  Select your profile icon located at the top of your navigation bar to the far right, then select 'Profile’.
2.  Select the ‘My opt-ins’ tab.
3.  Change your opt-in settings and click 'Save’.

To learn how you can change your preferences, view the following [document](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/GDPR-client-runbook.md).

Question #54: What do I do when I have memory issues?
Answer #54: This is an issue that sometimes comes across in some Cloud Pak instances. It has been shown to resolve itself with time, so we ask that you be patient.

Question #55: What is a TechDemo?
Answer #55: A TechDemo is a collection with a journey aligned to lead-with or growth offerings and is owned by a Product Squad leader with role-based privileges to create Platinum level content.

Question #56: How do I publish my collection and/or resource on TechZone?
Answer #56: **Collection status change**:

On the edit collection form, navigate to the bottom right of the collection to the 'Collection status' field. Then change the status from draft to active. 

  

**Resource status change** **(Journeys and environments have a similar process):**

On the resource edit form, navigate to the bottom right of the resource to the 'Status' field. Then change the status from disabled to enabled. 

  

View our [How to Publish your Collection or Resource on TechZone](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/how-to-publish-on-itz.md) runbook for screenshots and step-by-step instructions.

Question #57: How do I share my ROKS cluster environment with another user?
Answer #57: Here are the steps to share a ROKS Cluster Environment:

1.  Go to "My Library" and click on "My reservations"
2.  Find the reservation that needs to be shared.
3.  Click on the three dots and select 'Share' from the dropdown options.
4.  Enter the IBMid you want to share your cluster with.
5.  Click on "Share" blue button

The cluster will automatically become available to the another user on IBM Cloud.

View [How To Share ROKS Cluster Environment](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/share_environment.md) runbook for step-by-step instructions with screenshots.

Question #58: How do I delete a reservation?
Answer #58: Here are the simple steps to delete your reservation:

1.  Locate ‘My library’ on the top of the page > Click ‘My reservations’ in the dropdown options.
2.  Locate the reservation you want to extend and click on the 3 dots > Click 'Delete’.
3.  Confirm your action by entering the value shown in bold (you can select the copy icon to copy and paste) and selecting 'Delete’. Your reservation will be automatically deleted.

View [How To Delete Your Reservati](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/delete-reservation.md)[on](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/extend-a-reservation.md) runbook for step-by-step instructions.

For questions about the environment or support, reach out to the author of the collection.

Question #59: What are the GDPR Guidelines and Features offered at IBM Technology Zone?
Answer #59: IBM Technology Zone is algined with IBM GDPR standards to properly capture your sign off on the data that we capture from you logging in and using the site.

In order to use IBM Technology Zone, you have to agree to the terms and conditions by checking the checkbox at the bottom left of the page. To view or change your opt-ins, view this [documentation](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/GDPR-client-runbook.md) to get step-by-step instructions.

Question #60: Are there existing demos I can leverage?
Answer #60: Yes, Platinum content is considered the highest quality offerings on the site today and there is one Platinum Live Demos collection per IBM Technology brand. You can access Platinum content from the Platinum or Featured tab on the home page. As well, you can contribute to an existing Live Demos collection by following the instructions in the [IBM Technology Zone programs guide](https://ibm.box.com/s/5oc5vww7j5pf9w9r7e5tgvsrcev7t7x6).

Question #61: How can clients gain access to content on the IBM Technology Zone?
Answer #61: Clients cannot access all of IBM Technology Zone as this portal is currently for internal IBMers and Business Partners. However, clients can access environments that are shared with them by IBMers and Business Partners. If you would like your clients to view an environment, they need to create an IBMid to be able to access the environment that you want to share with them.

  

Please send them to this [URL](https://www.ibm.com/account/reg/us-en/signup?formid=urx-19776&target=https%3A%2F%2Flogin.ibm.com%2Foidc%2Fendpoint%2Fdefault%2Fauthorize%3FqsId%3D1156c9eb-c357-471b-a524-9ae38869e775%26client_id%3DODllMDk4YzItMjgxOC00) to get started with creating their IBMid.

Question #62: How can I give feedback because content is wrong?
Answer #62: Contact the Content Author directly by selecting the help icon located at the top of the page. This will either direct you to a slack channel that the author has set up to support this content or an email modal will pop up to allow you to email them directly from the site.

Question #63: What do I do when I have memory issues?
Answer #63: This is an issue that occurs with some Cloud Pak instances. It has been shown to resolve itself in time, but if you are still having issues after a significant amount of time please contact [techzone.help@ibm.com](mailto:techzone.help@ibm.com) for further assistance.

Question #64: What is the turnaround time for an inquiry I post in Open a Case or Email: techzone.help@ibm.com?
Answer #64: [Open a case](https://ibmsf.force.com/ibminternalproducts/s/createrecord/NewCase?language=en_US) or Email: [techzone.help@ibm.com](mailto:techzone.help@ibm.com)t are monitored by support staff. Inquiries are addressed the same day as they are posted. If level one support cannot answer the inquiry themselves, they will escalate to SMEs who can respond and/or fix the issue. This escalation process is automated and issues are captured in GitHub for developers to manage as part of their development priorities. SLAs and services are posted in the **Help** section of the site.

Question #65: What do I do if I have issues registering my IBMid?
Answer #65: If you are having issues getting your IBM Cloud account created, it is most likely due to using a personal email account that was detected by IBM Cloud as a fraud account. It is recommended by IBM Cloud support to try registering again with a company email account.

Question #66: How do I add to an existing Activation Kit?
Answer #66: If you would like to add to an existing Activation Kit, use the **Ask for Help** icon at the top of the Kit page to work with the Content Author.

Question #67: Is content on IBM Technology Zone kept current?
Answer #67: Per the IBM Technology Zone Contributor Guidelines, all content contributors must adhere to quality, maintainance and support guidelines before publishing content on the site.

Question #68: How can I create a Platinum Collection?
Answer #68: Currently TechDemos are the only Platinum collections with authors who have gone through required enablement and onboarding. However, you can contribute to an existing TechDemos Platinum collection by following the instructions in the [IBM Technology Zone Programs](https://ibm.box.com/s/5oc5vww7j5pf9w9r7e5tgvsrcev7t7x6) overview guide.

Question #69: Where do I find my reserved Workshops?
Answer #69: You can find requested Workshops in “My library” tab on the IBM Technology Zone page, click on “My Workshops”.

Question #70: Where can I get help for Workshop Manager?
Answer #70: Contact the support team [Open a case](https://ibmsf.force.com/ibminternalproducts/s/createrecord/NewCase?language=en_US) or Email: [techzone.help@ibm.com](mailto:techzone.help@ibm.com) for all Workshop Manager help/inquiries.

Business Partners can report the issue using [techzone.help@ibm.com]( techzone.help@ibm.com)

  

Support Hours - 24/7.

Question #71: My Workshop was rejected what do I do?
Answer #71: Requesters are sent details for why their workshop was rejected and what is required to have it approved via [Open a case](https://ibmsf.force.com/ibminternalproducts/s/createrecord/NewCase?language=en_US) or Email: [techzone.help@ibm.com](mailto:techzone.help@ibm.com)

Business Partners - Contact ITZ Support - [techzone.help@ibm.com](mailto:techzone.help@ibm.com)

Question #72: If a workshop needs to be rescheduled, will it still be subject to the 72 hour lead time?
Answer #72: Yes, we need 72 hours notice to ensure we have capacity available for your workshop. Please contact support as soon as you have a shift in schedule so that we can work to the best of our ability to get you the environments you need based on capacity we have at that time.

Question #73: How do I transfer my reservation to another user?
Answer #73: Here are the steps on how to transfer a reservation:

1.  Go to "My Library" tab on the top of IBM Technology Zone > Click "My reservations" from the dropdown options >
2.  Locate what you would like to transfer and click on the 3 dots > Select 'Transfer' from the dropdown.
3.  Enter the IBMid to transfer to and enter the resource name. Note: all fields have to be field for "Transfer" to turn red.
4.  Click on "Transfer".
5.  The resource will now appear in the 'My reservations' of the person you transferred it to.

View [How To Transfer Your Reservati](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/transfer_environment.md)[on](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/extend-a-reservation.md) runbook for step-by-step instructions.

For questions about the environment or support, reach out to the author of the collection.

Question #74: What is the IBM Technology Zone?
Answer #74: **IBM Technology Zone** is the single destination for our technical go-to-market teams, business partner ecosystem, and customers to easily learn, build, customize, and share live environments with IBM technology that solve real customer problems and showcase the value of IBM. IBM created the IBM Technology Zone for our selling team and business partner ecosystem, however TechZone has evolved into the one-stop-shop for all infrastructure and demo environment needs such as workshops for IBM TechXchange conferences globally, self-learning environments, and of course, client demonstrations.

Users of Technology Zone can find and reserve a wide range of live environments across infrastructures and platforms with only a few clicks. **Get started** by visiting the **IBM TechZone** [**Onboarding Collection**](https://techzone.ibm.com/collection/onboarding) or dive right into IBM Technology Zone and experience featured IBM base-images first-hand in the [**TechZone Certified Base Images Collection**](https://techzone.ibm.com/collection/5fb3200cec8dd00017c57f20)**.**

Question #75: How can I effectively onboard to the IBM Technology Zone?
Answer #75: An [Onboarding Collection](https://techzone.ibm.com/collection/onboarding) has been created containing a series of helpful how-to videos to showcase new and existing site features, how to navigate the site, how to search for content, how to search & reserve an environment.

If you would like to suggest new videos and topics for the onboarding collection, comment on the onboarding collection page itself located towards the bottom of the page.

Question #76: What do I do when I get a certificate issue?
Answer #76: Follow this method to resolve this issue:

*   Run check-expiration.sh script to see if certs expired. Only then, run resetcert.sh
*   Run check-csr.sh to see if there are pending CSRs. Approve all the pending CSRs
*   Check nodes status using “oc get nodes”. Some nodes may be in “NotReady” state because of previous errors (pending CSRs). They are supposed to recover automatically and go into Ready state within 3-5 minutes. If this does not occur, try restating the environment.

If you are still having issues email [techzone.help@ibm.com](techzone.help@ibm.com) for further support or visit [#itz-workshop-support](https://ibm-techzone.slack.com/archives/CTA2MV9AM) slack channel so we can assist with additional troubleshooting.

Question #77: Why have my environments not been provisioned?
Answer #77: Environments are provisioned at least 2 hours before the requested start date and time

Question #78: How can I request multiple environments for group reservations, group engagements or workshops?
Answer #78: Group reservations, group engagements or workshops can be scheduled on IBM Technology Zone using the “schedule a workshop” feature which allows you the ability to request multiple environment using the Workshop Manager tool. On a Workshop Manager request, you may select the desired environment, specify the number of environments and attendees, and choose the start and end dates. You can also save draft requests for later.

At this time, workshops support VMWare, IBM Cloud, SaaS, and Hosted environment requests.

For more information about requesting a multiple environments for group reservations, group engagements or workshops, view the [How to schedule a hosted workshop](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/How-to-schedule-a-hosted-workshop.md) runbook.

([https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/How-to-schedule-a-hosted-workshop.md](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/How-to-schedule-a-hosted-workshop.md))

For more information about the maximum number of environments, view the [Reservation Duration Policy](https://github.com/IBM/itz-support-public/blob/eaf03a72d78dc771c0b46d6c3404b230d8edb2c4/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/reservation-duration-policy.md) runbook.

Question #79: I asked for 15 environments and was told I’d get 15, why am I only seeing 7 right now?
Answer #79: Your workshop was set to autogrow\*\*

\*\*autogrow- is a feature where environments are automatically provisioned on a need base until the maximum number of environments have been deployed. Once you start to claim environments, as fewer become available, more will begin to deploy automatically until you have the full number of environments that you requested.

Question #80: How do I manage my workshop as an Instructor
Answer #80: You manage your workshop directly from the “My Workshop” page. See box folder [How do I manage my workshop as an Instructor](https://ibm.box.com/s/o4879elzfn78pa6x6fvzj7hcbaninssa)

Question #81: Can additional instructors be added later to a Workshop?
Answer #81: At this moment, additional instructors can be added by yourself up till the workshop is approved. If you would like to add an additional instructor after that time, please contact support with the email of the instructor that you would like to add.

Question #82: How can I create a resource?
Answer #82: Steps to create the a resource:

1.  Navigate to ‘My Resources’
2.  Click the ‘Edit’ button on the top right corner of the screen
3.  Scroll down until you see the ‘Resources’ section and click the 'Add a Resource’.

For a demo, watch this video to learn [How to Create a Resource](https://ibm.box.com/s/t1k31yr2ylygkdaaolbwvjut9tkgks4k).

Question #83: How do I catalog an environment?
Answer #83: Here are the steps to cataloguing an environment:

1.  Navigate to the resource that is cataloging the environment you want to reproduce.
2.  Click on the resource > It will take you to a Box Folder url where you will find an image/screenshot of the environment settings.
3.  Mimic the same environment settings as the screenshot to achieve your desired environment.
4.  To customize your environment further, view this [runbook](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/gitops-tf-override.md) to learn how you can override your environment setting.

View [How to Catalog Your Own Environment](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/catalog-your-environment.md) runbook for step-by-step instructions.

For questions about the environment or support, reach out to the author of the collection.

Question #84: How do I upgrade configurations on my reserved environment?
Answer #84: Here are ways you can upgrade your environment’s configurations:

*   Adding VMs
*   \[Adding worker nodes\](itz-support-public/resizing-roks-cluster-worker-pool.md at main · IBM/itz-support-public)
*   Adding storage

To make any of these upgrades, follow the runbooks or request help from ITZ support:

A **Business Partner** can leverage: [techzone.help@ibm.com](mailto:techzone.help@ibm.com)

An **IBMer** can leverage the slack channel: [Open a case](https://ibmsf.force.com/ibminternalproducts/s/createrecord/NewCase?language=en_US) or Email: [techzone.help@ibm.com](mailto:techzone.help@ibm.com)

Question #85: What are some valid opportunity code to input on reservation form?
Answer #85: View [Valid Opportunity Code To Input for Your Own Environment](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/valid-opportunity-codes.md) runbook to learn how opportunity codes are validated and what systems/portals we work with to validate them when users are making a reservation.

For questions about the environment or support, reach out to the author of the collection.

Question #86: How do I find collections with Technical Decision Points?
Answer #86: You can find them by clicking on the first journey on the IBM Technology Zone home page. You can also find them by filtering your search by clicking on “Show Advanced” and then locating the “Technical Decision Points” category.

Question #87: How do I report ROKS Issues?
Answer #87: Please provide this information to support to help speed up the process:

*   **Minimum Information Needed**:
*   cluster name or cluster ID
*   environment/reservation owner if not yourself
*   short description of the issues
*   Additional information if related:
*   worker name or IP address if you need help reloading or rebooting a worker
*   cloud pak name if the issue is related to a cloud pak install or usage
*   user name/id if the issue is related to acess

Business Partners - Contact ITZ Support - [techzone.help@ibm.com](mailto:techzone.help@ibm.com)

IBMers - Make a post on [Open a case](https://ibmsf.force.com/ibminternalproducts/s/createrecord/NewCase?language=en_US) or Email: [techzone.help@ibm.com](mailto:techzone.help@ibm.com)

Question #88: How do I resize my ROKS cluster worker pool?
Answer #88: View [Resizing a ROKS cluster worker pool](https://github.ibm.com/dte-support/private/blob/master/IBM-Cloud/ROKS/resizing-roks-cluster-worker-pool.md) runbook for step-by-step instructions.

Question #89: How long does it typically take for a contribution to a collection to be approved?
Answer #89: Anyone can contribute a collection of Gold, Silver, Bronze. A collection will only have an approval process if it goes through the platinum review board. Platinum is where the additional review comes in. Approval timeline is unique to the collection and can be determined by your Squad Lead.

Question #90: Can I get an IP for my environment?
Answer #90: No, public IPs are not allowed for environment access. Some VMs in environments have opened ports and can be accessed using published services. If ports are opened for a VM you will receive the details when the activation email was received.

Question #91: What is a journey?
Answer #91: A journey is simply a tab. For example, the tabs inside a collection are called journeys as they essentially help guide users through the content.

View the [Introduction to Journeys](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/intro-collection-journey.md) runbook to learn more about them.

Question #92: Can I see usage metrics for my content?
Answer #92: Yes, As consumers begin to search and curate content, Content Authors can view the following metrics to track content usage: pageviews, unique users, type of users (IBMer or BP), and region of user. To get started, review the [Content metrics](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/content-metrics.md) runbook.

Question #93: How do I ensure the content URL I share does not change when sending to others?
Answer #93: We recommend using vanity URLs when sharing any content. When or if a URL changes, a vanity URL gives you the power to control where the user gets redirected. Start creating your custom vanity URLs [here](https://snip.innovate.ibm.com/) and take control of any changing links.

Question #94: How can I leverage IBM Technology Zone?
Answer #94: IBM Technology Zone can be leveraged in multiple ways:

*   Consume content - leverage the [onboarding](https://techzone.ibm.com/collection/onboarding) materials to learn how to effectively navigate and consume content
*   Build content – use the environments provided to build a ‘Show Me’ demo for your customers utilizing the various branding standards for [Bronze, Silver, Gold and Platinum](https://ibm.box.com/s/5oc5vww7j5pf9w9r7e5tgvsrcev7t7x6) content
*   Share content – take advantage of the IBM Technology Zone [Rewards Program](https://ibm.box.com/s/5oc5vww7j5pf9w9r7e5tgvsrcev7t7x6) by sharing your branded content and earn points towards Blue Points rewards!
*   Curate content – earn points for rating, flagging favorite, and bookmarking site content

Question #95: Workshop Manager Support
Answer #95: ### Workshop Manager allows you to reserve multiple instances of a demo environment for your internal and client needs. Workshop Manager provides the ability to schedule your environments in advance to ensure they are available and ready to use. As the Workshop owner, you will have the ability to manage your environments, including starting, stopping, or adding more as needed. Leverage our 24 x 7 Support IBMers - Click on [Open a case](https://ibmsf.force.com/ibminternalproducts/s/createrecord/NewCase?language=en_US) to create a support case, runbook on “How to Open a Case” can be found [here](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/open_case_web_internal.md)

  

Business Partners - Contact ITZ Support - [techzone.help@ibm.com](mailto:techzone.help@ibm.com)

Question #96: How can I create a journey?
Answer #96: View the [How to Create a Journey](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/journey-creation-process.md) runbook to learn.

Question #97: What are the GDPR Guidelines and Features for clients on techzone?
Answer #97: IBM Technology Zone is aligned with IBM GDPR standards and this [document](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/GDPR-client-runbook.md) will demonstrate the data that we capture from you logging in and using the site.

In order to use IBM Technology Zone, you have to agree to the terms and conditions by checking the checkbox at the bottom left of the page. To change your opt-in at any time, view this [runbook](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/GDPR-client-runbook.md) to learn how.

Question #98: What is a bookmark search?
Answer #98: A bookmark is used to save a search, as it saves any keyword or filters. Leverage the [onboarding materials](https://techzone.ibm.com/collection/onboarding) to watch a self-help video outlining how to use this feature and others on the site.

Question #99: What is an Activation Kit?
Answer #99: Activation Kits are collections with predefined tabs, tied to products and solutions defined by brand technical executives and may be aligned to a Technology Decision Point (TDP), that consolidates and organizes other Technology Zone collections, as well resources, from multiple repositories so that technical go-to-market teams and the Business Partner ecosystem can "show", progress client opportunities, and implement solutions.

Question #100: Who do I contact for content support?
Answer #100: Content is supported by the Content Contributor. There is a help icon located at the top of every page for you to get in contact directly with the content owners through options of a direct email modal option from the site, a community-monitored Slack channel or collaborators that support the content for you to get in contact with your content support questions.

For site or environment support, send an issue or inquiry to [Open a case](https://ibmsf.force.com/ibminternalproducts/s/createrecord/NewCase?language=en_US) or Email: [techzone.help@ibm.com](mailto:techzone.help@ibm.com). Business Partners should use [techzone.help@ibm.com](mailto:techzone.help@ibm.com) for all of their support requirements.

All support offerings are outlined under the **Help** page from the top navigation bar.

For further instructions on how to proceed with getting support on collection, leverage our runbook [How to Get Support](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/How%20to%20get%20support.md).

Question #101: How can I provide feedback about IBM Technology Zone?
Answer #101: Feedback can be provided via the [Open a case](https://ibmsf.force.com/ibminternalproducts/s/createrecord/NewCase?language=en_US) or Email: [techzone.help@ibm.com](mailto:techzone.help@ibm.com). Business Partners should use [techzone.help@ibm.com](mailto:techzone.help@ibm.com) for all of their support requirements.

If your feedback is relative to a request for enhancement or system requirement, please use the [IBM Technology Zone Enhancements](https://itz-enhancements.ideas.aha.io/portal_session/new) portal.

Question #102: Will using the IBM Technology Zone cost me/my department, i.e. are there charge backs?
Answer #102: Use of the IBM Technology Zone is free of charge to Technical Sellers, Technology Garage, Technology Enablement, Customer Success Managers, GBS, and Business Partners. At this time all usage/reservations made through Technology Zone infrastructure options are free of charge.

Question #103: How many environments can I reserve, and for how long?
Answer #103: Each request is different in terms of the size of the environment, time requested, and what other events are planned during your requested time. For a very large environment such as Cloud Pak for Data, we cannot support more than 10 environments in a given region for up to 2 days. For smaller environments such as Cognos, we have the ability to support more than 20 for over a week.

Unfortunately, there is no set standard response to any given request, so we suggest limiting the number of environments and the amount of time you need them for your workshop. Please make sure to plan your workshop through Workshop manager tool before confirming dates with clients to ensure we have the capacity for the workshop.

Question #104: I need to provision an OpenShift Container Platform (ROKS) environment to validate a client scenario. How can I get access to this?
Answer #104: IBM Technology Zone does have OpenShift options available, labeled as ROKS infrastructure options. Select the ‘Environments’ tab located in the top navigation bar and select the ‘Infrastructure’ filter drop down to filter on ROKS specific options. Select the blue desktop icon located to the right to start your reservation request.

Question #105: How can I find out about site outages, announcements, and/or important news about IBM Technology Zone?
Answer #105: Join the [**#itz-techzone-announcements**](https://ibm-dte.slack.com/app_redirect?channel=itz-techzone-announcements) Slack channel for all things IBM Technology Zone. From news, announcements, roadmaps, webinar events, user surveys, contests, and more. The announcements channel is your one-stop shop!

Check out other [engagement methods](https://ibm.box.com/s/so63jezi3xmiwl56enn0vh4ghaq2beyc) our team has in place today and their purpose breakouts. The list includes: [Notifications page](https://techzone.ibm.com/notifications), [Open a case](https://ibmsf.force.com/ibminternalproducts/s/createrecord/NewCase?language=en_US) or Email: [techzone.help@ibm.com](mailto:techzone.help@ibm.com), [#itz-workshop-support](https://ibm-dte.slack.com/app_redirect?channel=itz-workshop-support), home page banner, and home page alert.

Question #106: How do I request a Workshop on IBM Technology zone?
Answer #106: Leverage the “Request multiple environments for workshop” option on the “Create a reservation page”. Go to the “Environments” tab on the IBM Technology Zone Page, Search for the required resource and click “reserve”

Question #107: Who can request a workshop using Workshop Manager?
Answer #107: IBMrs are the only users that we currently support with Workshop Manager at this time. IBMrs can request workshops on behalf of business partners or setup a workshop to do enablement sessions with business partners, but business partners accessing the site will not see the request or schedule a workshop option today.

Question #108: How can I search for an environment?
Answer #108: View this video to learn [How to Search for an Environment](https://ibm.ent.box.com/s/h8m5hvyr1ikexq8b3jfpdnxbvglnqgg2).

Question #109: I got a “Reservation: Not a Production Template” error, can anyone help?
Answer #109: Cause of error: The template associated with the collection has not been onboarded.

Resolution: Contact ITZ support:

**Business Partners** - Contact ITZ Support - [techzone.help@ibm.com](mailto:techzone.help@ibm.com)

**IBMers** - Make a post on the [Open a case](https://ibmsf.force.com/ibminternalproducts/s/createrecord/NewCase?language=en_US) or Email: [techzone.help@ibm.com](mailto:techzone.help@ibm.com)

Question #110: What is a collection?
Answer #110: A collection is a group of resources and environments all collected onto one page.

An example of a collection: The Security Verify experience page is a collection since it houses resources like a video, overview and use cases documentation, guided simulation, additional support resource links, and most importantly the register for the experience labeled as an environment. All types of content associated on this page make the Security Verify page a collection.

Question #111: What are Technical Decision Points?
Answer #111: Technology Decision Points (TDPs) are strategic IBM technologies that we want to land at our clients, which position them to succeed in the post-COVID market.

To learn more about TDPs, click [here](https://ibm.seismic.com/app?ContentId=6fff78a4-d544-41c7-b33c-2e5bd2cceba9#/doccenter/5477419a-9474-4c51-94af-b442e9169fab/doc/%252Flfe527a70b-a9b5-4445-a400-c4fed5ce4f71/grid/).

View this [runbook](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/technical-decision-points.md) to learn more.

Question #112: What if I do not have an opportunity code, but I know I will need the environment longer for my client engagement?
Answer #112: Send an email to [techzone.help@ibm.com](mailto:techzone.help@ibm.com) requesting an exception.

Question #113: How do I request a specific environment that is not listed on the IBM Technology Zone?
Answer #113: If you are looking for an environment option that the IBM Technology Zone does not have already on the site, submit your infrastructure request through [IBM Technology Zone Enhancements](https://itz-enhancements.ideas.aha.io/portal_session/new) .

Question #114: I have submitted my workshop what next?
Answer #114: Workshop request are reviewed (approved/rejected) within 72 hours from when they where submitted

Question #115: How do I onboard an environment to be used for Workshop Manager requests?
Answer #115: To onboard a template at this time, please fill out our [custom request form](https://custom-requests.ideas.aha.io) and provide the template information that you would like onboarded. Select the request type: Template onboarding request. Our team will review and upon approval work with you to determine next steps on how to catalog the environment to the site.

Question #116: How do I change self-signed SSL certs for **CP4D** on ROKS?
Answer #116: Here are the steps to change self-signed SSL certs for CP4D:

1.  Log in to your cluster with your IBMid.
2.  Switch to the Cloud Pak for Data project (`zen` by default):
3.  Extract ROKS ingress certificates to your local folder:
4.  Create a new external-tls-secret from the extracted certs:
5.  Restart all ibm-nginx pods:

Now you should be able to check Cloud Pak for Data dashboard route and see valid ROKS SSL certificates.

For more details, check out our [How to Change Self-Signed SSL certs for **CP4D** on ROKS](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/cp4d-certs.md) runbook.

Question #117: How do I add an ODF/OCS storage cluster to a ROKS cluster?
Answer #117: Please contact our support team for [Open a case](https://ibmsf.force.com/ibminternalproducts/s/createrecord/NewCase?language=en_US) or Email: [techzone.help@ibm.com](mailto:techzone.help@ibm.com)o to increase your storage cluster. **_Disclaimer:_** At this time, this is only available for ROKS on VPC. Increasing storage cluster for ROKs on Classic is not supported.

View the [Adding an ODF/OCS storage cluster to a ROKS cluster](https://github.ibm.com/dte-support/private/blob/master/IBM-Cloud/ROKS/adding-odf-storage-cluster-to-roks.md) runbook for additional help and clarification.

Question #118: How do I search for Platinum content?
Answer #118: There are two ways you can browse through Platinum Content:

1.  Locate the “Platinum” tab on the IBM Technology Zone banner.
2.  On the “Environment” page there is a button "Advanced Filter", navigate to the “Contributor Flags” option and click the option "Platinum".

Question #119: How do I search for technical content?
Answer #119: We suggest you leverage the [Onboarding Materials](https://techzone.ibm.com/collection/onboarding) as there is a great self-help video outlining how to effectively search for content.

Question #120: Who do I contact if something is broken on the site?
Answer #120: You should initially check the [System Status site](https://w3.ibm.com/w3publisher/dte-cms-guidance/dte-platform-support) to ensure there isn’t a planned outage. If not, report this by creating a support case by click on the [support web form](https://ibmsf.force.com/ibminternalproducts/s/createrecord/NewCase?language=en_US) or sending a mail [techzone.help@ibm.com](mailto:techzone.help@ibm.com).

Question #121: I have multiple instructors how do I give them access?
Answer #121: Add all required instructors to the required instructor email field which can be found in step 4: "workshop information".

Question #122: I'm having trouble setting up/cataloging an environment, can anyone help?
Answer #122: For any questions or concerns pertaining to setting up or cataloging an environment, reach out to the content author on the collection for help.

Question #123: How can I request an enhancement or redesign for IBM Technology Zone?
Answer #123: As an IBMer, you can use the [IBM Technology Zone Enhancements](https://itz-enhancements.ideas.aha.io/portal_session/new) to log any enhancement or redesign requests.

Question #124: How can I create a Collection?
Answer #124: All IBMrs and Business Partners can create a Collection. To create a collection, from the home page, select the **Share your content** button in the top right corner, then follow the guidance outlined in the submission form.

View this video on [How to Create a Collection](https://ibm.ent.box.com/s/r9ywt10xjl47d2sfmtk4gxtc2e07jhqh) for more details.

Question #125: What industries are supported on IBM Technology Zone?
Answer #125: *   Financial Services Sector - Banking, Insurance
*   Communications Sector - Telco, Media, Entertainment, Energy, Environment, Utilities
*   Distribution Sector - Consumer Industries (Agribusiness, Consumer Products, Retail), Travel & Transportation
*   Industrial Sector - Automotive, Aerospace &
*   Defense, Chemicals, Petroleum & Industrial Products, Electronics
*   Public Sector - Government, Healthcare & Life Sciences

Question #126: What can business partners access on IBM Technology Zone?
Answer #126: Business Partners have access to a wide range of collections and environments on IBM Technology Zone. IBMrs can leverage this [business partner visibility runbook](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/bp-visibility.md) to help navigate what partners can and can not access on the site.

*   Leverage visibility filters on every search page to see what is visible to business partners
*   Reference every collection, resource, environment tile to see what is visible to business partners
*   If you have questions for the author about why a collection or environment is not visible to business partners, contact the author for additional support on this inquiry

All referenced within the business partner visibility runbook.

Question #127: How do I manage my Workshop?
Answer #127: You manage your workshop from the “My Workshop” tab. Select the Workshop Name from the list to see Information details.

Question #128: I got an "Business Partner Access Error(403)", can anyone help?
Answer #128: View this [runbook](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/BusinessPartnersAccess.md) to resolve this issue.

Question #129: How do I add my collection to a TDP on the Technical decision points tab?
Answer #129: At this time, only selected Activation Kits and Platinum Demo Collections will represent a TDP on the Technical decision points tab. People can no longer flag their own content under a TDP. If you feel as though your content should be part of a TDP, reach out to the [TDP owners](https://ibm.box.com/v/tdp-allocations-and-owners) who will review and determine if your content should be included. If approved, your content will either be added to the Activation Kit or Platinum Live Demos collection for that TDP and not as a standalone collection.

Question #130: How do I create advanced Mermaid journeys on my collections?
Answer #130: The main purpose of Mermaid is to help with Visualizing Documentation and resources using text and code.

To learn how you can create them, view our runbook [Customized Journeys with Mermaid](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/mermaid-docs.md) to receive support and step-by-step instructions.

Question #131: Does “Public Cloud Providers” include Power options? Power Virtual Server and/or Skytap?
Answer #131: Yes. PowerVS is a part of public IBM Cloud provider.

Please see the following examples for Power Virtual Server (PowerVS) :

*   [IBM Power Sap](https://github.ibm.com/dte2-0/ccp-gitops-patterns/tree/main/ibm-power-sap)
*   [IBM PVS IAAS](https://github.ibm.com/dte2-0/ccp-gitops-patterns/tree/main/ibm-pvs-iaas)

Public provider Skytap is also included.

Question #132: How to schedule a Hosted workshop?
Answer #132: Here are the steps to schedule a workshop:

1.  From the IBM Technology Home page > Click ‘Environments’
2.  Filter for the desired Infrastructure (Hosted)
3.  Find the environment you would like to use for your workshop > Click on the ‘Reserve’ icon
4.  Select ‘Schedule a workshop’ > You will be taken to the “Request a workshop” page.
5.  After going through each step filling out your workshop details > Click Done.

For **Hosted**: For more details and instructions, view our [How to Schedule a Hosted workshop](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/How-to-schedule-a-hosted-workshop.md) runbook.

Question #133: How do I get content support?
Answer #133: Content Support for all Collections, resources and environments are handled by the Content Author.

To report/log a content issue follow steps listed below.

1.  Go to the Collection/resource > Click on the Question Mark “Ask for help” > Select the “Ask for help or report a problem with the content on this page”
2.  Fill out the form with details and click send. This will go directly to the content author, collaborators or the support contact listed for the collection/resource.

Note: By clicking on the “Ask for Help” button for some collection/resource instances, this will direct you to slack channels for support.

View this [runbook](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/ContentSupport.md) for step-by-step with screenshots to learn how to leverage content support.

Question #134: How do I create a journey?
Answer #134: Before you get started, you must already have created a collection.

Here are the steps to create a journey:

1.  Once on the edit collection page scroll down to the journeys section.
2.  Select “Add a journey” button to create your first journey.
3.  Fill in the minimum required journey fields: Title, description, visibility and status.
4.  Now, lets associate which resources and environments that you would like to display in this collection. Drag and drop the resources and environments that you want on the journey tab to the right hand Journey section.
5.  Select ‘Save’ to capture this newly created journey.
6.  Navigate to the ‘Preview’ button at the bottom of the edit collection form to see how your new journey will display.
7.  Then proceed down to the bottom of your edit collection form to save the entire collection with this newly added journey.

You have now created your first journey.

For more step-by-step instructions with images, view our [How To Create a Journey](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/journey-creation-process.md) runbook

Question #135: How do I update my reservation to enable the self-service extension option?
Answer #135: Here are the simple steps to extend your reservation:

1.  Locate ‘My library’ on the top of the page > Click ‘My reservations’ in the dropdown options.
2.  Locate the reservation you want to edit and click on the 3 dots > Click 'Reservation details'.
3.  Select the 'Edit' button from the reservation details page.
4.  Select the new purpose that you would like to update for this reservation.
5.  Include the opportunity code from IBM Sales Cloud or relationship ID from Gainsite.
6.  Select the 'Save' button to capture the changes to your reservation.
7.  Wait a few minutes for your changes to process, then return to the 'My reservations' page.
8.  Locate the reservation you want to extend and click on the 3 dots > and see now the 'Extend' option will not display after updating the reservation details.
9.  Click the 'Extend' button and extend the reservation one week out from today's date.

View [How to Update Your Reservation](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/extend-self-education-into-sales-demo.md) purpose and opportunity code runbook for screenshots with step-by-step instructions.

Additional runbook option: View [How To Extend Your Reservation](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/extend-a-reservation.md) runbook for screenshots of the step-by-step instructions.

  

For questions about the environment or support, reach out to the author of the collection.

Question #136: Can I share my environments/reservation?
Answer #136: Yes, you can share your environments with an IBMr, Business Partners or Client. Additional information on "[How do I share my environment](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/share_environment.md)"

Question #137: Can I use customer data in an IBM Technology Zone environment?
Answer #137: IBM Technology Zone allows a select set of environments that will support specific classifications of customer data. For unsupported customer data classifications, self-generated data is recommended to avoid any PI/SPI data being injected into a Technology Zone environment. Dummy, fake, or sample data is allowed. For more information including exceptions, view the [Customer Data Enabled Environments on IBM Technology Zone](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Customer-data%20on%20TechZone.md) runbook.[  
](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Customer-data%20on%20TechZone.md)  
**Supported Customer Data Classifications:**

*   Publicly available (example of data available through the web is [BERKELEY SETI RESEARCH CENTRE](https://seti.berkeley.edu/listen/data.html))
*   Anonymized / Obfuscated / Masked
*   Non-PI

**NOT Supported Customer Data Classifications:**

*   No regulated data allowed. Regulated - PI, SPI, PCI, PHI, Financial Data, Other.
*   Governed by a plethora of global/federal/local regulations- GDPR, HIPAA, GLB, FTC, CCPA, Sarbanes-Oxley, + many others. Regulated data requires engaging Legal & BISO.

Question #138: Can we test a collection (environments) before it is published?
Answer #138: Yes, you can test environments in a collection by adding a user/tester as a collaborators to the collection and leave collection status in “draft”

Additional details in [Runbook](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/testing-collections-before-launch.md)

Question #139: When does my workshop get approved?
Answer #139: Workshop request are reviewed (approved/rejected) within 72 hours from when they were submitted

Question #140: Why have my workshop environments not been provisioned?
Answer #140: 1.    Environments are provisioned at least 4 hours before the requested start date and time

Question #141: What are the Terms and Conditions for using IBM Technology Zone?
Answer #141: When IBM Technology Zone users first log in to TechZone, they were prompted with a terms and conditions page. To re-review the content that you agreed to, please visit: [https://techzone.ibm.com/terms](https://techzone.ibm.com/terms)

Question #142: How do I get IBM Technology Zone certified?
Answer #142: This badge earner will have a foundational understanding of what IBM Technology Zone is, how to effectively leverage to drive deal progression, and has successfully demonstrated an IBM product or solution using a live IBM Technology Zone environment.

To get IBM certified, click on the following link:

*   [IBM Employees complete the course here.](https://yourlearning.ibm.com/activity/PLAN-312D48375968)
*   [Business Partners complete the course here.](https://learn.ibm.com/course/view.php?id=12725)

Question #143: I have this environment and need to replicate in TechZone.
Answer #143: Please make absolutely sure that your environment or something similar doesn’t already exist in TechZone. There are over 700 technical assets available in TechZone today, built by SMEs and IBM product practitioners. If you are positive there’s nothing that can be used in TechZone, then you should consider porting your application into TechZone by leveraging a [TechZone Certified Base Image](https://techzone.ibm.com/collection/tech-zone-certified-base-images).

Question #144: Why doesn’t the ‘Reservations’ option display on my collection options list?
Answer #144: Answer: ‘Reservations’ option will only display if there is an environment catalogued on your collection.

Here are the steps to check:

1.  Select the collection edit button
2.  Scroll down to the Environments section to see if there are any environments catalogued on this collection.

*   If there are no environments catalogued on this collection that need to be, please use the ‘Create an environment’ runbook for next steps on how to add an environment to your collection.
*   If there is an environment catalogued on this collection, then please contact support with the collection URL so we can create an issue and further investigate this issue.

Question #145: Can a Business Partner "Schedule a workshop"?
Answer #145: No, that option is not available to a Business Partner

Question #146: Can I request a Custom Environment?
Answer #146: Yes, you can request a custom environment using our [Custom Request Form](https://ibm.biz/dte-environment-requests)  
This [Runbook](https://ibm.ent.box.com/s/8gx9dohzo0ie3sxfxm89ofs99x071b8z) has instructions for making a request.

Question #147: I persist MVP workloads for a client that purchases IBM Cloud?
Answer #147: a commercial POC account free for up to 90 days utilizing the following instructions, [https://ibm.box.com/v/commercial-poc-process](https://ibm.box.com/v/commercial-poc-process)

Question #148: Can memory be added to the nodes of an existing cluster?
Answer #148: No, memory cannot be added to the nodes of an existing cluster. Worker memory is fixed based on “flavor” of the node.

Workaround

1.  Add more worker nodes to your existing worker pool, detail on how to can be found \[here\](itz-support-public/resizing-roks-cluster-worker-pool.md at main · IBM/itz-support-public)
2.  Create a new worker pool with a flavor that has more CPU and memory

Question #149: What is Model Home?
Answer #149: Model Home showcases a suite of IBM solutions that provide visibility, control, and automation of IBM Technology Zone's hybrid cloud infrastructure and the workloads it runs. Check out the Model Home collection to learn more about the IBM solutions that IBM Technology Zone uses and get immediate read-only access to production environments to see IBM products at work.

Model Home: [https://ibm.biz/tzmodelhome](https://ibm.biz/tzmodelhome)

Question #150: How can I extend my environment without an opportunity number?
Answer #150: You can extend your environment without an opportunity number by requesting an exception using our [Custom Request Form](https://custom-requests.ideas.aha.io/ideas/new).

Question #151: How to accept an IBM Cloud invite?
Answer #151: To accept an IBM Cloud invite, you can accept it **through your email** or **through your IBM Cloud account**.

To see the step-by-step instructions (with screenshots) of these two ways of accepting an invite, view our [runbook](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/ibm-cloud-accept-invite.md).

Question #152: Can I transfer my environment/reservation to another user?
Answer #152: Yes, you can transfer an environment/reservation to another user. Guide on "[How do I transfer my environment/reservation to another user](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/transfer_environment.md)?

Question #153: What is a Hands-on Lab?
Answer #153: It’s a set of tasks with included steps that users follow to review or build a use case. Targets pre-sale situation, which typically require reservation of an environment.

**_Disclaimer:_** The term "Hands-on Lab" has now been retired and the correct term is "live environment". This update will soon be applied across all IBM Technology Zone.

Question #154: What if a Business Partner does not want to contribute content on ITZ because they don’t want the competitors see what they are doing?
Answer #154: This is not a problem. Business Partners can create their own collections and leave them in a **status of draft** if they do not want other partners or IBMrs to see their resources and environments. If they want only specific people to be able to access their collection, they can add them as collaborators to the collection.

Question #155: Why are no reservation metrics displaying after selecting the ‘Reservations’ option?
Answer #155: Answer: Reservation metrics are captured from environments that are catalogued on a collection and the provisioning pipeline has to be one that IBM Technology Zone team currently supports. If you have an environment catalogued on your collection that is of infrastructure type: Systems Redirect, or Hosted Redirect then please note that these environment options are merely a redirect to another site where then the reservation is to be provisioned from. As we consolidate additional environments from CECC, ISCEP, SCS and more these metrics will start to display on your collections once they are reserved directly from an IBM Technology Zone collection.

Here are the steps to check:

1.  Select the collection edit button
2.  Scroll down to the Environments section
3.  Select an Environment to see the ‘Infrastructure’ field.

*   If you have an environment catalogued as one of the infrastructure redirect types and would like to know when the environment is planned to be migrated, please contact [brooke.jones@ibm.com](mailto:brooke.jones@ibm.com). We are currently working with CECC, ISCEP, SCS and SBaaS portals to consolidate environments to IBM Technology Zone.

If you have an environment that is not of the infrastructure redirect types, as mentioned above, then please contact support as there might be an issue with how the environment is catalogued or there could be issues with the environment itself not taking reservations.

Question #156: Who can access TechZone?
Answer #156: IBM Technology Zone is accessible to IBMers, Business Partners, and Customers.

*   IBMers can log in with their W3id credentials.
*   Business Partners can log in with the IBMid associated with their Partner Plus account. Partners having issues logging into IBM Technology Zone should reach out to their company authorized profile administrators (APA) to have their IBMid associated with their company partner account.
*   Customers can log in with an IBMid.

To get started with TechZone, navigate to the onboarding page for either IBMers or Business Partners:

Welcome [IBMers](https://techzone.ibm.com/collection/onboarding/journey-welcome-ibmers) ([https://techzone.ibm.com/collection/onboarding/journey-welcome-ibmers](https://techzone.ibm.com/collection/onboarding/journey-welcome-ibmers))  
Welcome [Business Partners](https://techzone.ibm.com/collection/onboarding/journey-welcome-partners) ([https://techzone.ibm.com/collection/onboarding/journey-welcome-partners](https://techzone.ibm.com/collection/onboarding/journey-welcome-partners))

For Business Partners who need further assistance accessing TechZone, view the [Business Partner Access runbook](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/BusinessPartnersAccess.md). ([https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/BusinessPartnersAccess.md](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/BusinessPartnersAccess.md))

Question #157: Can infrastructure be physically isolated once the resources are reserved for a specific workshop?
Answer #157:   
If the resources are for a workshop the workshop owner should have capacity dedicated to them for their customer facing purpose. TechZone cannot provision an entire bare metal server for every user.

Question #158: My Cloud account is being cancelled can you stop it?
Answer #158: Cloud accounts are between the IBM Cloud team and individual owners. The IBM Technology Zone Customer Care team is unable to assist with this request.

If you received a notice of suspension and believe there is a justified purpose for your Cloud account, please review the ‘Internal Account Suspension’ email to understand the next steps.

Question #159: Can I template my reservations?
Answer #159: Yes, you can now create a template for your IBM Cloud Classic reservations.

Question #160: I have this environment and need to replicate in TechZone.
Answer #160: Please make absolutely sure that your environment or something similar doesn’t already exist in TechZone. There are over 700 technical assets available in TechZone today, built by SMEs and IBM product practitioners. If you are positive there’s nothing that can be used in TechZone, then you should consider porting your application into TechZone by leveraging a [TechZone Certified Base Image](https://techzone.ibm.com/collection/tech-zone-certified-base-images).

Question #161: How can I extend my environment outside the standard reservation duration policies?
Answer #161: If you require extensions outside the [standard reservation duration policies](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/reservation-duration-policy.md), make use of our [Custom Request Form](https://ibm.biz/dte-environment-requests)

Question #162: Can I recover a deleted environment?
Answer #162: We do not store backups for deleted environments, they cannot be recovered. Kindly ensure you extend your environments before they expire.

Question #163: What is TechZone Deployer?
Answer #163: IBM TechZone Deployer or Technology Zone Deployer is a complementary system that works together to enable technical sellers to build and deploy IBM software quickly and easily. Deployer also enables Technical sellers to use the same automation technology in both TechZone and customer infrastructure. Additional details can be found [here.](https://pages.github.ibm.com/skol/itz-deployer-docs/)

Question #164: 
Answer #164: Yes, it is automatically subscribed to the RHN (Red Hat Network)

Question #165: How do I request extensions?
Answer #165:  IBMers should open a [Open a case](mailto:Open%20a%20case), and Business Partners can report the issue using Email: [techzone.help@ibm.com](mailto:techzone.help@ibm.com) for support to request extensions. Note: Opportunity numbers or valid use cases are required for all extension requests. Extensions are also granted based on resource availability.

Question #166: How to enable an IBM Cloud environment for workshop requests?
Answer #166: Workshop Manager can now manage requests for IBM Cloud environments, but not all IBM Cloud environments are enabled today.

  

IBM Cloud environments enabled for workshop requests today: [Custom ROKS Requests](https://techzone.ibm.com/collection/custom-roks-vmware-requests) collection

*   Managed OpenShift cluster (ROKS) in IBM Cloud (“classic infrastructure”) with NFS
*   Managed OpenShift cluster (ROKS) in IBM Cloud on VPC Gen2 infrastructure with ODF (OCS) support.

  

To request an additional IBM Cloud environment that is live on IBM Technology Zone today to allow for workshop requests, please reference the [How to enable workshop requests on an IBM Cloud environment](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/enable-ibmcloud-workshop.md) documentation to understand the request and testing process needed before enabling a new IBM Cloud workshop request option.

Question #167: What environments require approval?
Answer #167: Not all but some Premium environments tab found from the [Certified base image collection](https://techzone.ibm.com/collection/tech-zone-certified-base-images/journey-premium-aws-azure-roks): [https://techzone.ibm.com/collection/tech-zone-certified-base-images/journey-premium-aws-azure-roks](https://techzone.ibm.com/collection/tech-zone-certified-base-images/journey-premium-aws-azure-roks)

*   ROKS environments and a select set of third part cloud environments like AWS and Azure. Not all go through an approval process so reference the [approval workflow runbook](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/approval-workflow.md) on how to identify which environments require approval. These requests have a two day review process. [https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/approval-workflow.md](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/approval-workflow.md)

Additionally, all workshop request must go through approval process and details on review process can be found in the [workshop manager policies](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/reservation-duration-policy.md#workshop-manager-policies) runbook. [https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/reservation-duration-policy.md#workshop-manager-policies](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/reservation-duration-policy.md#workshop-manager-policies)

Question #168: Can I provision clusters directly on IBM Cloud?
Answer #168: No, clusters cannot be provisioned directly from IBM Cloud, you will need to select from our wide variety of [environments](https://techzone.ibm.com/environments) on IBM Technology Zone.

Question #169: How do I transfer my collection to another user?
Answer #169: Here are the steps on how to transfer a collection:

1.  Go to “My Library” tab on the top of IBM Technology Zone > Click “My created resources” from the dropdown options.
2.  Locate the collection you would like to transfer and click on the tile to navigate to the edit collection form.
3.  Scroll down to the Owner field and input the new email of the person you would like to transfer this collection to.
4.  Click "Save".
5.  Allow time for the collection fields to update through the cache layer of Technology Zone and have the new owner check their “My created resources” page to confirm the transfer was a success.

Additional questions? Contact the IBM Technology Zone support team via email: [techzone.help@ibm.com](mailto:techzone.help@ibm.com)

Question #170: How can I request multiple environments for a workshop?
Answer #170: Leverage the “Schedule a worksop” option on the “Create a reservation page”.

Go to the “Environments” tab on the IBM Technology Zone Page, Search for the required resource, click “reserve” and Schedule a Workshop

Question #171: How do I move my account over to TechZone?
Answer #171: Private accounts cannot be moved under TechZone. If you wish to retain the content, please review the process for [replicating functionality]( https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/how-to-submit-itz-enhancements.md) in TechZone.

Question #172: Are there token limits for Watsonx.ai?
Answer #172: No there are no limits, if you are hitting a limit for a TechZone reserved environment you may be pointing to a WML service in your personal IBM cloud account. Learn more in the [watsox Troubleshooting Guide runbook.](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md)

Question #173: After I was added as a workshop instructor, why don't I see it appear in "My Workshops?"
Answer #173: At this time, only the creator of the workshop can see it in the "My Workshops" section. If you are listed as an instructor, please have the creator of the workshop share the instructor link as you will still have access to this.

Question #174: After I was added as a workshop instructor, why don't I see it appear in "My Workshops?"
Answer #174: At this time, only the creator of the workshop can see it in the "My Workshops" section. If you are listed as an instructor, please have the creator of the workshop share the instructor link as you will still have access to this.

Question #175: After I was added as a workshop instructor, why don't I see it appear in "My Workshops?"
Answer #175: At this time, only the creator of the workshop can see it in the "My Workshops" section. If you are listed as an instructor, please have the creator of the workshop share the instructor link as you will still have access to this.

Question #176: After I was added as a workshop instructor, why don't I see it appear in "My Workshops?"
Answer #176: At this time, only the creator of the workshop can see it in the "My Workshops" section. If you are listed as an instructor, please have the creator of the workshop share the instructor link as you will still have access to this.

Question #177: After I was added as a workshop instructor, why don't I see it appear in "My Workshops?"
Answer #177: At this time, only the creator of the workshop can see it in the "My Workshops" section. If you are listed as an instructor, please have the creator of the workshop share the instructor link as you will still have access to this.

