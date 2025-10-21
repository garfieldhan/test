┌──(root㉿kali)-[~]
└─# apt install -y linux-image-amd64 linus-headers-amd64
错误： 无法定位软件包 linus-headers-amd64      

┌──(root㉿kali)-[~]
└─# cat /etc/apt/sources.list                                         
# See https://www.kali.org/docs/general-use/kali-linux-sources-list-repositories/
deb http://http.kali.org/kali kali-rolling main non-free non-free-firmware
deb-src http://mirrors.tuna.tsinghua.edu.cn/kali kali-rolling main contrib non-free non-free-firmware

# Additional line for source packages
# deb-src http://http.kali.org/kali kali-rolling main contrib non-free non-free-firmware

