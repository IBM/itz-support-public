## VMware WireGuard VPN Access

The WireGuard VPN tunnel allows users to access their VMs in an isolated environment network.![image](https://media.github.ibm.com/user/408676/files/64f0c210-a26a-4a79-9195-06f6071be549)
![image](https://media.github.ibm.com/user/408676/files/7808612d-11f7-4643-a660-fe2255dbf4ea)


![VPN](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/vmware-vpn.png)

1. Enable VPN Access in the reservation form

![VPN](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/vmware-vpn-reserve.png)

2. Once the reservation has been completed, verify that Public VPN Endpoint is enabled, and download its Wireguard VPN config file

![VPN](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/vmware-vpn-download.png)

3. Download and install the WireGuard VPN client on your local machine.
See https://www.wireguard.com/install/ for its various OS instructions

4. Launch the client. Import your downloaded VPN config file

![VPN](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/vmware-vpn-import.png)

![VPN](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/vmware-vpn-import2.png)

5. Activate connection

![VPN](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/vmware-vpn-activate.png)

6. Once the VPN connection has been activated, verify its status
![VPN](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/vmware-vpn-activated.png)

7. Open your terminal and ping the VPN gateway `192.168.253.1` to test its connection

![VPN](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/vmware-vpn-test.png)

The VPN connection is established.

### Support

For any questions, contact ITZ support: techzone.help@ibm.com
