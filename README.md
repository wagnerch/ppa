# Debian Buster PPA

This repository contains the GNU C library forked from Debian glibc 2.28-10 with some additional patches to support Widevine 4.10.2252.0 or later on ARM-based devices.

This PPA is not required for the following Debian Buster derivative operating systems:
* Raspberry Pi OS 10 (Buster), libc6 2.28-10+rpt2+rpi1 or later.  Available through regular OS update channels (apt).
* OSMC (Kodi 19), libc6 2.28-110.1 or later.  See [here](https://discourse.osmc.tv/t/widevine-add-ons-stopped-working-from-01-09/90684) for instructions.

```sh
wget -qO - https://wagnerch.github.io/ppa/buster/KEY.gpg |sudo apt-key add -
sudo wget -qO /etc/apt/sources.list.d/wagnerch-buster-ppa.list https://wagnerch.github.io/ppa/buster/wagnerch-buster-ppa.list
sudo apt update && sudo apt upgrade
```

You may still need to install Widevine 4.10.2252.0 manually.


The additional patches applied to Debian glibc 2.28-10 can be found [here](https://github.com/wagnerch/glibc-deb/compare/debian/2.28-10...buster-widevine).

