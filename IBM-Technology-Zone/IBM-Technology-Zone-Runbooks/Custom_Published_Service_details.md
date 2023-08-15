
# Defining Custom Published Services

## All ports opened for environments in Skytap are automatically sent with reservation emails

1. Go to (https://techzone.ibm.com)
2. Click on edit
3. Click Environments.
4. Click edit "pencil" icon
5. Go to Link Patterns
6. Enter Port Number And Template

Undefined port    

  Port Number 80 Default Template http://targetDomain:targetPort  
  email output = http://services-uscentral.skytap.com:16617  
  
Defined Port   

  Port Number 8080 Template Access to port 8080: http://targetDomain:targetPort  
  email output = Access to port 8080: http://services-uscentral.skytap.com:16624  


Link Pattern and Template example  
![Defined port IBM Technology Zone](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/Defined-port-techzone.png)  

Email output received   
![Defined port email](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/Defined-port-email.png)  
