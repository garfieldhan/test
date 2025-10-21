┌──(root㉿kali)-[~]
└─# lsusb               
Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
Bus 001 Device 002: ID 0bda:8832 Realtek Semiconductor Corp. 802.11ac WLAN Adapter
Bus 002 Device 001: ID 1d6b:0001 Linux Foundation 1.1 root hub
Bus 002 Device 002: ID 0e0f:0003 VMware, Inc. Virtual Mouse
Bus 002 Device 003: ID 0e0f:0002 VMware, Inc. Virtual USB Hub
                                                                                           
┌──(root㉿kali)-[~]
└─# echo 0bda 8832 > /sys/bus/usb/drivers/rtl8852bu/new_id
                                                                                           
┌──(root㉿kali)-[~]
└─# dmesg | tail -n 100
[    9.843506] systemd[1]: Expecting device dev-disk-by\x2duuid-3e575410\x2d07ac\x2d4d2b\x2d9b1a\x2d6abb9e804e64.device - /dev/disk/by-uuid/3e575410-07ac-4d2b-9b1a-6abb9e804e64...
[    9.843528] systemd[1]: Expecting device dev-disk-by\x2duuid-50d41a06\x2d3599\x2d4d8e\x2da716\x2dd011d49d5f1d.device - /dev/disk/by-uuid/50d41a06-3599-4d8e-a716-d011d49d5f1d...
[    9.843548] systemd[1]: Expecting device dev-disk-by\x2duuid-b9c78a21\x2d8ee1\x2d4107\x2d82ee\x2dc9f03273e251.device - /dev/disk/by-uuid/b9c78a21-8ee1-4107-82ee-c9f03273e251...
[    9.843565] systemd[1]: Expecting device dev-disk-by\x2duuid-fe45058f\x2da136\x2d452b\x2dafbc\x2dc98822a823db.device - /dev/disk/by-uuid/fe45058f-a136-452b-afbc-c98822a823db...
[    9.843646] systemd[1]: Reached target nss-user-lookup.target - User and Group Name Lookups.
[    9.843695] systemd[1]: Reached target slices.target - Slice Units.
[    9.843736] systemd[1]: Reached target stunnel.target - TLS tunnels for network services - per-config-file target.
[    9.845366] systemd[1]: Listening on systemd-creds.socket - Credential Encryption/Decryption.
[    9.845633] systemd[1]: Listening on systemd-initctl.socket - initctl Compatibility Named Pipe.
[    9.845863] systemd[1]: Listening on systemd-journald-dev-log.socket - Journal Socket (/dev/log).
[    9.846121] systemd[1]: Listening on systemd-journald.socket - Journal Sockets.
[    9.846174] systemd[1]: systemd-pcrextend.socket - TPM PCR Measurements was skipped because of an unmet condition check (ConditionSecurity=measured-uki).
[    9.846200] systemd[1]: systemd-pcrlock.socket - Make TPM PCR Policy was skipped because of an unmet condition check (ConditionSecurity=measured-uki).
[    9.846381] systemd[1]: Listening on systemd-udevd-control.socket - udev Control Socket.
[    9.846558] systemd[1]: Listening on systemd-udevd-kernel.socket - udev Kernel Socket.
[    9.849549] systemd[1]: Mounting dev-hugepages.mount - Huge Pages File System...
[    9.854163] systemd[1]: Mounting dev-mqueue.mount - POSIX Message Queue File System...
[    9.857940] systemd[1]: Mounting run-lock.mount - Legacy Locks Directory /run/lock...
[    9.861954] systemd[1]: Mounting sys-kernel-debug.mount - Kernel Debug File System...
[    9.871425] systemd[1]: Mounting sys-kernel-tracing.mount - Kernel Trace File System...
[    9.871662] systemd[1]: auth-rpcgss-module.service - Kernel Module supporting RPCSEC_GSS was skipped because of an unmet condition check (ConditionPathExists=/etc/krb5.keytab).
[    9.877505] systemd[1]: Starting keyboard-setup.service - Set the console keyboard layout...
[    9.886221] systemd[1]: Starting kmod-static-nodes.service - Create List of Static Device Nodes...
[    9.895893] systemd[1]: Starting modprobe@configfs.service - Load Kernel Module configfs...
[    9.911712] systemd[1]: Starting modprobe@drm.service - Load Kernel Module drm...
[    9.922042] systemd[1]: Starting modprobe@efi_pstore.service - Load Kernel Module efi_pstore...
[    9.930588] systemd[1]: Starting modprobe@fuse.service - Load Kernel Module fuse...
[    9.930887] systemd[1]: systemd-fsck-root.service - File System Check on Root Device was skipped because of an unmet condition check (ConditionPathExists=!/run/initramfs/fsck-root).
[    9.933329] systemd[1]: systemd-hibernate-clear.service - Clear Stale Hibernate Storage Info was skipped because of an unmet condition check (ConditionPathExists=/sys/firmware/efi/efivars/HibernateLocation-8cf2644b-4b0b-428f-9387-6d876050dc67).
[    9.951656] systemd[1]: Starting systemd-journald.service - Journal Service...
[    9.971650] systemd[1]: Starting systemd-modules-load.service - Load Kernel Modules...
[    9.971721] systemd[1]: systemd-pcrmachine.service - TPM PCR Machine ID Measurement was skipped because of an unmet condition check (ConditionSecurity=measured-uki).
[   10.007927] systemd[1]: Starting systemd-remount-fs.service - Remount Root and Kernel File Systems...
[   10.008196] systemd[1]: systemd-tpm2-setup-early.service - Early TPM SRK Setup was skipped because of an unmet condition check (ConditionSecurity=measured-uki).
[   10.013530] systemd[1]: Starting systemd-udev-load-credentials.service - Load udev Rules from Credentials...
[   10.024000] systemd[1]: Starting systemd-udev-trigger.service - Coldplug All udev Devices...
[   10.043104] systemd[1]: Mounted dev-hugepages.mount - Huge Pages File System.
[   10.055076] systemd[1]: Mounted dev-mqueue.mount - POSIX Message Queue File System.
[   10.057321] systemd[1]: Mounted run-lock.mount - Legacy Locks Directory /run/lock.
[   10.057899] systemd[1]: Mounted sys-kernel-debug.mount - Kernel Debug File System.
[   10.058773] systemd[1]: Mounted sys-kernel-tracing.mount - Kernel Trace File System.
[   10.061061] systemd[1]: Finished keyboard-setup.service - Set the console keyboard layout.
[   10.062855] systemd[1]: Finished kmod-static-nodes.service - Create List of Static Device Nodes.
[   10.068194] systemd[1]: modprobe@configfs.service: Deactivated successfully.
[   10.069728] systemd[1]: Finished modprobe@configfs.service - Load Kernel Module configfs.
[   10.073483] systemd[1]: modprobe@drm.service: Deactivated successfully.
[   10.074640] systemd[1]: Finished modprobe@drm.service - Load Kernel Module drm.
[   10.075048] systemd-journald[409]: Collecting audit messages is disabled.
[   10.076248] systemd[1]: modprobe@efi_pstore.service: Deactivated successfully.
[   10.077054] systemd[1]: Finished modprobe@efi_pstore.service - Load Kernel Module efi_pstore.
[   10.078649] systemd[1]: modprobe@fuse.service: Deactivated successfully.
[   10.080132] systemd[1]: Finished modprobe@fuse.service - Load Kernel Module fuse.
[   10.081977] systemd[1]: Finished systemd-modules-load.service - Load Kernel Modules.
[   10.088894] EXT4-fs (sda1): re-mounted 17488327-c7c2-4ceb-a568-a6f62b8a6cdc r/w.
[   10.096195] systemd[1]: Mounting sys-fs-fuse-connections.mount - FUSE Control File System...
[   10.110180] systemd[1]: Mounting sys-kernel-config.mount - Kernel Configuration File System...
[   10.120239] systemd[1]: Starting systemd-sysctl.service - Apply Kernel Variables...
[   10.127236] systemd[1]: Starting systemd-tmpfiles-setup-dev-early.service - Create Static Device Nodes in /dev gracefully...
[   10.160148] systemd[1]: Finished systemd-remount-fs.service - Remount Root and Kernel File Systems.
[   10.167857] systemd[1]: Finished systemd-udev-load-credentials.service - Load udev Rules from Credentials.
[   10.172617] systemd[1]: Mounted sys-fs-fuse-connections.mount - FUSE Control File System.
[   10.173978] systemd[1]: Mounted sys-kernel-config.mount - Kernel Configuration File System.
[   10.184055] systemd[1]: Mounting run-vmblock\x2dfuse.mount - VMware vmblock fuse mount...
[   10.191721] systemd[1]: systemd-hwdb-update.service - Rebuild Hardware Database was skipped because of an unmet condition check (ConditionNeedsUpdate=/etc).
[   10.244698] systemd[1]: Finished systemd-sysctl.service - Apply Kernel Variables.
[   10.283142] systemd[1]: Mounted run-vmblock\x2dfuse.mount - VMware vmblock fuse mount.
[   10.296507] systemd[1]: Finished systemd-tmpfiles-setup-dev-early.service - Create Static Device Nodes in /dev gracefully.
[   10.297065] systemd[1]: systemd-sysusers.service - Create System Users was skipped because no trigger condition checks were met.
[   10.304753] systemd[1]: Starting systemd-tmpfiles-setup-dev.service - Create Static Device Nodes in /dev...
[   10.391563] systemd[1]: Finished systemd-tmpfiles-setup-dev.service - Create Static Device Nodes in /dev.
[   10.391968] systemd[1]: Reached target local-fs-pre.target - Preparation for Local File Systems.
[   10.397542] systemd[1]: Starting systemd-udevd.service - Rule-based Manager for Device Events and Files...
[   10.762546] systemd[1]: Started systemd-udevd.service - Rule-based Manager for Device Events and Files.
[   10.946742] systemd[1]: Started systemd-journald.service - Journal Service.
[   11.702472] sr 1:0:0:0: Attached scsi generic sg0 type 5
[   11.702803] sd 2:0:0:0: Attached scsi generic sg1 type 0
[   11.979428] ACPI: AC: AC Adapter [ACAD] (on-line)
[   12.383041] Adding 487420k swap on /dev/sda6.  Priority:-2 extents:1 across:487420k 
[   12.700848] EXT4-fs (sda7): mounted filesystem 3e575410-07ac-4d2b-9b1a-6abb9e804e64 r/w with ordered data mode. Quota mode: none.
[   12.911314] EXT4-fs (sda5): mounted filesystem b9c78a21-8ee1-4107-82ee-c9f03273e251 r/w with ordered data mode. Quota mode: none.
[   13.031962] systemd-journald[409]: Received client request to flush runtime journal.
[   13.049416] EXT4-fs (sda8): mounted filesystem fe45058f-a136-452b-afbc-c98822a823db r/w with ordered data mode. Quota mode: none.
[   13.167078] random: crng init done
[   13.768167] input: PC Speaker as /devices/platform/pcspkr/input/input6
[   15.263701] RPC: Registered named UNIX socket transport module.
[   15.263711] RPC: Registered udp transport module.
[   15.263717] RPC: Registered tcp transport module.
[   15.263722] RPC: Registered tcp-with-tls transport module.
[   15.263727] RPC: Registered tcp NFSv4.1 backchannel transport module.
[   15.566391] RAPL PMU: API unit is 2^-32 Joules, 0 fixed counters, 10737418240 ms ovfl timer
[   15.809155] NET: Registered PF_QIPCRTR protocol family
[   15.905429] e1000: eth0 NIC Link is Up 1000 Mbps Full Duplex, Flow Control: None
[  404.389671] cfg80211: Loading compiled-in X.509 certificates for regulatory database
[  404.411654] Loaded X.509 cert 'benh@debian.org: 577e021cb980e0e820821ba7b54b4961b8b4fadf'
[  404.412033] Loaded X.509 cert 'romain.perier@gmail.com: 3abbc6ec146e09d1b6016ab9d6cf71dd233f0328'
[  404.412381] Loaded X.509 cert 'sforshee: 00b28ddf47aef9cea7'
[  404.412736] Loaded X.509 cert 'wens: 61c038651aabdcf94bd0ac7ff06c7248db18c600'
[  869.063080] 8852bu: loading out-of-tree module taints kernel.
[  869.063339] 8852bu: module verification failed: signature and/or required key missing - tainting kernel
[  873.093061] usbcore: registered new interface driver rtl8852bu
                                                                                           
┌──(root㉿kali)-[~]
└─# ip link show                   
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN mode DEFAULT group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP mode DEFAULT group default qlen 1000
    link/ether 00:0c:29:75:a9:60 brd ff:ff:ff:ff:ff:ff
                                                    
