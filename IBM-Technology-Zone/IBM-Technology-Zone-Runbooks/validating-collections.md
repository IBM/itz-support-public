## How to Verify Validaiton Runs Against a Collection

1. Log in to Techzone
2. Navigate to the collection in question via https://techzone.ibm.com/collection/<id> or https://techzone.ibm.com/collection/<slug>
  
3. Click the ellipses and click the "Validation" selection
  
![image](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/validatingcollections1.png)
  
4. a table opens showing the current validations run against that collection 
  
## Understanding Validations

![image](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/validatingcollections2.png)

- Current validations run once a week on Mondays.

- Some active collections may not have validations because they meet all criteria and never have been invalidated
- Some validations can run multiple times and have a higher `attempt` number
- Some validations can have a value of Zero. If a collection had invalid criteria (ie needs to be updated) then it was updated. The attempts then go to zero
- Some validations can have criteria that is valid and some that are invalid. (ie valid owner but the updated date is too far in the past)

Breaking down the above picture from bottom to top.

  **Rule: validateOwner attempt 0**

  This rule validates against the techzone auth service if a user is still in our system. if not it increments by one and contacts the colloborators. If a collaborator is not valid or available it is auto-retired

**Rule: validateUpdateAt attempt 5**

  This rule checks the `updatedAt` variable in the collection model and determines if its too old. if So the `attempt` is incremented and the owner is contacted via email
  
**Rule validateUpdateAtEscalationCollaborators attempt 3.** 
  
  This rule is an escalation rule of the previous rule `validateUpdateAt` it contacts the collaborators after trying to contact the owner to update the collection
  
**Rule validateUpdateAtEscalationExpire attempt 1**

  This rule is another escalation on `validateUpdateAt` it finally retires the collection as no action has been taken on the Owner or the collaborators
  
  
## Why was my collection retired ?
- collection can be auto retired by multiple validations. 
1. the collection hasnt been updated in awhile after 180 days (this can change)
How Do I fix it ? ---> update the collection data by adding/changing anything in the `Collection Edit` screen
2. there wasn't a valid owner/collaborator combination found
How Do I fix it ? ---> Add a valid owner (ie and email that is know to techzone via the `user` panel)
