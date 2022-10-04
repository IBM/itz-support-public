# IBM On-premise

## Known limitations
- Extending a reservation is not possible: This will be addressed soon and is coming in a future release.
- Several resources within a same network: If you need more than 1 resource and they need to be able to communicate with each other, please book one or two days in the future and open a support ticket with a list of the reservation ids requesting they be placed in the same project. Project support will be available in IBM Technology Zone soon, but is being handled manually in the interm.
- SSH key: Injecting your own SSH key into the OS is currently disabled though we hope to bring this feature back at some point. In the meantime you can use the auto-generated project key.


## Self-service runtime actions currently not available
- Add a second disk after the creation: A workaround is to cancel your current reservation and add a second disk during the booking process. Otherwise please open a support ticket.
- Add shared storage: Please open a support ticket.
- Add VPN access or add more VPN IDs: Please open a support ticket.
- Hard reboot a server or VM: If you are unable to run shutdown -r yourself then please open a support ticket.
- Rebuild a server or VM without a full reprovision: Please open a support ticket.     

## Withdrawn features
- Persistent file storage, centralized Active Directory accounts, and post provision user install hooks are withdrawn and no longer available.

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
