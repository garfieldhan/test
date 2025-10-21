┌──(root㉿kali)-[~]
└─# uname -r
6.16.8+kali-amd64
                                                                                         
┌──(root㉿kali)-[~]
└─# lsmod | grep -i 8852              
                                                                                         
┌──(root㉿kali)-[~]
└─# lsmod | grep -i 88x2
                                                                                         
┌──(root㉿kali)-[~]
└─# dmesg | grep -i -E '8852|8832|rtl|firmware|wlan' | tail -n 80
[    0.000000] Command line: BOOT_IMAGE=/boot/vmlinuz-6.16.8+kali-amd64 root=UUID=17488327-c7c2-4ceb-a568-a6f62b8a6cdc ro quiet splash
[    0.098133] Kernel command line: BOOT_IMAGE=/boot/vmlinuz-6.16.8+kali-amd64 root=UUID=17488327-c7c2-4ceb-a568-a6f62b8a6cdc ro quiet splash
[    0.520288] ACPI: [Firmware Bug]: BIOS _OSI(Linux) query ignored
[    0.588322] ACPI: Enabled 4 GPEs in block 00 to 0F
[    6.328331] usb 1-1: New USB device found, idVendor=0bda, idProduct=8832, bcdDevice= 0.00
[    6.328354] usb 1-1: Product: 802.11ac WLAN Adapter
[    8.043189] EXT4-fs (sda1): mounted filesystem 17488327-c7c2-4ceb-a568-a6f62b8a6cdc ro with ordered data mode. Quota mode: none.
[    9.933329] systemd[1]: systemd-hibernate-clear.service - Clear Stale Hibernate Storage Info was skipped because of an unmet condition check (ConditionPathExists=/sys/firmware/efi/efivars/HibernateLocation-8cf2644b-4b0b-428f-9387-6d876050dc67).
[   10.088894] EXT4-fs (sda1): re-mounted 17488327-c7c2-4ceb-a568-a6f62b8a6cdc r/w.
                                                                                         
┌──(root㉿kali)-[~]
└─# ls /lib/modules/6.16.8+kali-amd64/kernel/drivers/net/wireless | grep -i 8852
8852bu.ko
                                                                                         
┌──(root㉿kali)-[~]
└─# modinfo ftl8852bu 2>/dev/null | grep -E 'filename|version|alias'
                                                                                         
┌──(root㉿kali)-[~]
└─# ip link show
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN mode DEFAULT group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP mode DEFAULT group default qlen 1000
    link/ether 00:0c:29:75:a9:60 brd ff:ff:ff:ff:ff:ff
                                                                                         
┌──(root㉿kali)-[~]
└─# iw dev      
