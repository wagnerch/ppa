# Debian Buster PPA

This repository contains the GNU C library forked from Debian glibc 2.28-10 with some additional patches to support Widevine 4.10.2252.0 or later on ARM-based devices.

```sh
wget -qO - https://wagnerch.github.io/ppa/buster/KEY.gpg |sudo apt-key add -
sudo wget -qO /etc/apt/sources.list.d/wagnerch-buster-ppa.list https://wagnerch.github.io/ppa/buster/wagnerch-buster-ppa.list
sudo apt update && sudo apt upgrade
```

You may still need to install Widevine 4.10.2252.0 manually, since some add-ons like InputStream Helper require certain assertions provided by the operating system or Kodi startup scripts to make it aware that the system is compatible with the requirements of the later Widevine libraries.  Unfortunately those assertions are not provided by this repository, in order to prevent the risk of other unforseen incompatibilities.

The additional patches applied to Debian glibc 2.28-10 can be found [here](https://github.com/wagnerch/glibc-deb/compare/debian/2.28-10...buster-widevine)

