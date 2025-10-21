┌──(root㉿kali)-[~]
└─# lsmod | grep -i 8852                  
8852bu               8376320  0
cfg80211             1466368  1 8852bu
usbcore               425984  5 ehci_pci,8852bu,usbhid,ehci_hcd,uhci_hcd
