                                                                                 
┌──(root㉿kali)-[/usr/src/rtl8852bu]
└─# sudo make clean 2>/dev/null || true
cd phl ; rm -fr */*/*/*/*.mod.c */*/*/*/*.mod */*/*/*/*.o */*/*/*/.*.cmd */*/*/*/*.ko
cd phl ; rm -fr */*/*/*.mod.c */*/*/*.mod */*/*/*.o */*/*/.*.cmd */*/*/*.ko
cd phl ; rm -fr */*/*.mod.c */*/*.mod */*/*.o */*/.*.cmd */*/*.ko
cd phl ; rm -fr */*.mod.c */*.mod */*.o */.*.cmd */*.ko
cd phl ; rm -fr *.mod.c *.mod *.o .*.cmd *.ko
cd core ; rm -fr */*.mod.c */*.mod */*.o */.*.cmd */*.ko
cd core ; rm -fr *.mod.c *.mod *.o .*.cmd *.ko
cd os_dep/linux ; rm -fr *.mod.c *.mod *.o .*.cmd *.ko
cd os_dep/linux/hwsim ; rm -fr *.mod.c *.mod *.o .*.cmd *.ko
cd os_dep ; rm -fr *.mod.c *.mod *.o .*.cmd *.ko
cd platform ; rm -fr *.mod.c *.mod *.o .*.cmd *.ko
rm -fr Module.symvers ; rm -fr Module.markers ; rm -fr modules.order
rm -fr *.mod.c *.mod *.o .*.cmd *.ko *~
rm -fr .tmp_versions
                                                                                 
┌──(root㉿kali)-[/usr/src/rtl8852bu]
└─# make -j$(nproc)
make ARCH=x86_64 CROSS_COMPILE= -C /lib/modules/6.16.8+kali-amd64/build M=/usr/src/rtl8852bu  modules
make[1]: 进入目录“/usr/src/linux-headers-6.16.8+kali-amd64”
make[2]: 进入目录“/usr/src/rtl8852bu”
  CC [M]  platform/platform_ops.o
  CC [M]  os_dep/osdep_service.o
  CC [M]  os_dep/osdep_service_linux.o
  CC [M]  os_dep/linux/rtw_cfg.o
os_dep/osdep_service.c:17:10: fatal error: drv_types.h: 没有那个文件或目录
   17 | #include <drv_types.h>
      |          ^~~~~~~~~~~~~
compilation terminated.
platform/platform_ops.c:15:10: fatal error: drv_types.h: 没有那个文件或目录
   15 | #include <drv_types.h>
      |          ^~~~~~~~~~~~~
compilation terminated.
make[4]: *** [/usr/src/linux-headers-6.16.8+kali-common/scripts/Makefile.build:292：os_dep/osdep_service.o] 错误 1
make[4]: *** 正在等待未完成的任务....
make[4]: *** [/usr/src/linux-headers-6.16.8+kali-common/scripts/Makefile.build:292：platform/platform_ops.o] 错误 1
os_dep/osdep_service_linux.c:16:10: fatal error: drv_types.h: 没有那个文件或目录
   16 | #include <drv_types.h>
      |          ^~~~~~~~~~~~~
compilation terminated.
make[4]: *** [/usr/src/linux-headers-6.16.8+kali-common/scripts/Makefile.build:292：os_dep/osdep_service_linux.o] 错误 1
os_dep/linux/rtw_cfg.c:17:10: fatal error: drv_types.h: 没有那个文件或目录
   17 | #include <drv_types.h>
      |          ^~~~~~~~~~~~~
compilation terminated.
make[4]: *** [/usr/src/linux-headers-6.16.8+kali-common/scripts/Makefile.build:292：os_dep/linux/rtw_cfg.o] 错误 1
make[3]: *** [/usr/src/linux-headers-6.16.8+kali-common/Makefile:2027：.] 错误 2
make[2]: *** [/usr/src/linux-headers-6.16.8+kali-common/Makefile:260：__sub-make] 错误 2
make[2]: 离开目录“/usr/src/rtl8852bu”
make[1]: *** [/usr/src/linux-headers-6.16.8+kali-common/Makefile:260：__sub-make] 错误 2
make[1]: 离开目录“/usr/src/linux-headers-6.16.8+kali-amd64”
make: *** [Makefile:738：modules] 错误 2
                                                     
