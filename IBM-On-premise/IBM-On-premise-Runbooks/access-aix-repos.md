# AIX Repositories

On-premise AIX systems will be installed with default images that do not have lots of extras installed.  Additional images and updates are automatically mounted by the NFS automounter when needed at the /repos mount point.

    
These are broken out into aix71, aix72, and aix73 subdirectories and the trial versions of the XLC compilers can be found in the lpp/XLC directory.  For non-IBMers these are typically but may not always be installed during provisioning.


Note we may sometimes overlook staging updates there, so if you find something missing you need please open a support ticket.
