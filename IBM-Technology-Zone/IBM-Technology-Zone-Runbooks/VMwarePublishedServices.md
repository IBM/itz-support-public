## VMware Published Services

Published Services allow users to expose TCP/UDP ports on VM to the Internet. 
They are commonly used to access a VM via SSH or direct RDP, or to access web or application services running on a VM.

![svc](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/vmware-public-svc.png)

**NOTE: You must configure the VM guest operating system and applications running on the VM to accept the remote connection**

### Environment Configuration
1. Set `ports` field in `vm_map_string`. 
Its format is `"ports": ["<port_number>/<protocol>", …]`
TCP and UDP protocols are supported

![svc](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/vmware-public-svc-map.png)

2. Add Link patterns – map VM’s internal IP:port with a link template

![svc](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/vmware-public-links.png)

### Reservation
Reserve the new environment. Once completed, verify published services links for your exposed web-services in a browser

![svc](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/vmware-public-reservation.png)

If you exposed the remote access services (RDP, VNC, or SSH), verify its direct connection with a client.
E.g. open MS Remote Desktop client and add the published service RDP link

![svc](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/vmware-public-rdp.png)

Enter your RDP credentials
(https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/vmware-public-rdp2.png)

### Support

For any questions, contact ITZ support: techzone.help@ibm.com
