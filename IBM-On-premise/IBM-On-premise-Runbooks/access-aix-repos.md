# AIX Repositories

AIX systems will be installed with default images.  Additional images and updates are automatically mounted by the NFS automounter when needed at the following locations:

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