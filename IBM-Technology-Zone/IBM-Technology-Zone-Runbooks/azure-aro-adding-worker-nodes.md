# Azure ARO Adding Worker Nodes

Users should be able to do this on their own as they have kubeadmin access to the cluster.

TBD: Should this runbook be in the public runbooks repository?

# Step-by-step

1. Log into the OCP console as admin.

2. In the left-hand navigation pane, open `Compute` and select `MachineSets`.

3. You should see 3 machinesets. (Each machineset is configured for a separate zone.) (See figure below.)

![OpenShift Cluster machinesets for an ARO cluster](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/azure-aro-machinesets.png))

4. Edit the number of machines for each machineset to increase the number by a third of the total number of machines to be added.
  - You can click on the machineset
  - Or select `Edit MachineSet` in the 3-dots menu at the right.
  - If you get to the YAML view in the machineset, click on `Details` to get a more user friendly view.

5. Under `Desired count`, click the edit icon (pencil) to modify the number of machines. (See figure below.)

![OpenShift Cluster machineset Edit Desired Count](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/azure-aro-edit-machineset-desired-count.png)

6. In the popup editor increase the desired machine count appropriately and click Save. (See figure below.)
  - Only increase the count for each machineset by 1/3 of the total number of machines to be added.
  - For example, if adding 3 new nodes, then increase each machineset "desired count" by 1.

![OpenShift Cluster machineset increase Desired Count](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/azure-aro-machineset-increase-desired-count.png)

7. Repeat for each machineset.

### Support

For any questions, contact ITZ support - techzone.help@ibm.com
