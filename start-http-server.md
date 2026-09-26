# start-http-server.md

start-http-server.md

## 要件

Pythonがインストールされていること．

以下は試した環境Debianでの確認コマンド結果抜粋である。一部を伏せ字にしている。

```
user@hostname:~$ cat /etc/*release*
PRETTY_NAME="Debian GNU/Linux 13 (trixie)"
NAME="Debian GNU/Linux"
VERSION_ID="13"
VERSION="13 (trixie)"
VERSION_CODENAME=trixie
DEBIAN_VERSION_FULL=13.7
ID=debian
HOME_URL="https://www.debian.org/"
SUPPORT_URL="https://www.debian.org/support"
BUG_REPORT_URL="https://bugs.debian.org/"

user@hostname:~$ hostnamectl
 Static hostname: hostname
       Icon name: computer-vm
         Chassis: vm 🖴
      Machine ID: ********************************
         Boot ID: ********************************
  Virtualization: kvm
Operating System: Debian GNU/Linux 13 (trixie)    
          Kernel: Linux 6.12.107+deb13-amd64
    Architecture: x86-64
 Hardware Vendor: QEMU
  Hardware Model: Standard PC _Q35 + ICH9, 2009_
Firmware Version: 1.16.3-debian-1.16.3-2
   Firmware Date: Tue 2014-04-01
    Firmware Age: 12y 5month 3w 4d                

user@deb132609241254:~$ python3 --version
Python 3.13.5

```

## 手順


## 終わるには

## 参考

https://docs.python.org/3/library/http.server.html
https://docs.python.org/ja/3.8/library/http.server.html
https://zenn.dev/enken/articles/enken-python-http-server
