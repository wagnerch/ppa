# Debian Buster PPA

```sh
curl -s --compressed "https://wagnerch.github.io/ppa/buster/KEY.gpg" | sudo apt-key add -
sudo curl -s --compressed -o /etc/apt/sources.list.d/wagnerch-buster-ppa.list "https://wagnerch.github.io/ppa/buster/wagnerch-buster-ppa.list"
sudo apt update
```
