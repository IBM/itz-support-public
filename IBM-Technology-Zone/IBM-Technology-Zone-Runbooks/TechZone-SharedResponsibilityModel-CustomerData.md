# Shared Responsibility Models

The Shared Responsibility Model is a security and compliance framework that outlines the responsibilities of cloud service providers (CSPs) and customers for securing every aspect of the cloud environment, including hardware, infrastructure, endpoints, data, configurations, settings, operating system (OS), network controls and access rights.

In its simplest terms, the Shared Responsibility Model dictates that the cloud provider—such as Amazon Web Service (AWS), Microsoft Azure, or Google Cloud Platform (GCP)—must monitor and respond to security threats related to the cloud itself and its underlying infrastructure. Meanwhile, end users, including individuals and companies, are responsible for protecting data and other assets they store in any cloud environment.*

# Customer Data on TechZone and Shared Responsibility Model

TechZone supports some classifications of customer data without need for further approvals as detailed on the [Customer D
ata Document](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Customer-data%20on%20TechZone.md)


## IBM Cloud Environments

### IBM Cloud Shared Responsibility Model [link](https://cloud.ibm.com/docs/overview?topic=overview-shared-responsibilities)

In IBM Cloud®, as is the case for other cloud service providers, the responsibilities for managing the lifecycle of, operating, and securing products are shared between IBM® and the customer.

The responsibility of completing the following types of tasks on various products can be exclusive to IBM, the customer, or shared between the two. The tasks for each type of product are grouped in the following categories:

    Incident and operations management: Includes tasks such as monitoring, event management, high availability, problem determination, recovery, and full state backup and recovery.
    Change management: Includes tasks such as deployment, configuration, upgrades, patching, configuration changes, and deletion.
    Identity and access management: Includes tasks such as authentication, authorization, access control policies, and approving, granting, and revoking access.
    Security and regulation compliance: Includes tasks such as security controls implementation and compliance certification.
    Disaster recovery: Includes tasks such as providing dependencies on disaster recovery sites, provision disaster recovery environments, data and configuration backup, replicating data and configuration to the disaster recovery environment, and failover on disaster events.


### TechZone Security Terms and Conditions

TechZone users must adhere to [terms and conditions(https://techzone.ibm.com/terms)], [Content contributor Guidelines](https://techzone.ibm.com/terms/contributor), and [end user security policies](https://techzone.ibm.com/terms/securitypolicy).


### TechZone Provisioning and account access responsibilities

Client facing reservations (purpose: Customer Demo, Proof of Technology) with customer data will be provisioned in dedicated infrastructure to ensure a secure environment for supported customer data classifications as listed in the customer data runbook.

As part of provisioning, TechZone will: 

1. Whitelist the account for services
2. Activate SCC
3. Register with SoS for Vuln Scanning.
4. Add a logdna instance to the account
5. Add an activity tracker instance.
6. Onboard a designated Account Owner
7. Close the account when activity is over.

### Customer Team Responsibilities

Designated Account Owner is responsible for further onboarding of team members and security of the Demo services, applications and data.



---

- [SM Ref from Crowdstrike.com](https://www.crowdstrike.com/cybersecurity-101/cloud-security/shared-responsibility-model/)
