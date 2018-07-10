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
create a variable declartion on a host basis like this:

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
    state: present
```