# Connecting to AIX / Linux hosted in IBM Cloud

By default, password authentication is disabled in IBM Cloud. You must connect using the project SSH private key.

Opening a SSH connection with private key is different if you run on a Windows or Linux/Mac OS machine. Choose the right method below.

## Connecting with a Windows machine and Putty

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

7. (Optional) Save your configuration to avoid doing all this again next time. Go back to the left menu Session, provide a name in **Saved Sessions** and click Save. Later on you click on your saved sessions name and use the **Load** button to reload your configuration.

![](images/putty-save.png)

8. Open the SSH connection using the Open button. Answer **Yes** to the security alert window.

![](images/putty-security.png)

9. Enter your system login. Check your reservation details. It should be **cecuser**.
Your connection is now opened.


## Connecting with a Linux / MacOS machine

1. Save the private key in a text file (eg: ~/Downloads/private-key.txt). The private SSH key is provided through the project kit or directly within your TechZone reservation page details. To help you identify the private key, it starts with `-----BEGIN RSA PRIVATE KEY-----`

2. Change the permissions on that file to match 600 `chmod 600 ~/Downloads/private-key.txt`

3. Open the SSH connection using the private key such as `ssh cecuser@123.123.123.123 -i ~/Downloads/private-key.txt`