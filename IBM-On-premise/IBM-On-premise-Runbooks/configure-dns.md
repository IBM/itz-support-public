
# DNS Settings
    
How to change DNS settings on your PC running Windows 10 [https://www.windowscentral.com/how-change-your-pcs-dns-settings-windows-10](https://www.windowscentral.com/how-change-your-pcs-dns-settings-windows-10)

**If you are experiencing connection issues please follow these steps.**

You can configure the DNS suffix search order on a Windows system by following these steps:


Access the properties of the network interface you wish to configure.


Double-click on "Internet Protocol (TCP/IP).


1. In the Internet Protocol (TCP/IP) Properties dialog box, click the Advanced button.
2. Click the DNS tab in the Advanced TCP/IP Settings dialog box.
3. Click the "Append these DNS suffixes (in order)" radio button.
4. Now click the Add button to add DNS suffixes to the connection.
5. In the TCP/IP Domain Suffix dialog box, enter the name of the first domain name to append to any DNS search (Example: pbm.ihost.com).
6. Repeat steps 6-7 for each additional domain.
7. When finished, click OK to close the Advanced TCP/IP Settings dialog box.
8. Click OK to close the Internet Protocol (TCP/IP) Properties dialog box.
9. Click OK to close the network connection's Properties dialog box. 

Add these suffixes:
```
 pbm.ihost.com
 cecc.ihost.com
 ibm.com
```
