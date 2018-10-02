Ansible ZFS Role for Debian
===========================

Features:
---------
* configures zfs on linux
* builds zfs modules
* configures zpools
* configures zvols
* configures automatic mounts at boot

Supported Platforms:
--------------------
- Debian stretch

Changelog:
----------
- Install linux-headers


Usage:
------
Create a variable declaration on a host basis along the following:

```yaml
zfs_zpools:
  zfs1:
    devices: /dev/disk/by-id/wwid... /dev/disk/by-id/wwid... /dev/disk/by-id/wwid...
  zfs2:
    devices: /dev/disk/by-id/wwid... /dev/disk/by-id/wwid...

zfs_zvols:
  vmlandscape:
    pool: zfs
    mountpoint: /var/lib/docker
    sync: standard
    vol_size: 10G
    state: present
    snapdir: visible
    snapdev: visible 
    compression: lz4
```
please note: mountpoint,state,volsize,snapdir,sync,compression are optional.
