# Configure your second disk

During the reservation process you can add a second disk. The additional disk is mapped to your system and we let you use it at your convenience (raw, LVM, formatting, mount points, etc).
Here are some examples on how to discover, format and mount the disk in a traditional fashion.

[Add storage to a Linux server](#add-storage-to-a-linux-server)

[Add storage to an AIX server](#add-storage-to-an-aix-server)

[Add storage to an IBM i server](#add-storage-to-an-ibm-i-server)


## Add storage to a Linux server

The volume added to your system is presented as a "block device". In order to make use of it, some additional steps are required.
Depending on the environment and operating system your system is currently running with, the following instructions will help you with basic configuration of your newly added block device as a filesystem. 

### Discover the new block device
The command to list block devices on Linux is lsblk. If you type it on your system before you add a volume, you should get the following output, or similar:

```shell
[user664@c664-kvm1 ~]$ lsblk
NAME   MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
sr0     11:0    1  580K  0 rom
vda    253:0    0   60G  0 disk
├─vda1 253:1    0    4M  0 part
└─vda2 253:2    0   60G  0 part /
```

## Add storage to an AIX server

## Add storage to an IBM i server 