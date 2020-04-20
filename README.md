# sunxi_A10_nfs_buildroot
Using MK802ii for tftp, nfs, Shadowsocks-Manager server. Buildroot is used to create rootfs

Using SystemV, Console must set to tty0. Do not use systemD for Linux kernel <3.14

**addusr minxu -G sudo**

default tftp path,(cat /etc/init.d/S80tftpd-hpa)

**/var/lib/tftpboot**

## Buildroot : Using out of tree defconfig
**make defconfig BR2_DEFCONFIG=../mk802ii/mk802ii_buildroot_defconfig O=../mk802ii/**
