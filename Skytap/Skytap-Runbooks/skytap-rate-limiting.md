# What is Rate Limiting?

## Rate limiting is not an error. Rate limiting is an intentional and expected behavior when the system is busy. The bigger the environment, the more likely it is going to happen

![rate-limiting-image](https://github.com/IBM/itz-support-public/blob/main/Skytap/Skytap-Runbooks/Images/rate-limiting.png)

Rate limiting within Skytap is a queueing system in which an API call (such as start/stop/suspend/shutdown Environment) is sent to the Skytap hypervisor (ESXi) and algorithmically measured to determine the overall impact that call might have on the underlying infrastructure. The "rate limited" message you'll see occasionally is specifically when our infrastructure has determined that, given the magnitude of the VM and its resource cost to invoke against it, its action is placed in a queue until other actions that are happening in parallel are completed.

To prevent this, please start/stop/suspend/shutdown your Environment ahead of time.

In case of emergency


Business Partners - Contact DTE Support - itz@us.ibm.com, Provide your Environment Name or ID in the email.

IBMers - Make a post on the [#itz-techzone-support](https://ibm-itz.slack.com/archives/C0124J683GW) slack channel, Provide your Environment Name or ID in the post.
