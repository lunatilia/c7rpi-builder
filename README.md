## c7rpi-builder

## 内容
c7rpi-builder は、CentOS Userland 7 for Raspberry Pi 2/3 のカスタムイメージを作成するスクリプトです。

## 要件
- CentOS Userland 7 が稼働している Raspberry Pi 2B / 3B / 3B+
    - [SpecialInterestGroup/AltArch/armhfp - CentOS Wiki](https://wiki.centos.org/SpecialInterestGroup/AltArch/armhfp)
    - [公式イメージ](http://isoredirect.centos.org/altarch/7/isos/armhfp)
- root権限
- anaconda、lorax、python-six および依存パッケージがインストールされていること

## 実行例
```
# ./c7rpi-builder kickstarts/c7rpi-ks.cfg
```

## デフォルトからの変更内容
- キーボードと言語を日本語に変更
- タイムゾーンを Asia/Tokyo に変更
- スワップパーティションを削除
- 代わりにスワップファイル管理スクリプトを追加
- cockpit を追加
- yum-utils を追加
- Bluetooth と Wi-Fi を無効化
- history のフォーマットを変更
- EPEL リポジトリを追加
- CR リポジトリを有効化

## イメージ
- [イメージのダウンロード](https://github.com/lunatilia/c7rpi-builder/releases/tag/1.0.0-20190908)

## ライセンス
[GNU General Public License v2.0](https://github.com/lunatilia/c7rpi-builder/blob/master/LICENSE) (The CentOS Projectのデフォルトライセンス)

## スクリプトの実行結果
```
[root@c7rpi-builder workdir]# ./c7rpi-builder kickstarts/c7rpi-ks.cfg
2019-09-08 20:39:47,407: livemedia-creator 19.7.19-1
2019-09-08 20:39:47,773: disk_size = 2GiB
2019-09-08 20:39:47,774: disk_img = /root/devel/workdir/release/CentOS-Userland-7-armhfp-RPi3-Minimal-1810m.raw.img
find_file: stat /proc/device-tree/chosen/bootpath, No such file or directory
Starting installer, one moment...
anaconda argparse: terminal size detection failed, using default width
[Errno 25] Inappropriate ioctl for device
anaconda 21.48.22.147-1 for Red Hat Enterprise Linux 7 (pre-release) started.
20:39:58 Running pre-installation scripts
Starting automated install..............................................................................................
Checking software selection
Generating updated storage configuration
Checking storage configuration...
Your /boot partition is less than 200 MiB which is lower than recommended for a normal Red Hat Enterprise Linux install.
You have not specified a swap partition. Although not strictly required in all cases, it will significantly improve performance for most installations.
================================================================================
================================================================================
Installation

 1) [x] Language settings                 2) [x] Time settings
        (Japanese (Japan))                       (Asia/Tokyo timezone)
 3) [x] Installation source               4) [x] Software selection
        (http://mirror.centos.org/altar          (Custom software selected)
        ch/7/os/armhfp/)                  6) [x] Network configuration
 5) [x] Installation Destination                 (Wired (eth0) connected)
        (Warning checking storage
        configuration)
================================================================================
================================================================================
Progress
Setting up the installation environment
.
Creating disklabel on /dev/mapper/CentOS-Userland-7-armhfp-RPi3-Minimal-1810m.raw
.
Creating ext4 on /dev/mapper/CentOS-Userland-7-armhfp-RPi3-Minimal-1810m.raw2
.
Creating ext4 on /dev/mapper/CentOS-Userland-7-armhfp-RPi3-Minimal-1810m.raw1
.
Running pre-installation scripts
.
Starting package installation process
Preparing transaction from installation source
Installing kbd-misc (1/347)
Installing libreport-filesystem.armv7hl (2/347)
Installing tzdata (3/347)
Installing firewalld-filesystem (4/347)
Installing ncurses-base (5/347)
Installing pcp-conf.armv7hl (6/347)
Installing kbd-legacy (7/347)
Installing raspberrypi2-firmware.armv7hl (8/347)
Installing iwl100-firmware (9/347)
Installing iwl6000-firmware (10/347)
Installing iwl3945-firmware (11/347)
Installing rootfiles (12/347)
Installing iwl5150-firmware (13/347)
Installing iwl6000g2a-firmware (14/347)
Installing iwl2030-firmware (15/347)
Installing iwl1000-firmware (16/347)
Installing iwl135-firmware (17/347)
Installing iwl105-firmware (18/347)
Installing iwl6050-firmware (19/347)
Installing iwl2000-firmware (20/347)
Installing iwl7260-firmware (21/347)
Installing iwl3160-firmware (22/347)
Installing iwl4965-firmware (23/347)
Installing iwl6000g2b-firmware (24/347)
Installing iwl5000-firmware (25/347)
Installing libgcc.armv7hl (26/347)
Installing extlinux-bootloader.armv7hl (27/347)
Installing bash.armv7hl (28/347)
Installing nss-softokn-freebl.armv7hl (29/347)
Installing ncurses.armv7hl (30/347)
Installing chkconfig.armv7hl (31/347)
Installing glibc-common.armv7hl (32/347)
Installing setup (33/347)
Installing filesystem.armv7hl (34/347)
Installing basesystem (35/347)
Installing glibc.armv7hl (36/347)
Installing zlib.armv7hl (37/347)
Installing nspr.armv7hl (38/347)
Installing nss-util.armv7hl (39/347)
Installing libcom_err.armv7hl (40/347)
Installing libstdc++.armv7hl (41/347)
Installing ncurses-libs.armv7hl (42/347)
Installing info.armv7hl (43/347)
Installing popt.armv7hl (44/347)
Installing gawk.armv7hl (45/347)
Installing libsepol.armv7hl (46/347)
Installing libffi.armv7hl (47/347)
Installing libattr.armv7hl (48/347)
Installing libcap.armv7hl (49/347)
Installing libacl.armv7hl (50/347)
Installing pcre.armv7hl (51/347)
Installing libselinux.armv7hl (52/347)
Installing sed.armv7hl (53/347)
Installing grep.armv7hl (54/347)
Installing gmp.armv7hl (55/347)
Installing p11-kit.armv7hl (56/347)
Installing libtasn1.armv7hl (57/347)
Installing p11-kit-trust.armv7hl (58/347)
Installing ca-certificates (59/347)
Installing keyutils-libs.armv7hl (60/347)
Installing libverto.armv7hl (61/347)
Installing centos-userland-release.armv7hl (62/347)
Installing krb5-libs.armv7hl (63/347)
Installing openssl-libs.armv7hl (64/347)
Installing coreutils.armv7hl (65/347)
Installing centos-logos (66/347)
Installing raspberrypi2-kernel.armv7hl (67/347)
Installing linux-firmware (68/347)
Installing xz-libs.armv7hl (69/347)
Installing libuuid.armv7hl (70/347)
Installing libblkid.armv7hl (71/347)
Installing kmod-libs.armv7hl (72/347)
Installing bzip2-libs.armv7hl (73/347)
Installing readline.armv7hl (74/347)
Installing libdb.armv7hl (75/347)
Installing libcap-ng.armv7hl (76/347)
Installing audit-libs.armv7hl (77/347)
Installing libgpg-error.armv7hl (78/347)
Installing libgcrypt.armv7hl (79/347)
Installing sqlite.armv7hl (80/347)
Installing elfutils-libelf.armv7hl (81/347)
Installing libmount.armv7hl (82/347)
Installing gzip.armv7hl (83/347)
Installing findutils.armv7hl (84/347)
Installing cpio.armv7hl (85/347)
Installing expat.armv7hl (86/347)
Installing lua.armv7hl (87/347)
Installing xz.armv7hl (88/347)
Installing libxml2.armv7hl (89/347)
Installing diffutils.armv7hl (90/347)
Installing libaio.armv7hl (91/347)
Installing libnl3.armv7hl (92/347)
Installing cracklib.armv7hl (93/347)
Installing cyrus-sasl-lib.armv7hl (94/347)
Installing libmnl.armv7hl (95/347)
Installing lz4.armv7hl (96/347)
Installing cracklib-dicts.armv7hl (97/347)
Installing libpwquality.armv7hl (98/347)
Installing pam.armv7hl (99/347)
Installing libnl3-cli.armv7hl (100/347)
Installing device-mapper-persistent-data.armv7hl (101/347)
Installing glib2.armv7hl (102/347)
Installing shared-mime-info.armv7hl (103/347)
Installing json-glib.armv7hl (104/347)
Installing gobject-introspection.armv7hl (105/347)
Installing nss-softokn.armv7hl (106/347)
Installing nss-pem.armv7hl (107/347)
Installing nss.armv7hl (108/347)
Installing nss-sysinit.armv7hl (109/347)
Installing libassuan.armv7hl (110/347)
Installing gdisk.armv7hl (111/347)
Installing groff-base.armv7hl (112/347)
Installing libidn.armv7hl (113/347)
Installing which.armv7hl (114/347)
Installing libedit.armv7hl (115/347)
Installing e2fsprogs-libs.armv7hl (116/347)
Installing file-libs.armv7hl (117/347)
Installing ethtool.armv7hl (118/347)
Installing jansson.armv7hl (119/347)
Installing libnfnetlink.armv7hl (120/347)
Installing hostname.armv7hl (121/347)
Installing tcp_wrappers-libs.armv7hl (122/347)
Installing sysvinit-tools.armv7hl (123/347)
Installing gdbm.armv7hl (124/347)
Installing gsettings-desktop-schemas.armv7hl (125/347)
Installing python-libs.armv7hl (126/347)
Installing python.armv7hl (127/347)
Installing python-decorator (128/347)
Installing libxml2-python.armv7hl (129/347)
Installing libselinux-python.armv7hl (130/347)
Installing python-slip (131/347)
Installing python-configobj (132/347)
Installing python-six (133/347)
Installing python-iniparse (134/347)
Installing python-IPy (135/347)
Installing python-chardet (136/347)
Installing python-kitchen (137/347)
Installing python-linux-procfs (138/347)
Installing python2-futures (139/347)
Installing audit-libs-python.armv7hl (140/347)
Installing pygobject2.armv7hl (141/347)
Installing python-gobject-base.armv7hl (142/347)
Installing python-perf.armv7hl (143/347)
Installing yum-metadata-parser.armv7hl (144/347)
Installing pyxattr.armv7hl (145/347)
Installing python-schedutils.armv7hl (146/347)
Installing pyliblzma.armv7hl (147/347)
Installing libnetfilter_conntrack.armv7hl (148/347)
Installing iptables.armv7hl (149/347)
Installing iproute.armv7hl (150/347)
Installing less.armv7hl (151/347)
Installing nss-tools.armv7hl (152/347)
Installing pkgconfig.armv7hl (153/347)
Installing libudisks2.armv7hl (154/347)
Installing libteam.armv7hl (155/347)
Installing ipset-libs.armv7hl (156/347)
Installing ipset.armv7hl (157/347)
Installing setools-libs.armv7hl (158/347)
Installing libdb-utils.armv7hl (159/347)
Installing xfsprogs.armv7hl (160/347)
Installing bzip2.armv7hl (161/347)
Installing logrotate.armv7hl (162/347)
Installing binutils.armv7hl (163/347)
Installing alsa-lib.armv7hl (164/347)
Installing bind-export-libs.armv7hl (165/347)
Installing libssh2.armv7hl (166/347)
Installing libcurl.armv7hl (167/347)
Installing curl.armv7hl (168/347)
Installing rpm-libs.armv7hl (169/347)
Installing rpm.armv7hl (170/347)
Installing openldap.armv7hl (171/347)
Installing libuser.armv7hl (172/347)
Installing python-pycurl.armv7hl (173/347)
Installing python-urlgrabber (174/347)
Installing mariadb-libs.armv7hl (175/347)
Installing fipscheck-lib.armv7hl (176/347)
Installing fipscheck.armv7hl (177/347)
Installing nettle.armv7hl (178/347)
Installing mpfr.armv7hl (179/347)
Installing libbytesize.armv7hl (180/347)
Installing vim-minimal.armv7hl (181/347)
Installing tar.armv7hl (182/347)
Installing libselinux-utils.armv7hl (183/347)
Installing acl.armv7hl (184/347)
Installing make.armv7hl (185/347)
Installing openssl.armv7hl (186/347)
Installing pinentry.armv7hl (187/347)
Installing libmodman.armv7hl (188/347)
Installing libproxy.armv7hl (189/347)
Installing mozjs17.armv7hl (190/347)
Installing libss.armv7hl (191/347)
Installing e2fsprogs.armv7hl (192/347)
Installing libestr.armv7hl (193/347)
Installing libndp.armv7hl (194/347)
Installing dosfstools.armv7hl (195/347)
Installing libfastjson.armv7hl (196/347)
Installing libsmartcols.armv7hl (197/347)
Installing ustr.armv7hl (198/347)
Installing libsemanage.armv7hl (199/347)
Installing shadow-utils.armv7hl (200/347)
Installing libutempter.armv7hl (201/347)
Installing libsemanage-python.armv7hl (202/347)
Installing libpipeline.armv7hl (203/347)
Installing lzo.armv7hl (204/347)
Installing hardlink.armv7hl (205/347)
Installing dtc.armv7hl (206/347)
Installing checkpolicy.armv7hl (207/347)
Installing pth.armv7hl (208/347)
Installing gnupg2.armv7hl (209/347)
Installing gpgme.armv7hl (210/347)
Installing pygpgme.armv7hl (211/347)
Installing rpm-build-libs.armv7hl (212/347)
Installing rpm-python.armv7hl (213/347)
Installing yum-plugin-fastestmirror (214/347)
Installing yum (215/347)
Installing libdaemon.armv7hl (216/347)
Installing slang.armv7hl (217/347)
Installing newt.armv7hl (218/347)
Installing raspberrypi-vc-libs.armv7hl (219/347)
Installing json-c.armv7hl (220/347)
Installing libseccomp.armv7hl (221/347)
Installing lsscsi.armv7hl (222/347)
Installing qrencode-libs.armv7hl (223/347)
Installing yum-utils (224/347)
Installing sos (225/347)
Installing procps-ng.armv7hl (226/347)
Installing util-linux.armv7hl (227/347)
Installing kpartx.armv7hl (228/347)
Installing device-mapper.armv7hl (229/347)
Installing device-mapper-libs.armv7hl (230/347)
Installing cryptsetup-libs.armv7hl (231/347)
Installing dracut.armv7hl (232/347)
Installing kmod.armv7hl (233/347)
Installing elfutils-libs.armv7hl (234/347)
Installing systemd-libs.armv7hl (235/347)
Installing dbus-libs.armv7hl (236/347)
Installing systemd.armv7hl (237/347)
Installing dbus.armv7hl (238/347)
Installing elfutils-default-yama-scope (239/347)
Installing systemd-sysv.armv7hl (240/347)
Installing polkit.armv7hl (241/347)
Installing polkit-pkla-compat.armv7hl (242/347)
Installing policycoreutils.armv7hl (243/347)
Installing dhcp-libs.armv7hl (244/347)
Installing dhcp-common.armv7hl (245/347)
Installing pcp-selinux.armv7hl (246/347)
Installing selinux-policy (247/347)
Installing python-pyudev (248/347)
Installing selinux-policy-targeted (249/347)
Installing aic94xx-firmware (250/347)
Installing dracut-config-rescue.armv7hl (251/347)
Installing cloud-utils-growpart (252/347)
Installing iputils.armv7hl (253/347)
Installing initscripts.armv7hl (254/347)
Installing libgudev1.armv7hl (255/347)
Installing device-mapper-event-libs.armv7hl (256/347)
Installing parted.armv7hl (257/347)
Installing libblockdev-utils.armv7hl (258/347)
Installing wpa_supplicant.armv7hl (259/347)
Installing crontabs (260/347)
Installing cronie-anacron.armv7hl (261/347)
Installing cronie.armv7hl (262/347)
Installing iscsi-initiator-utils-iscsiuio.armv7hl (263/347)
Installing iscsi-initiator-utils.armv7hl (264/347)
Installing NetworkManager-libnm.armv7hl (265/347)
Installing NetworkManager.armv7hl (266/347)
Installing openssh.armv7hl (267/347)
Installing dhclient.armv7hl (268/347)
Installing dracut-network.armv7hl (269/347)
Installing kexec-tools.armv7hl (270/347)
Installing libblockdev-loop.armv7hl (271/347)
Installing libblockdev.armv7hl (272/347)
Installing libblockdev-swap.armv7hl (273/347)
Installing device-mapper-event.armv7hl (274/347)
Installing lvm2-libs.armv7hl (275/347)
Installing lvm2.armv7hl (276/347)
Installing libblockdev-lvm.armv7hl (277/347)
Installing audit.armv7hl (278/347)
Installing PackageKit-glib.armv7hl (279/347)
Installing PackageKit-yum.armv7hl (280/347)
Installing PackageKit.armv7hl (281/347)
Installing libdrm.armv7hl (282/347)
Installing systemd-python.armv7hl (283/347)
Installing uboot-tools.armv7hl (284/347)
Installing ebtables.armv7hl (285/347)
Installing trousers.armv7hl (286/347)
Installing gnutls.armv7hl (287/347)
Installing glib-networking.armv7hl (288/347)
Installing cockpit-bridge.armv7hl (289/347)
Installing cockpit-system (290/347)
Installing cockpit-ws.armv7hl (291/347)
Installing libcgroup.armv7hl (292/347)
Installing policycoreutils-python.armv7hl (293/347)
Installing fxload.armv7hl (294/347)
Installing alsa-firmware (295/347)
Installing alsa-tools-firmware.armv7hl (296/347)
Installing mdadm.armv7hl (297/347)
Installing libblockdev-mdraid.armv7hl (298/347)
Installing teamd.armv7hl (299/347)
Installing avahi-libs.armv7hl (300/347)
Installing pcp-libs.armv7hl (301/347)
Installing pcp.armv7hl (302/347)
Installing dbus-glib.armv7hl (303/347)
Installing dbus-python.armv7hl (304/347)
Installing python-slip-dbus (305/347)
Installing python-firewall (306/347)
Installing setroubleshoot-plugins (307/347)
Installing setroubleshoot-server.armv7hl (308/347)
Installing device-mapper-multipath-libs.armv7hl (309/347)
Installing device-mapper-multipath.armv7hl (310/347)
Installing libblockdev-part.armv7hl (311/347)
Installing libblockdev-fs.armv7hl (312/347)
Installing plymouth-core-libs.armv7hl (313/347)
Installing plymouth-scripts.armv7hl (314/347)
Installing plymouth.armv7hl (315/347)
Installing libatasmart.armv7hl (316/347)
Installing volume_key-libs.armv7hl (317/347)
Installing libblockdev-crypto.armv7hl (318/347)
Installing udisks2.armv7hl (319/347)
Installing udisks2-lvm2.armv7hl (320/347)
Installing udisks2-iscsi.armv7hl (321/347)
Installing virt-what.armv7hl (322/347)
Installing tuned (323/347)
Installing cockpit-storaged (324/347)
Installing firewalld (325/347)
Installing cockpit.armv7hl (326/347)
Installing cockpit-packagekit.armv7hl (327/347)
Installing uboot-images-armv7 (328/347)
Installing cockpit-pcp.armv7hl (329/347)
Installing NetworkManager-team.armv7hl (330/347)
Installing openssh-clients.armv7hl (331/347)
Installing openssh-server.armv7hl (332/347)
Installing NetworkManager-tui.armv7hl (333/347)
Installing NetworkManager-wifi.armv7hl (334/347)
Installing kbd.armv7hl (335/347)
Installing postfix.armv7hl (336/347)
Installing net-tools.armv7hl (337/347)
Installing rsyslog.armv7hl (338/347)
Installing chrony.armv7hl (339/347)
Installing irqbalance.armv7hl (340/347)
Installing iprutils.armv7hl (341/347)
Installing raspberrypi-vc-utils.armv7hl (342/347)
Installing btrfs-progs.armv7hl (343/347)
Installing man-db.armv7hl (344/347)
Installing sudo.armv7hl (345/347)
Installing passwd.armv7hl (346/347)
Installing libsysfs.armv7hl (347/347)
Performing post-installation setup tasks
Installing boot loader
.
Performing post-installation setup tasks
.

Configuring installed system
.
Creating users
.
Configuring addons
.
Generating initramfs
.
Running post-installation scripts
.
find_file: stat /proc/device-tree/chosen/bootpath, No such file or directory
2019-09-08 21:03:09,317: Disk Image install successful
2019-09-08 21:03:09,321: SUMMARY
2019-09-08 21:03:09,322: -------
2019-09-08 21:03:09,323: Logs are in /root/devel/workdir/logs
2019-09-08 21:03:09,323: Disk image is at /root/devel/workdir/release/CentOS-Userland-7-armhfp-RPi3-Minimal-1810m.raw.img
2019-09-08 21:03:09,324: Results are in /root/devel/workdir/release

/dev/loop0
100+0 records in
100+0 records out
104857600 bytes (105 MB) copied, 1.20001 s, 87.4 MB/s
failed to stat() /dev//dev/loop0
mkfs.fat 3.0.20 (12 Jun 2013)
unable to get drive geometry, using default 255/63
/dev/mapper/loop0p1 has 255 heads and 63 sectors per track,
logical sector size is 512,
using 0xf8 media descriptor, with 204800 sectors;
filesystem has 2 16-bit FATs and 4 sectors per cluster.
FAT size is 200 sectors, and provides 51091 clusters.
There is 1 reserved sector.
Root directory contains 512 slots and uses 32 sectors.
Volume ID is e00110f4, no volume label.
Searching for bad blocks
fsck.fat 3.0.20 (12 Jun 2013)
/dev/mapper/loop0p1: 0 files, 0/51091 clusters
E001-10F4

#
# /etc/fstab
# Created by anaconda on Sun Sep  8 20:42:08 2019
#
# Accessible filesystems, by reference, are maintained under '/dev/disk'
# See man pages fstab(5), findfs(8), mount(8) and/or blkid(8) for more info
#
UUID=1948472c-674a-47b3-81fe-5b54705b7fe9 /                       ext4    defaults,noatime 0 0
UUID=E001-10F4                            /boot                   vfat    defaults,noatime 0 0
del devmap : loop0p2
del devmap : loop0p1
loop deleted : /dev/loop0
[root@c7rpi-builder workdir]# 
```
