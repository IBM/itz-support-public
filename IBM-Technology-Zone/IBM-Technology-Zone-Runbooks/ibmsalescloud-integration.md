# IBM Technology Zone integration with IBM Sales Cloud

The IBM Technology Zone (TechZone) integration with IBM Sales Cloud (ISC) automatically logs qualified reservations from TechZone as a Technical Sales Activity (TSA) in ISC. Continue to read through this runbook to understand the qualifying requirements from ISC side and the TechZone reservation side in order for the automatic TSA to be automatically created in ISC. 

One ISC Requirement:
1. The user making the reservation in TechZone must be a valid ISC user. Valid ISC user meaning an active ISC account holder with appropriate 'sales-role' assigned.

Three TechZone Requirements:
1. The reservation being made must have one of the following purposes selected: Customer Demo, Proof of Concept, or Proof of Technology.

![reservation purposes](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/reservationpurposes.png)

2. An ISC sales opportunity number must be provided.

3. An ISC sales opportunity product line item associated to the sales opportunity number must be selected.

![Opp_number_and_product_fields](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/oppnumberandproduct.png)

When a reservation is created, the system will automatically log a new TSA in ISC and will associate it with the opportunity number and the opportunity product provided and selected from the TechZone reservation form. Please note, there is a delay as Activities that will be loaded as part of a daily batch job. Qualifying TechZone reservations will be logged as either a Custom Demo or Proof of Value.

Supporting resources:

- [IBM Sales Cloud Knowledge Base](https://ibm.seismic.com/app?ContentId=5730eed4-2220-4a03-bff5-b47635e39904#/doccenter/5477419a-9474-4c51-94af-b442e9169fab/doc/%252Fdd98c5a3df-6b7c-1d77-6f07-d12e63954c78%252FdfOTRiYmU4NTQtNWY4NC03Y2QyLWZjYWUtOGIxYmFmZjkyZThk%252CPT0%253D%252CUm91bmR1cCBvciBzdW1tYXJ5%252Flfd5be20cb-4b40-4f42-9264-4af7af3d56cc/grid/?anchorId=cfe9d4bd-7888-4b99-8d92-0766e2b8d0b6) in Seismic. 
- Learn more about [working with Oppportunities](https://ibm.seismic.com/app?ContentId=5730eed4-2220-4a03-bff5-b47635e39904#/doccenter/5477419a-9474-4c51-94af-b442e9169fab/doc/%252Fdd98c5a3df-6b7c-1d77-6f07-d12e63954c78%252FdfOTRiYmU4NTQtNWY4NC03Y2QyLWZjYWUtOGIxYmFmZjkyZThk%252CPT0%253D%252CSG93LXRv%252Flf222d5ac8-8e11-4142-9ebf-b6a0097233ad//?mode=view&parentPath=sessionStorage) in ISC. 
- Learn more about [working with Products](https://ibm.seismic.com/app?ContentId=0612f17d-d710-46ed-bb06-6274fff2992a#/doccenter/5477419a-9474-4c51-94af-b442e9169fab/doc/%252Fdd98c5a3df-6b7c-1d77-6f07-d12e63954c78%252FdfOTRiYmU4NTQtNWY4NC03Y2QyLWZjYWUtOGIxYmFmZjkyZThk%252CPT0%253D%252CSG93LXRv%252Flff4384ac4-d25b-469f-84e2-3109fcb7817d/grid/?anchorId=334448a9-c480-4063-9d2e-e5100bd36fe4) in ISC. 
- Learn more about [working with Activities](https://ibm.seismic.com/app?ContentId=5730eed4-2220-4a03-bff5-b47635e39904#/doccenter/5477419a-9474-4c51-94af-b442e9169fab/doc/%252Fdd98c5a3df-6b7c-1d77-6f07-d12e63954c78%252FdfOTRiYmU4NTQtNWY4NC03Y2QyLWZjYWUtOGIxYmFmZjkyZThk%252CPT0%253D%252CSG93LXRv%252Flf03396212-db07-449e-97a2-483907c05dab//?mode=view&searchId=12d474f6-b612-4fbf-af1f-b4da7ec0b206&anchorId=334448a9-c480-4063-9d2e-e5100bd36fe4) in ISC. 
- [Request and manage your ISC access](https://ibm.seismic.com/app?ContentId=5730eed4-2220-4a03-bff5-b47635e39904#/doccenter/5477419a-9474-4c51-94af-b442e9169fab/doc/%252Fdd98c5a3df-6b7c-1d77-6f07-d12e63954c78%252FdfOTRiYmU4NTQtNWY4NC03Y2QyLWZjYWUtOGIxYmFmZjkyZThk%252CPT0%253D%252CSG93LXRv%252Flfb1cdddc2-1fa0-41fd-a3a0-4b0c290a24ba//?mode=view&searchId=bf35cdae-6df7-407e-9d30-5b888b696cff) supporting documentation.
