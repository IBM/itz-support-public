# Template an IBM Cloud Classic or VPC VM for Your Collection  

1.  Got to https://techzone.ibm.com/my/reservations  

2.  Select the 3 Dots Icon on your IBM Cloud reservation that will be templated  

3.  Select "Template to Collection"  
![Select template to collection](Images/template-to-collection.png)  

4.  Select the Collection this new Template will be used for  
![Select template collection](Images/select-template-collection.png)  
  
5.  Select "Template" in the bottom right  
![select template to finish](Images/select-template-to-finish.png)  

6.  When the Templating process is complete, you will receive an email.  For VPC VMs, you must power-on your VM again manually using the IBM Cloud console (reservatio. desktop url) since it was shutdown for the templating process.
![sample self template email](Images/sample-self-template-email.png)  

7.  You can now edit your collection, and see the environmnet available, but disabled, select the pencil icon to edit it  
![your new environment in your collection](Images/your-new-environment-in-your-collection.png)  

8.  Edit your Environment and update any missing information, set the status to "Active".  Take careful note of the image_id or image_name (a number for Classic, a name for VPC ).  After editting and saving, please re-edit the environment to be sure your changes were saved.  
![edit-your-environment-with-new-options](Images/edit-your-environment-with-new-options.png)  

9. The environment will now be available to provision on your environment (A [Cache Update](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/cache-update.md) may be required to see the saved changes)  
![new self template ready as env](Images/new-self-template-ready-as-env.png)  

### Support

For any questions, contact ITZ support - techzone.help@ibm.com
