# Add Environment variables/values to your Collection
This runbook will guide you through how to build your vm-map-string for your VMware Environment on IBM Cloud infrastructure. <br>

### Prerequisites
1. Need a Collection created beforehand, view the How to Create a Collection Runbook for more information on how to create a collection:

https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/techzone-content.md#how-to-create-a-collection <br>

2. Need to gather the following information from the Content author:

   hostname, IP addresses, VM startup order for the stage number, subnet, router IP, domain name, published ports (if needed)

### 1. Build your vm-map-string for your Environment
1. Use a text editor to view the provided Json stub file from TechZone Support (for example: TET-LABNUM-vm-map-string.json) <br>
![VMMAPSTRING1](https://media.github.ibm.com/user/334015/files/14d8a239-8d0e-4b6d-a019-0765707e344c) <br>

2. Open the Jsonformatter Web tool on the Internet<br>
https://www.jsonformatter.io/ <br>

3. In the left pane, Paste the contents of TechZone provided Json stub file <br>
![VMMAPSTRING2](https://media.github.ibm.com/user/334015/files/2e48ebb3-a6ad-4ba9-9b1a-a8c6383a450e) <br>

4.In the left pane, for each VM template:  add the VM hostname and IP address (in between double quotes), update the stage number for startup order, add port number (if needed). <br>
![VMMAPSTRING3](https://media.github.ibm.com/user/334015/files/ecdc019c-0215-4e24-8f88-da7f9eebb5cc) <br>

5. In the right pane, click on "Minify" to convert Json to a single line <br>
![VMMAPSTRING4](https://media.github.ibm.com/user/334015/files/cefddea7-72c2-4449-922c-c31fa8400cb7) <br>

6. In the right pane, click "Copy" to copy the Minified vm-map-string  to be pasted later in step below to the Collection vm-map-string value field <br>
![VMMAPSTRING5](https://media.github.ibm.com/user/334015/files/2642853e-5d50-4b3e-b8dd-3ec9249fdd81) <br>

 

### 2. **To test your migration **Create Techzone environment**, please create your own collection beforehand and follow steps below. <br>
1. Open your Collection URL created beforehand: https://techzone.ibm.com/collection/YOURCOLLECTION <br>

2. Click "Edit" for your the Collection <br>
![EditCollection1](https://media.github.ibm.com/user/334015/files/caed1922-2ab7-456d-b79e-fad2a89fc0e2) <br>

3. Scroll down to the "Environment".<br>
- If new, Click "Add an environment" <br>
- If existing, click on the pencil icon on left to edit <br>
![EditCollection2](https://media.github.ibm.com/user/334015/files/4da19d2c-bb6e-4f12-8831-8585d3ebebed)

4. For GitOps Pattern, use Pulldown menu to select vmware-template <br>
  and For Settings, use Pulldown menus to select Account Pool, Cloud Account, Geo, Region, Datacenter<br>
![EditCollection3](https://media.github.ibm.com/user/334015/files/c89aa560-81eb-481b-b1c4-47c8f539a0da)  <br>

5. Add the netework information provided by TechZone Support and paste the vm-map-string created in Step 1. <br>
NOTE: See Below for description of the variables. <br>

![EditCollection4](https://media.github.ibm.com/user/334015/files/c5947175-56e4-4ba7-8bd7-bef13e45cdbe) <br>

6. Click "Save" to save the Environment<br>

7. Scroll to bottom and Click "Save" to save the Collection Updates<br>
![EditCollection5](https://media.github.ibm.com/user/334015/files/e0ffa87a-aa72-484f-b53f-c88627ca3f6b) <br>


### VARIABLE DESCRIPTION: <br>
Default Variables required:<br>
- Infrastructure - where to deployed. For example "IBM Cloud"<br>
- GitOps Patterns - Provisioning instructions - Select "vmware-template"<br>
- Account pool - Location - Select the different locations (itzvmware), Cloud Account (itzvmware), Geo (Americas), Region (us-east), Datacenter (wdc04)<br>
- vm_template_folder - parent folder name. For example "templates-shared"<br>
- vm_template_id- the template folder name for the VMs<br>
- vm_map_string - values for the VMs - make sure your VM Map string is correct, you can use any JSON validators like https://jsonlint.com/) <br>
- vm_domain - Network domain for the VM<br>
- vm_router_ip - Router for the VM<br>
- vm_subnet - Subnet for the VM<br>

Note: If you do not have custom Network requirements, use the defaults values below for the Network details:<br>
Default vm_domain value is ibmdte.net<br>
Default vm_router_ip value is 10.0.0.254<br>
Default vm_subnet value is 10.0.0.0/24<br>

Example of a vm_map_string: <br>
{ 	"GKLM41-20230105": { 		"ip": "10.0.0.1", 		"hostname": "host-1", 		"stage": 1 	} }<br>

"GKLM41-20230105" - Template file name<br>
"ip": "10.0.0.1" - IP address for the VM<br>
"hostname": "host-1" - Hostname for the VM<br>
"stage": 1 - create and launch first (order to create a VM which has no dependency)<br>
"stage": 2 - Optional if have more than 1 VM and there are dependencies: create and launch second (create after stage 1 has been created - dependent on stage 1 creation)<br>
"stage": 3 - Optional if have more than 1 VM and there are dependencies: create and launch third (create after stage 2 has been created - dependent on stage 2 creation)<br>

### Published Services variables (if adding ports to be exposed as publish services, add port variable to the vm_map_string):<br>
https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/VMwarePublishedServices.md<br>
