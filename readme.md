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


Usage:
------
Create a variable declaration on a host basis along the following:

```yaml
zfs_zpools:
  zfs1:
    devices: /dev/sda3 /dev/sdb3 /dev/sdc3
  zfs2:
    devices: /dev/sde3 /dev/sdf3

zfs_vols:
  zfs1:
    vol_name: docker
    mountpoint: /var/lib/docker
    sync: standard
    vol_size: 10G
    state: present
    snapdir: visible
    snapdev: visible 
```
please note: mountpoint,state,volsize,snapdir,sync are optional.
