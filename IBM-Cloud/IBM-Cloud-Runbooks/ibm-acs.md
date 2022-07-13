# Connect to IBM i in the cloud with Access Client Solution

By default, not all the ports are opened on IBM Cloud firewall to connect to the IBM i partition. Port 23 that allows you to open a 5250 session to your IBM i partiiton is NOT opened.
You can visit this page [https://cloud.ibm.com/docs/power-iaas?topic=power-iaas-network-security](https://cloud.ibm.com/docs/power-iaas?topic=power-iaas-network-security) to have more information about the list of opened ports.



To connect to your IBM i partition, you must 
- configure a SSH tunnel to redirect local ports from your local machine to remote ports of your IBM i system.
- configure Access Client Solution (ACS) to use your local port


## Configure the SSH tunnel

Opening a SSH tunnel is different if you run on a Windows or Linux/Mac OS machine. Choose the right method below.

### Configure the SSH tunnel on a Windows machine

1. Install [PuTTY](https://www.putty.org/) onto your system including PuTTYgen to manipulate SSH keys.

2. Save the project SSH private key into a file on your laptop using Notepad or Notepad++ (not MS Word or OpenOffice). You can name this file `private-key.txt`. To help you identify the private key, it starts with `-----BEGIN RSA PRIVATE KEY-----`

![](images/privatekey-notepad.png)

3. Convert the SSH key into a compatible PuTTY SSH key. Open PuTTYGen. Open menu Convertions -> Import Key and open the file `private-key.txt` you just saved.

![](images/puttygen-import.png)

4. Save the Putty private key using button *Save Private Key* and confirm that you save it WITHOUT a passphrase. You can name the file `putty-private-key.ppk`. You can then close PuTTYGen.

5. Open PuTTY and configure the IP address/Hostname. Make sure you use the public *external IP address*.

![](images/putty-session.png)

6.

### Configure the SSH tunnel on a Linux/Windows machine

- 
Read IBM Cloud official documentation here https://cloud.ibm.com/docs/power-iaas?topic=power-iaas-connect-ibmi to get the right procedure.
Warning: At the beginning of the page, you are requested to start SSH server issuing STRTCPSVR SERVER(*SSHD) from the console. Skip this task as SSHD is started automatically at IPL.
You can also skip the paragraph "Starting the TCP servers" as they also start at IPL automatically.

By default, for security purpose, we disabled SSH authentication with password, so you must use SSH key authentication.

This will let you open a 5250 session using your loopback IP address (127.0.0.1 or localhost) and port 50000 automatically redirected to the port 23 of your remote IBM i partition. 

## AIX 7.1

`/cecc/repos/aix71`

`/cecc/repos/lpp`

## AIX 7.2

`/cecc/repos/aix72`

`/cecc/repos/lpp`

Example: 
```shell
cecuser@p1304-pvm1:/cecc/repos/aix72 $ ls
TL3                   TL4                   expansion_pack_92018  license
cecuser@p1304-pvm1:/cecc/repos/aix72 $ cd TL4
cecuser@p1304-pvm1:/cecc/repos/aix72/TL4 $ ls
BASE  SP1   SP2
cecuser@p1304-pvm1:/cecc/repos/aix72 $ cd /cecc/repos/lpp
cecuser@p1304-pvm1:/cecc/repos/lpp $ ls
XLC
```

## AIX 7.3

`/cecc/repos/aix73`

`/cecc/repos/lpp`