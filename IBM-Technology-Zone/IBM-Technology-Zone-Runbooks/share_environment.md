# Summary
The purpose of this runbook is to showcase how an IBM Technology Zone reservation can be shared with another IBM Technology Zone user. When attepting to share a reservation, the user should consider the type of environment (vmware, IBM Cloud, AWS, Azure, Fyre) they are trying to share the and the type of user (Business Partener or IBM employee) whom they want to share the environment with prior to attempting to share it. In order to share a reservation navigate in the IBM Technology Portal to the "My Library" section at the top of the website and click on "My reservations". Choose the reservation which you would like to be share and then expand the three vertical dots menu by clicking on it. After that select the option "Share". A modal will apear in which the IBM IDs of those users whom this environment should be shared with can be listed sperated by comma. Once that is completed, click the blue "Share" button. 

IMPORTANT: Please note this is a summary of the steps, for edge cases and expections review the whole document at: https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/share_environment.md


# How do I share my environment in the IBM Technology Zone Platform with another user?

Share an environoment with an IBMr, a business partner, or even invite a client to access the environment. The following steps will show you how to manage your environment reservation to share with the entended user and how they will be invited to the environment per persona (IBMr, business partner, clients). Continuing reading below to understand the rules of who can reserve each environment by infrastructure and which persona the environment can be shared with. 

**IBM Cloud** - IBM Cloud environments (this includes ROKS, Hosted, SaaS, and VMWare on IBM Cloud options) can be reserved by IBMrs and Business Partners and can be shared amongst IBMrs, Business Partners, and Clients. Ensure that the tagret user has accepted the IBM Cloud invite or they will not be able to access the environment that being shared. The IBM Cloud invite is an email sent to the IBMid email that the owner shared the environment with. 

_**IMPORTANT: IBM Technology Zone user that you are sharing an IBM Cloud environment with (IBMer, Business Partner, and/or client) must have an IBMid for you to share access to the environment.**_

**AWS and Azure** - AWS and Azure environments on IBM Technology Zone Platform can be reserved by IBMrs and Business Partners and can be shared with other IBMrs, Business Partners, and Clients following the regular steps. 
 
**Fyre** - Fyre environments on IBM Technology Zone can ONLY be reserved by IBMers at this time due to VPN access. These environments are only accessible to IBMers so they can not be shared with any other user at this time. 

## Before you share

Ensure that the user that you wish to share this environment with has an IBMid. Please send them to this [URL](https://www.ibm.com/account/reg/us-en/signup?formid=urx-19776&target=https%3A%2F%2Flogin.ibm.com%2Foidc%2Fendpoint%2Fdefault%2Fauthorize%3FqsId%3D1156c9eb-c357-471b-a524-9ae38869e775%26client_id%3DODllMDk4YzItMjgxOC00) to get started creating their IBMid. 

Cannot access URL? Alt url: https://www.ibm.com/account/reg/us-en/signup?formid=urx-19776&target=https%3A%2F%2Flogin.ibm.com%2Foidc%2Fendpoint%2Fdefault%2Fauthorize%3FqsId%3D1156c9eb-c357-471b-a524-9ae38869e775%26client_id%3DODllMDk4YzItMjgxOC00

**IMPORTANT:** Users that create an IBMid do NOT need an IBM Cloud account to accept an invite to the shared environment. As long as the user you are sharing with has an IBMid, they will receieve the email invite as shown in the process below. No IBM Cloud account is needed to share an invite to the reserved environment. This process also allows you as the owner of the reservation trying to share with a client the ability to bypass the IBM Cloud account creation process as TechZone will send an email invite to the users IBMid email without the need to create an IBM Cloud account.


## How to share

1. Log in to the portal using your IBM id
2. Go to "My Library" and click on "My reservations"

![Myreservations](Images/my%20reservations.png)

3. Find the reservation that you would like to share
4. Click on the three vertical dots menu, select Share.

As the reservation owner, you can share the reservation, transfer ownership of the reservation, and extend once a valid opportunity is added to the reservation.

![Share](Images/share%20feature.png)

5. Enter the IBMid to whom you want to share this environment with. If you have multiple IBMid's that you would like to share this environment with, enter each IBMid and then seperate with a comma.

![Sharereservation](Images/email%20for%20share.png)

6. Click on "Share" blue button.

7. An email will then be sent to the user that you shared the environment with. Access credentials included in the email. 

![shared with](https://github.com/IBM/itz-support-public/blob/43f3d35125c666a2e346a60e3cf90b0885b351ef/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/shared%20with.png)

**Important:** Once shared it can not be revoked. Only by ITZ Admins per owner request.

## Users experience that has been shared a reservation

An email will then be sent to the user that you shared the environment with. See below for a blank email template example of what the user will receive in their email. 

![shared template](https://github.com/IBM/itz-support-public/blob/51fda870b998856c006c1cd9a1ad8d95a948cb6b/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/Blank%20shared%20email.png)

IBMrs and Partners that you shared the environment with will be able to login to IBM Technology Zone and see a reservation card on their "My reservations" page. The shared environment will have **(Shared)** notation next to their status field.

![sharee view](https://github.com/IBM/itz-support-public/blob/51fda870b998856c006c1cd9a1ad8d95a948cb6b/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/sharee%20view.png)

**IMPORTANT:** Users that are shared a reserved environment on TechZone will not be able to extend, share, or transfer the reserved environment. The owner of the shared reservation that initially shared the reserved environment can field these requests and perform these actions as needed. The shared reservation owner will however be able to delete their shared reservation. This will not delete the parent reservation. Deleting a shared reservation will remove the reservation from the users My reservations page and there is no impact to the original owners reservation record. 

## Keywords
Sharing, Reservation, IBM Technology Zone Portal, Step-by-Step guide

### Support

For any questions, contact ITZ support - techzone.help@ibm.com
