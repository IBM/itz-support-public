# How Do I Share My Environment With Another User?

Share an environoment with an IBMr, a business partner, or even invite a client to access the environment. The following steps will show you how to manage your environment reservation to share with the entended user and how they will be invited to the environment per persona (IBMr, business partner, clients).

**Important - Know who you can share what infrastructure with:** 

Who (IBMrs, Business Partners, Clients) has access to certain infrasturctures?

- KVM Fyre environments can only be reserved by IBMrs at this time and due to VPN access these environments can only be shared amongst IBMrs.
- Skytap environments can be shared with IBMrs, business partners, and clients using the desktop URL to access.
- IBM Cloud (ROKS,Hosted) environments can be shared with IBMrs, business partners, and clients. Ensure that the user has accepted the IBM Cloud invite or they will not be able to access the environment. The IBM Cloud invite is an email sent to the IBMid email that the owner shared the environment with. 
- AWS and Azure can only be reserved by IBMrs at this time, but the environment can be shared with IBMrs, business partners, and clients.

## How to share

1. Log in to the portal using your IBM id
2. Go to "My Library" and click on "My reservations"

![Myreservations](Images/my%20reservations.png)

3. Find the reservation that you would like to share
4. Click on the three vertical dots menu, select Share.

**Notice:** As the reservation owner, you can share the reservation, transfer ownership of the reservation, and extend once a valid opportunity is added to the reservation.

![Share](Images/share%20feature.png)

5. Enter the IBMid to whom you want to share this environment with. If you have multiple IBMid's that you would like to share this environment with, enter each IBMid and then seperate with a comma.

- If the user that you wish to share this environment with does not have an IBMid, please send them to this [URL](https://www.ibm.com/account/reg/us-en/signup?formid=urx-19776&target=https%3A%2F%2Flogin.ibm.com%2Foidc%2Fendpoint%2Fdefault%2Fauthorize%3FqsId%3D1156c9eb-c357-471b-a524-9ae38869e775%26client_id%3DODllMDk4YzItMjgxOC00) to get started creating their IBMid. 

![Sharereservation](Images/email%20for%20share.png)

6. Click on "Share" blue button

**Important:** Once shared it can not be revoked. Only by ITZ Admins per owner request.

7. See who you have shared this environment with right from the reservation card from "My reservations" page. 

![shared with](Images/shared%20with.png)

## How IBMrs, business partners, and clients will now access the shared environment

**IBMrs and Partner that were shared an environment:** Login to IBM Technology Zone and see that a reservation was shared with them and by whom it was shared by. 

![sharee view](Images/sharee%20view.png)

**Notice:** Users who are shared an environment will not be able to share, transfer, or in some cases when an opp code is provided by the owner extend. These are all owner actions. The person that was shared the environment will only be able to view the collection of resources that are tied to this environment, view the reservation details, get support by selecting help, and delete the shared reservation from the "My reservations" page when they are finished with the environment. 

**Clients that were shared an environment:** the owner at this time will have to forward the ready email for the user to access the reservation. This is because clients do not have access to IBM Technology Zone at this time. They will have to access the direct url to access their environment and use the username and password to sign into the environment directly. 

### Support

For any questions, contact ITZ support - techzone.help@ibm.com
