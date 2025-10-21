┌──(root㉿kali)-[~]
└─# dmesg | grep -i -E 'usb|rtl|8832'
[    0.000000] Command line: BOOT_IMAGE=/boot/vmlinuz-6.12.38+kali-amd64 root=UUID=17488327-c7c2-4ceb-a568-a6f62b8a6cdc ro quiet splash
[    0.097422] Kernel command line: BOOT_IMAGE=/boot/vmlinuz-6.12.38+kali-amd64 root=UUID=17488327-c7c2-4ceb-a568-a6f62b8a6cdc ro quiet splash
[    6.834943] ACPI: bus type USB registered
[    6.835066] usbcore: registered new interface driver usbfs
[    6.835100] usbcore: registered new interface driver hub
[    6.844019] usbcore: registered new device driver usb
[    7.336397] ehci-pci 0000:02:03.0: new USB bus registered, assigned bus number 1
[    7.346889] ehci-pci 0000:02:03.0: USB 2.0 started, EHCI 1.00
[    7.347404] usb usb1: New USB device found, idVendor=1d6b, idProduct=0002, bcdDevice= 6.12
[    7.347417] usb usb1: New USB device strings: Mfr=3, Product=2, SerialNumber=1
[    7.347426] usb usb1: Product: EHCI Host Controller
[    7.347434] usb usb1: Manufacturer: Linux 6.12.38+kali-amd64 ehci_hcd
[    7.347442] usb usb1: SerialNumber: 0000:02:03.0
[    7.348025] hub 1-0:1.0: USB hub found
[    7.514993] uhci_hcd 0000:02:00.0: new USB bus registered, assigned bus number 2
[    7.518744] usb usb2: New USB device found, idVendor=1d6b, idProduct=0001, bcdDevice= 6.12
[    7.518761] usb usb2: New USB device strings: Mfr=3, Product=2, SerialNumber=1
[    7.518772] usb usb2: Product: UHCI Host Controller
[    7.518781] usb usb2: Manufacturer: Linux 6.12.38+kali-amd64 uhci_hcd
[    7.518790] usb usb2: SerialNumber: 0000:02:00.0
[    7.522888] hub 2-0:1.0: USB hub found
[    7.758939] usb 2-1: new full-speed USB device number 2 using uhci_hcd
[    7.909497] usb 2-1: New USB device found, idVendor=0e0f, idProduct=0003, bcdDevice= 1.03
[    7.909514] usb 2-1: New USB device strings: Mfr=1, Product=2, SerialNumber=0
[    7.909525] usb 2-1: Product: VMware Virtual USB Mouse
[    7.909535] usb 2-1: Manufacturer: VMware
[    8.046600] usb 2-2: new full-speed USB device number 3 using uhci_hcd
[    8.212083] usb 2-2: New USB device found, idVendor=0e0f, idProduct=0002, bcdDevice= 1.00
[    8.212096] usb 2-2: New USB device strings: Mfr=1, Product=2, SerialNumber=0
[    8.212103] usb 2-2: Product: VMware Virtual USB Hub
[    8.212161] usb 2-2: Manufacturer: VMware, Inc.
[    8.250642] hub 2-2:1.0: USB hub found
[    8.462141] usbcore: registered new interface driver usbhid
[    8.462152] usbhid: USB HID core driver
[    8.481647] input: VMware VMware Virtual USB Mouse as /devices/pci0000:00/0000:00:11.0/0000:02:00.0/usb2/2-1/2-1:1.0/0003:0E0F:0003.0001/input/input5
[    8.482424] hid-generic 0003:0E0F:0003.0001: input,hidraw0: USB HID v1.10 Mouse [VMware VMware Virtual USB Mouse] on usb-0000:02:00.0-1/input0
[   11.514959] EXT4-fs (sda1): mounted filesystem 17488327-c7c2-4ceb-a568-a6f62b8a6cdc ro with ordered data mode. Quota mode: none.
[   21.915783] EXT4-fs (sda1): re-mounted 17488327-c7c2-4ceb-a568-a6f62b8a6cdc r/w.
[  383.102451] usb 1-1: new high-speed USB device number 2 using ehci-pci
[  383.347113] usb 1-1: New USB device found, idVendor=0bda, idProduct=8832, bcdDevice= 0.00
[  383.347128] usb 1-1: New USB device strings: Mfr=1, Product=2, SerialNumber=3
[  383.347138] usb 1-1: Product: 802.11ac WLAN Adapter
[  383.347145] usb 1-1: Manufacturer: Realtek
[  383.347152] usb 1-1: SerialNumber: 00e04c000001
[ 1070.864637] usb 1-1: USB disconnect, device number 2
[ 1153.923178] usb 1-1: new high-speed USB device number 3 using ehci-pci
[ 1154.161414] usb 1-1: New USB device found, idVendor=0bda, idProduct=8832, bcdDevice= 0.00
[ 1154.161431] usb 1-1: New USB device strings: Mfr=1, Product=2, SerialNumber=3
[ 1154.161440] usb 1-1: Product: 802.11ac WLAN Adapter
[ 1154.161447] usb 1-1: Manufacturer: Realtek
[ 1154.161455] usb 1-1: SerialNumber: 00e04c000001
[ 1387.285841] usb 1-1: USB disconnect, device number 3
[ 4805.800843] usb 1-1: new high-speed USB device number 4 using ehci-pci
[ 4806.038369] usb 1-1: New USB device found, idVendor=0bda, idProduct=8832, bcdDevice= 0.00
[ 4806.038394] usb 1-1: New USB device strings: Mfr=1, Product=2, SerialNumber=3
[ 4806.038402] usb 1-1: Product: 802.11ac WLAN Adapter
[ 4806.038408] usb 1-1: Manufacturer: Realtek
[ 4806.038415] usb 1-1: SerialNumber: 00e04c000001
[ 6498.553807] usb 1-1: USB disconnect, device number 4
[ 6512.313469] usb 1-1: new high-speed USB device number 5 using ehci-pci
[ 6512.551595] usb 1-1: New USB device found, idVendor=0bda, idProduct=8832, bcdDevice= 0.00
[ 6512.551611] usb 1-1: New USB device strings: Mfr=1, Product=2, SerialNumber=3
[ 6512.551620] usb 1-1: Product: 802.11ac WLAN Adapter
[ 6512.551648] usb 1-1: Manufacturer: Realtek
[ 6512.551655] usb 1-1: SerialNumber: 00e04c000001
                                                                                 
┌──(root㉿kali)-[~]
└─# ip link show
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN mode DEFAULT group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP mode DEFAULT group default qlen 1000
    link/ether 00:0c:29:75:a9:60 brd ff:ff:ff:ff:ff:ff
