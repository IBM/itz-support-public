## VMware WireGuard VPN for multiple user access

**NOTE: The WireGuard VPN provisoned in Techzone supports only one simultaneous connection by default**

Users need to manually to create additional WireGuard VPN peers, if they need to share access to their VM envrionment, or would like to connect from multiple systems at the same time

1. Follow the initial steps to enable VPN for a reservation
[VMware WireGuard VPN Access](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/VMwareWireguardVPNaccess.md)

2. Generate WireGuard public and private keys for each user
`wg genkey | tee user2-privatekey | wg pubkey > user2-publickey`
If `wg` is not found, install it by `sudo yum install wireguard-tools`

3. Go the router web interface https://192.168.253.1/wg/vpn_wg_peers.php from your VM bastion
(Default username: `admin`, password: `< your bastion password from reservation page >`)
4. Create a VPN peer for each user:
- Click `Add peer`
- Select `tun_wg0` tunnel
- Enter description (`User2` for e.g.)
- Enter a generated user public key
- Set `Allowed IPs` to an unique address `192.168.253.x/32`
- Click `Save`

![VPN](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/wireguard-peer.png)

5. Modify your downloaded WireGuard config from reservation page
6. Replace `Address` and `Private Key` with your new values in `[Interface]` section

Example:
```
[Interface]
PrivateKey = < new user generated private key >
Address = < new user unique address >
DNS = 192.168.253.1

[Peer]
PublicKey = HLTSRKfAzLbnWTahvSbbtrbrbrutrtMwgUH9iU=
AllowedIPs = 10.184.162.246/32, 10.241.106.184/32, 10.241.106.135/32, 192.168.252.0/24, 10.241.106.134/32, 10.184.162.198/32, 10.241.106.167/32, 10.241.106.176/32, 10.184.162.174/32, 10.185.220.3/32, 10.241.106.162/32, 192.168.253.0/24, 10.184.18.66/32, 10.241.106.161/32, 10.241.106.137/32, 10.184.162.221/32, 10.241.106.164/32, 10.241.106.185/32, 10.241.106.190/32
Endpoint = 169.60.19.194:31907
```

7. Share the new WireGuard config with your user

Support
For any questions, contact ITZ support - techzone.help@ibm.com
