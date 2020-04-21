# sunxi_A10_nfs_buildroot
Using MK802ii for tftp, nfs, Shadowsocks-Manager server. Buildroot is used to create rootfs

*https://linux-sunxi.org/BSP*

Using SystemV, Console must set to tty0. Do not use systemD for Linux kernel <3.14

**addusr minxu -G sudo**

default tftp path,(cat /etc/init.d/S80tftpd-hpa)

**/var/lib/tftpboot**

## Buildroot : Using out of tree defconfig
**make defconfig BR2_DEFCONFIG=../mk802ii/mk802ii_buildroot_defconfig O=../mk802ii/**

## trouble shooting
`scripts/mk_livesuit_img.sh: 69: scripts/mk_livesuit_img.sh: /home/mx/sunxi-bsp/allwinner-tools/bins/u_boot_env_gen: not found`

u_boot_env_gen is a 32 bit program, if using 64 bit OS, need to install some libs. for Ubuntu 14.4, use the cmd below,

**apt-get install libc6-i386**
