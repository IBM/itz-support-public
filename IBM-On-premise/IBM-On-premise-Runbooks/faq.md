# Archived do NOT use August 30th 2023

# FAQ 

## Q: What is the IBM Technology Zone On-Premise Systems Infrastructure?
IBM Technology Zone On-Premise Systems Infrastructure was formerly known as the Cloud for Enablement and Co-Creation, or CECC. It provides access to IBM Power, Z and Storage environments for Business Partners, ISV's and IBMers. The environments are easy to request, easy to access, and usually provide adequate capacity for most common testing or demonstration requests.

## Q: How can I get started with IBM Technology Zone On-Premise Systems Infrastructure?
Users should start at the IBM Technology Zone portal - [https://techzone.ibm.com](https://techzone.ibm.com) - to view all the environments available.

## Q: What can ISV, BP, and IBM developers now do that they could not before?
Until now, ISV, BP, and IBM developers did not have the capital to acquire resources and ensure they had the capacity they needed to handle demonstrations, testing, proof of technologies, etc. IBM Technology Zone On-Premise Systems Infrastructure enables any ISV, BP, and IBM developer to leverage IBM Technology Zone Infrastructure OnPrem Systems Infrastructure's own benefits of scale with no capital investment.

## Q: How do I run systems in the IBM Technology Zone On-Premise Systems Infrastructure environment?
Login to the Portal and you will be automatically registered if you are an IBMer or Business Partner.

## Q: How quickly will systems be running?
Most resources are available the same day, but some, like bare metal or GPU, may require future scheduling or approval.

## Q: How do I load and store my data?
IBM Technology Zone Infrastructure OnPrem Systems Infrastructure allows you to set up and configure everything up to your operating system. An image is simply a pre-defined / pre-configured environment that includes all the necessary items to set up and access your instance. You can then transfer your data to be used in the environment from your own local systems, using SCP or a similar transfer protocol.

## Q: How do I access my systems?
Your environment will be provisioned and will provide user IDs, passwords, IP and DNS names, one for each system that has been created. This information is used to access the system exactly as you would if it were in your own data center. You own that machine while your reservation time is active. You will receive email confirmation on reservation activation to know when your system is ready to be used.

## Q: How can I get help?
There is a support tab in the portal that allows support requests to be submitted.

## Q: What kind of technical support is available?
Support up to Operating System is available using the support tab to submit a support request.

## Q: I want to use this for a demonstration, what should I do?
IBM Technology Zone On-Premise Systems Infrastructure does not provide pre-configured demonstration environments. Please see the IBM Technology Zone [https://techzone.ibm.com](https://techzone.ibm.com) for a list of available pre-configured demonstrations.

## Q: Is IBM Technology Zone On-Premise Systems Infrastructure used in conjunction with IBM Cloud?
No, it is used independently from IBM Cloud. By using IBM Technology Zone On-Premise Systems
Infrastructure, ISV, Business Partners, and IBM developers have access to scalable, reliable, fast, inexpensive
infrastructure.

## Q: How many instances can I run?
In many cases you are limited to running or scheduling 5 systems at a time. You can schedule multiple systems of different types in a single project, but most projects are restricted to subnets that only have 5 available IP addresses.

## Q: What operating system environments are supported?
We currently support a variety of operating systems including Ubuntu, Red Hat Enterprise Linux, SUSE Linux Enterprise
Server, AIX, IBM i, z/OS.

## Q: Do the systems have GPUs?
Yes, there is GPU availability with KVM and Bare metal requests.

## Q. What is the IBM Technology Zone On-Premise Systems Infrastructure Service Level Agreement?
Currently, there are no SLA’s.

## Q: What are the key use cases for Instances?
General Purpose instances offer a good choice for running development and test environments for a limited duration. Customers who are interested in running performance, business-critical, or long-term hosting may better be positioned to use one of the other IBM Technology Zone environments.

## Q. Which operating systems are supported?
The following OS’s are supported though not necessarily all on the same platform or processor type:
- IBM AIX 7.1, 7.2, and 7.3
- IBM i 7.2, 7.3, 7.4, and 7.5
- Red Hat Enterprise Linux 7, 8, and 9
- Ubuntu 18.04, 20.04, and 22.04
- SLES 12 and 15
- z/OS 2.4

More Operating systems are being evaluated for future releases.

## Q. When should I use GPU Graphics and Compute instances?
GPU instances work best for applications with massive parallelism such as workloads using thousands of threads. Graphics processing is an example with huge computational requirements, where each of the tasks is relatively small, the set of operations performed form a pipeline, and the throughput of this pipeline is more important than the latency of the individual operations. To be able build applications that exploit this level of parallelism, one needs GPU device specific knowledge by understanding how to program against various graphics APIs (DirectX, OpenGL) or GPU compute programming models (CUDA, OpenCL).

## Q. What APIs and programming models are supported by GPU Graphics and Compute instances?
Instances support CUDA 9 and OpenCL, P2 instances support CUDA 8, OpenCL 1.2, DirectX 12, OpenGL 4.5, CUDA 8, and OpenCL 1.2.

## Q. What are the storage options available?
We offer the following storage options:
- Baremetal servers will use internal storage
- KVM servers will use iSCSI storage
- PowerVM servers will use SAN storage
Currently, we do now allow any direct-attached dedicated storage devices.

## Q. What are the underlying hypervisor virtual instances?
- Ubuntu KVM for KVM virtual instances
- IBM PowerVM for PowerVM virtual instances
- IBM z/VM for IBM z Linux and z/OS instances

## Q. What is the max CPU allowed for virtual instances?
The max CPU for an instance is generally set to 16 per instance but may vary by offering platform.

## Q. What is the max memory allowed for virtual instances?
The max memory for an instance is generally set to 32GB per instance but may vary by offering platform.

## Q. What happens to my data when a system terminates?
The data stored on a local instance store will persist only if that instance is alive. We recommend that you use your local storage for temporary data and retention. All data left on system will be removed and unrecoverable on system termination.

## Q. Where is the additional storage that I requested through "Second Disk"?
An additional disk has been mapped to your system and we let you use this disk at your convenience (raw, LVM, formatting, mount points, etc).

Here are some examples on how to discover, format and mount the disk in a traditional fashion.
- [Add storage to a Linux server](configure-second-disk.md#add-storage-to-a-linux-server)
- [Add storage to an AIX server](configure-second-disk.md#add-storage-to-an-aix-server)
- [Add storage to an IBM i server](configure-second-disk.md#add-storage-to-an-ibm-i-server)

## Q. How do I prevent other people from viewing my systems?
You have complete control over the visibility of your systems. The IBM Technology Zone On-Premise Systems Infrastructure isolates each environment with separate VLAN’s and a firewall.

## Q. How many instances am I allowed to reserve?
Three (3) instances per request per system type and five (5) systems per project with different system types.


## Q. Can I modify a Reservation Request after it has started?
Currently you cannot extend a reservation after it has started. We are working on removing that limitation.

## Q. Can I end a Reservation Request after it has started?
Yes. You can end a Scheduled or Ready reservation at any time. 

## Q. Is IBM Technology Zone On-Premise Systems Infrastructure running in more than one region?
IBM Technology Zone On-Premise Systems Infrastructure is hosted in Poughkeepsie, NY.

## Q. What is the primary use case for an environment?
IBM Technology Zone On-Premise Systems Infrastructure provides a non-performance environment for POC, POT and Demo of product feature and function

## Q. Does IBM Technology Zone On-Premise Systems Infrastructure allow production workloads?
No!! IBM Technology Zone On-Premise Systems Infrastructure is only to be used for non-production environments for hands-on Power hardware, POC, POT, and Demo of product.

## Q. Does IBM Technology Zone On-Premise Systems Infrastructure allow confidential data loaded to environments?
No!! IBM Technology Zone On-Premise Systems Infrastructure does not allow for any confidential or personal information data to be loaded into the environment.

## Q. Does IBM Technology Zone On-Premise Systems Infrastructure allow for long-term hosting?
No. IBM Technology Zone On-Premise Systems Infrastructure provides short term usage of pre-defined and pre-configured offerings

## Q. Does IBM Technology Zone On-Premise Systems Infrastructure allow installation of software from other sites?
Yes, installation of other software, IBM or open-source, is allowed on the systems. One example is below:
- H2O: documentation is available online on the [H2O website](https://s3.amazonaws.com/artifacts.h2o.ai/releases/ai/h2o/dai/rel-1.5.4-65/docs/userguide/install/ibm-power.html)
- Registered IBM PartnerWorld Members can download IBM applications and middleware from the IBM Software Access Catalog.
Go here for details and steps required.

## Q. Does the On-Premises IBM Z z/OS Base Image come with RACF pre-installed and configured and is it accessible by external IP addrress (for instance, from an virtual server hosted on our IBM Cloud)? 
Yes, RACF should pre-installed and configured! However, this is not accessible by external IP address as these are in POK and not exposed on the internet in any manner.

Thank you!

