# VMWare Console Access Enhancement

How to enable Console Access
## Parity Map

-	All cloud providers have similar console access features with some exceptions
-	Compare vmware with other environments
-	Vmware – advanced self-service option – environment owners can choose to enable this feature or not.

![ConsoleAccess](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/Consoleaccess1.png)

## Console key features
-	vSphere Web Client via Remote Desktop Gateway
-	Advanced full environment control: Control power state, suspend, host other vms etc
-	Direct access to virtualized hardware: Change any hardware, network adapters etc
-	Utilization Monitoring: View what the consumption (CPU, memory, storage) for the environment is
-	Clone running ‘live’ environments to a new template
-	VM Template Development, Testing, and Debugging

## How to Enable Console Access

To enable console access, there are a few variables that must be set up.

## Techzone Environment Definition

Specify which bastion will be used (sidecar vm to attach to environment?)

- Set required `console_enable` to `true`
- Set optional `vm_bastion_template` if you need to use a custom template for your bastion VM
- Set required `bastion_ip`. Make sure it belongs to your defined `vm_subnet` and is out of DHCP range `vm_dhcp_range`

![ConsoleAccess2](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/Consoleaccess2.png)

## Connect to vSphere Console via VDI and VPN.

Advanced Access:

- Click the Bastion remote access desktop link to gain advanced access to the infrastructure 
OR
- Click the "Download Wireguard VPN Config.
- Use your vCenter credentials if vSphere console needed.


Regular Access:

Use buttons under "VM Remote Console" to access your provisioned VMs.

![ConsoleAccess3](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/Consoleaccess3.png)

### Support

For any questions, contact ITZ support - techzone.help@ibm.com
