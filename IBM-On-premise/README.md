# IBM On-premise

## Known limitations

- Inability to book serveral resources together so they provision on the same network. If you need this capability please book one or two days in the future and open a support ticket with a list of the reservation ids requesting they be placed in the same project so they provision on the same subnet. Please note that this functionality is only supported for on-premise reservations and not PowerVS, and generally only works with simple reservations that combine single VM's.
- The ability to inject your own SSH key into the OS during provisioning is currently not available.


## Actions available that require a Help Desk ticket

These are generally only available for on-premise provisions:
  
- Adding additional storage to a specific PowerVM based VM.
- Adding shared storage to all the PowerVM based VM's in a project.
- Adding VPN access or adding additional VPN IDs.
- Hard rebooting a server or VM if for some reason you are unable to run sudo shutdown -r yourself.
- Rebuild a server or VM keeping the same reservation and subnet assignment.

To get help, please open a ticket to [our support team](https://techzone.ibm.com/help)

## HOW-TOs

[Configure the VPN connection](IBM-On-premise-Runbooks/configure-vpn.md)

[Configure the second disk](IBM-On-premise-Runbooks/configure-second-disk.md)

[Access AIX automounted repositories](IBM-On-premise-Runbooks/access-aix-repos.md)

[Windows DNS search order configuration](IBM-On-premise-Runbooks/configure-dns.md)

[OpenShift offering information](IBM-On-premise-Runbooks/openshift.md)
    
[IBM z/OS offering information](IBM-On-premise-Runbooks/ibm-zos.md)

[IBM Spectrum Discover offering information](IBM-On-premise-Runbooks/spectrum-discover.md)

[Connecting to IBM i PowerVS systems](IBM-On-premise-Runbooks/connecting-to-ibmi.md)
    
## Maintenance

The IBM Technology Zone On-premise Systems Infrastructure team will attempt to notify customers about both scheduled and unscheduled service interruptions when possible.

The standard Maintenance Schedule is between 6 AM to 10 AM ET on the 1st and 3rd Monday of every month excluding US holidays. It may sometimes run later than 10 AM depending on the work being performed.

## FAQ

[Check our FAQ](IBM-On-premise-Runbooks/faq.md)
