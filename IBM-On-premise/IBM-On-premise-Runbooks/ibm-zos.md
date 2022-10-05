# IBM z/OS Offering

## The following application versions are part of the deployed builds:

- z/OS 2.4
- CICS v5.6
- CICS Performance Analyzer v5.4
- DB2 v12.1
- DB2 Admin Tool v 12.1
- MQ v9.2
- Rocket tools
- Bash v4.3
- TWS v9.3
- Java v8 (1.8.0_281)
- Enterprise Cobol v4r2, v5r1, v6r1, v6r2, v6r3
- PL1 v2r3, v3r3, v4r2
- REXX v1r4

## How to connect to the z/OS LPARs

Once your z/OS LPAR has been provisioned (and you have access to the IP address along with having the username and password) there are a few different ways you can connect to it depending on your workstation Operating System.

1. Connecting via TSO (port 23) by using PCOMM (for windows) or through Host-On-Demand (for Mac and Linux) PCOMM - Will be installed by default for all IBM issued windows machines. Host-On-Demand - can be installed for Mac by visiting the MAC@IBM store. More information will be provided soon about HOD for Linux.

2.  Connecting via SSH (port 22) or Telnet (port 623) can be done through PUTTY (for Windows) or through the terminal installed by default (for Mac and Linux) PUTTY - Also installed by default on IBM issued windows machines.

3.  Connecting via z/OSMF (port 443) by using the web browser The z/OSMF url will have the following structure - https://<hostname>/zosmf

## Additional Information

A lot of additional information about the provided z/OS environment can be found in the document here:

[https://github.com/IBM/itz-support-public/blob/main/IBM-On-premise/IBM-On-premise-Runbooks/docs/zOS_Information_0924.pdf](https://github.com/IBM/itz-support-public/blob/main/IBM-On-premise/IBM-On-premise-Runbooks/docs/zOS_Information_0924.pdf)

