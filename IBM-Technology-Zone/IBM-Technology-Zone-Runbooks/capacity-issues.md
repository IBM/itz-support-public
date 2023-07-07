# Ongoing Capacity Challenges

## Failures for customer-facing workloads

We have implemented intelligent workload placement for customer-facing workloads (ref: old announcement) and are still seeing capacity limitations on the newly segregated infrastructure dedicated for these customer activities.  

Regardless of the datacenter choice, we are querying capacity against several datacenters at the time of the reservation. 

We either leverage the chosen datacenter, re-route to a datacenter with capacity, or fail the reservation if no capacity exists. 

In the latter case, the failure is immediate, and the reservation will show under “My reservations” when enabling the “failed” status in the filter.

![capacity-issues](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/capacity-issues1.png)

The error message will show capacity challenges, although an email notification of the failure may not occur.

Given the dynamic nature of reservations, often waiting, and trying a new reservation at a later time is the best mitigation.  

We will be exposing capacity at a future time to allow better visibility, but this is not immediately available today.


Non-customer-facing workloads (those without opportunity codes) are not impacted and will attempt to provision based on datacenter choice at time of reservation whether capacity exists or not.

## Capacity Build Out

We continue to stand up additional infrastructure to dedicate to customer-facing workloads as fast as the hardware can be racked and stacked across various datacenters and geos.  We appreciate your patience as we work to scale to unprecedented 75% growth month-on-month.

## Support Volumes

Given the on-going challenges with capacity, we are experiencing higher than normal case volumes. 

Rest assured, all tickets are worked in the order they are received and with severity considered. Customer-facing workloads are given priority.  


We have seen several template issues recently and are addressing these at the source (template replication). 

It is important to communicate with support re: specific regional availability for your contributed content templates. 

Please leverage https://techzone.ibm.com/collection/onboarding/journey-share-your-content for more information.

  
