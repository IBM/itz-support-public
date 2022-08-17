# Connecting to IBM i hosted in IBM Cloud with Access Client Solution

By default, not all the ports are opened on IBM Cloud firewall to connect to the IBM i partition. Port 23 that allows you to open a 5250 session to your IBM i partiiton is NOT opened.
You can visit this page [https://cloud.ibm.com/docs/power-iaas?topic=power-iaas-network-security](https://cloud.ibm.com/docs/power-iaas?topic=power-iaas-network-security) to have more information about the list of opened ports.


To connect to your IBM i partition, you must:
- configure an SSH tunnel to redirect local ports from your local machine to remote ports of your IBM i system.
- configure Access Client Solution (ACS) to use your local ports


## Configuring the SSH tunnel

Opening a SSH tunnel is different if you run on a Windows or Linux/Mac OS machine. Choose the right method below.

### Configuring the SSH tunnel on a Windows machine

1. Install [PuTTY](https://www.putty.org/) onto your system including PuTTYgen to manipulate SSH keys.

2. Save the project SSH private key into a file on your laptop using Notepad or Notepad++ (do not use MS Word or OpenOffice). You can name this file `private-key.txt`. The private SSH key is provided through the project kit or directly within your TechZone reservation page details. To help you identify the private key, it starts with `-----BEGIN RSA PRIVATE KEY-----`

![](images/privatekey-notepad.png)

3. Convert the SSH key into a compatible PuTTY SSH key. Open PuTTYGen. Open menu Convertions -> Import Key and open the file `private-key.txt` you just saved.

![](images/puttygen-import.png)

4. Save the Putty private key using button **Save Private Key** and confirm that you save it WITHOUT a passphrase. You can name the file `putty-private-key.ppk`. You can then close PuTTYGen.

![](images/puttygen-save.png)

5. Open PuTTY and configure the IP address/Hostname. Make sure you use the public **external IP address** provided in your reservation .
Keep port **22** and Connection type **SSH**.

![](images/putty-session.png)

6. Load the private key into PuTTY. Expand the left menu Connection -> SSH -> Auth and use the Browse button to load your Putty private key `putty-private-key.ppk`.

![](images/putty-load-key.png)

7. Configure the port redirections. Expand the left menu Connection -> SSH -> Tunnel. Set Source Port with **50000**, Destination **Localhost:23**, and click Add. 

![](images/putty-conf-port.png)

Then repeat the same using these mapping - do not forget to click Add:
- source port: **449** / desination: **localhost:449**
- source port: **2001** / desination: **localhost:2001**
- source port: **2002** / desination: **localhost:2002**
- source port: **8470** / desination: **localhost:8470**
- source port: **8471** / desination: **localhost:8471**
- source port: **8472** / desination: **localhost:8472**
- source port: **8473** / desination: **localhost:8473**
- source port: **8474** / desination: **localhost:8474**
- source port: **8475** / desination: **localhost:8475**
- source port: **8476** / desination: **localhost:8476**

Once done, your configuration has a list with all the redirected ports.

![](images/putty-conf-all-ports.png)

8. (Optional) Save your configuration to avoid doing all this again next time. Go back to the left menu Session, provide a name in **Saved Sessions** and click Save. Later on you click on your saved sessions name and use the **Load** button to reload your configuration.

![](images/putty-save.png)

9. Open the SSH connection using the Open button. Answer **Yes** to the security alert window.

![](images/putty-security.png)

10. Enter your system login. Check your reservation details. It should be **cecuser**.
Your connection is now opened and you can go to the [part about configuring ACS](#configuring-access-client-solution-windows--linux--mac)

![](images/putty-user.png)


### Configuring the SSH tunnel on a Linux/Windows machine

1. Save the project SSH private key into a file on your laptop using the editor of your choice (avoid MS Word or OpenOffice). You can name this file `private-key.txt`. The private SSH key is provided through the project kit or directly within your TechZone reservation page details. To help you identify the private key, it starts with `-----BEGIN RSA PRIVATE KEY-----`

2. Open a terminal and enter the following command. Replace :
- the IP address with the public **External IP address** provided in your reservation details
- the location of the `private-key.txt` file after the `-i` parameter
- **cecuser** if you are provided with a different account

If your local user is **root** you can remove **sudo**.

```shell
sudo ssh -L 50000:localhost:23 -L 2001:localhost:2001 -L 2002:localhost:2002 -L 449:localhost:449 -L 8470:localhost:8470 -L 8471:localhost:8471 -L 8472:localhost:8472 -L 8473:localhost:8473 -L 8474:localhost:8474 -L 8475:localhost:8475 -L 8476:localhost:8476 -o ExitOnForwardFailure=yes -o ServerAliveInterval=15 -o ServerAliveCountMax=3 -i ~/Desktop/private-key.txt cecuser@128.168.153.117
```

![](images/terminal-sudo.png)

If you kept `sudo`, the password that the command prompts you is your local user password.

![](images/terminal-done.png)

Your connection is now opened and you can go to the [part about configuring ACS](#configuring-access-client-solution-windows--linux--mac)


## Configuring Access Client Solution (Windows / Linux / Mac)

1. Donwload and install Access Client Solution (ACS) [https://www.ibm.com/support/pages/ibm-i-access-client-solutions](https://www.ibm.com/support/pages/ibm-i-access-client-solutions)

2. Open ACS. Open **5250 Session Manager**.

![](images/acs-sesssion-manager.png)

3. Start a New Display Session.

![](images/acs-new-display.png)

4. Configure with **localhost** and port **50000** and click OK to open the connection.

![](images/acs-session-configure.png)

5. Use the provided **CECUSER** login and password to connect to your IBM i 5250 session.

![](images/acs-connect.png)