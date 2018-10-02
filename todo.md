[Unit]

Description=Disk /%I is online
Requires=%i.device
Before=zfs-import-scan.service zfs-import-cache.service

[Install]

WantedBy=zfs-import-scan.service
WantedBy=zfs-import-cache.service
Diese Unit wird für jede Disk, die zu einem zpool gehört, aktiviert; zum Beispiel wird für die Disk /dev/disk/by-id/scsi-0123456789abcdef der folgende Befehl verwendet (Einfache Hochkommas beachten, sonst löst die Shell das \x2d auf):

systemd enable 'disk-online@dev-disk-by\x2did-scsi\x2d0123456789abcdef.target'
