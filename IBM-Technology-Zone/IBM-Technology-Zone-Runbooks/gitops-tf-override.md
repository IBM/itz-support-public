# GitOps/Terraform Environment Variables

## Details 

The GitOps provisioner allows users to override default values in its Terraform patterns. Users can customize environments without altering the pattern's source code

### How to create and customize GitOps environments

Once your pattern is onboarded, you can create a new environment from it.

1. Open your collection and click `Edit` button
2. Scroll down to its `Environments` section
3. Click `Add an environment` or edit the existing one
4. Choose the required infrastructure*
5. Fill out title and description fields
6. Choose your pattern from drop-down list in `Regions` section. The pattern name should match your pattern subfolder in Git
7. Select and add the proper `Region` and `Cloud Account`. If you are not sure about the correct accounts, please contact the Techzone Support. Some accounts and regions do not have capabilities of provisioning particular resources
8. If you need to customize the pattern configuration, add variables from drop-down list in `Terraform Variables Overriding` section. The drop-down list will be auto populated with all variables from Terraform *.tf config files which are available for changings. It will show name, description, type, and default value of the selected variable.
9. Click `Save`

![GitOps environment](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/gitops-env.png)




*- GitOps based: IBM Cloud, AWS, and Azure

### Support

For any questions, contact DTE support.

Business Partners - Contact DTE Support - techzone.help@ibm.com

IBMers - Make a post on the [#itz-techzone-support](https://ibm-itz.slack.com/archives/C0124J683GW) slack channel.
