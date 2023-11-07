# How to Build your `vm-map-string`
This runbook will guide you through how to build your vm-map-string for your VMware Environment on IBM Cloud infrastructure. <br>

### Getting Started

1. Before building your `vm-map-string` you need a TechZone Collection, please view the [How to Create a Collection Runbook](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/techzone-content.md#how-to-create-a-collection) for more information on how to create a collection.

2. If you own an environment that was used at a TechXchange event and you would like to have migrated so others can make a reservation directly on TechZone, please view the [Techxchange Migration Process Runbook](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/techxchange-migration-process.md) before continuing.

3. Gather the following information about the environment:

   - hostname, IP addresses, VM startup order for the stage number, subnet, router IP, domain name, published ports (if needed)

### How to Build your `vm-map-string` for your Environment

1. Use a text editor to view the provided Json stub file from TechZone Support (for example: `TET-LABNUM-vm-map-string.json`) 

![VMMAPSTRING1](https://media.github.ibm.com/user/334015/files/14d8a239-8d0e-4b6d-a019-0765707e344c)

2. Open the Jsonformatter Web tool on the Internet

   - https://www.jsonformatter.io/

3. In the left pane, Paste the contents of TechZone provided Json stub file

![VMMAPSTRING2](https://media.github.ibm.com/user/334015/files/2e48ebb3-a6ad-4ba9-9b1a-a8c6383a450e)

4. In the left pane, for each VM template:  add the VM hostname and IP address (in between double quotes), update the stage number for startup order, add port number (if needed). <br>

![VMMAPSTRING3](https://media.github.ibm.com/user/334015/files/ecdc019c-0215-4e24-8f88-da7f9eebb5cc)

5. In the right pane, click on "Minify" to convert Json to a single line 

![VMMAPSTRING4](https://media.github.ibm.com/user/334015/files/cefddea7-72c2-4449-922c-c31fa8400cb7)

6. In the right pane, click "Copy" to copy the Minified vm-map-string  to be pasted later in step below to the Collection vm-map-string value field <br>

![VMMAPSTRING5](https://media.github.ibm.com/user/334015/files/2642853e-5d50-4b3e-b8dd-3ec9249fdd81)
