# How do I Share my Environment with Another User?

Share an environoment with an IBMr, a business partner, or even invite a client to access the environment. The following steps will show you how to manage your environment reservation to share with the entended user and how they will be invited to the environment per persona (IBMr, business partner, clients).

**Important - Know who can reserve each infrastructure and who you can share with:**
 
- Skytap environments: Reserved by IBMrs and Business Partners and can be shared amongst IBMrs, Business Partners, and Clients. 
- IBM Cloud environments (this includes ROKS, Hosted, SaaS options): Reserved by IBMrs and Business Partners and can be shared amongst IBMrs, Business Partners, and Clients. Ensure that the user has accepted the IBM Cloud invite or they will not be able to access the environment. The IBM Cloud invite is an email sent to the IBMid email that the owner shared the environment with. 
- AWS and Azure environments: Reserved by IBMrs and Business Partners and can be shared amongst IBMrs, Business Partners, and Clients. 
- Fyre environments: Reserved ONLY by IBMrs at this time due to VPN access. Can ONLY be shared amongst IBMrs at this time.


## How to share

1. Log in to the portal using your IBM id
2. Go to "My Library" and click on "My reservations"

![Myreservations](Images/my%20reservations.png)

3. Find the reservation that you would like to share
4. Click on the three vertical dots menu, select Share.

As the reservation owner, you can share the reservation, transfer ownership of the reservation, and extend once a valid opportunity is added to the reservation.

![Share](Images/share%20feature.png)

5. Enter the IBMid to whom you want to share this environment with. If you have multiple IBMid's that you would like to share this environment with, enter each IBMid and then seperate with a comma.

- If the user that you wish to share this environment with does not have an IBMid, please send them to this [URL](https://www.ibm.com/account/reg/us-en/signup?formid=urx-19776&target=https%3A%2F%2Flogin.ibm.com%2Foidc%2Fendpoint%2Fdefault%2Fauthorize%3FqsId%3D1156c9eb-c357-471b-a524-9ae38869e775%26client_id%3DODllMDk4YzItMjgxOC00) to get started creating their IBMid. 

![Sharereservation](Images/email%20for%20share.png)

6. Click on "Share" blue button.

**Important:** Once shared it can not be revoked. Only by ITZ Admins per owner request.

7. An email will then be sent to the user that you shared the environment with. Access credentials included in the email. 

**Important:** Not all environments trigger a shared email at this time. Shared emails will be sent with all IBM Cloud, Hosted, SaaS, AWS, and Azure environment reservations. The IBM Technology Zone team is working to integrate the Skytap, Fyre, and ROKS pipeline to have this same capability, but it is not available at this time. 

![shared template](Images/shared%20template.png)

IBMrs and Partners that you shared the environment with will be able to login to IBM Technology Zone and see a reservation card on their "My reservations" page. The shared environment will have **(Shared)** next to their status field. Users that are shared the environment will not be able to extend, share, or transfer the environment. These actions are owner actions and the user that was shared the environment will need to reach out to the owner to request these actions. 

![sharee view](Images/sharee%20view.png)

8. See who all you have shared this environment with right from the reservation card from "My reservations" page. 

![shared with](Images/shared%20with.png)


### Support

For any questions, contact ITZ support - techzone.help@ibm.com
