# start-http-server.md

Pythonで，簡易的なWebサーバーを立ち上げることができる．本番環境には推奨されない．

## 要件

Pythonがインストールされていること．

### 試した環境

Debian上に構築したKVM（Kernel-based Virtual Machine）による仮想マシン

以下は確認コマンド結果抜粋である。一部を伏せ字にしている。

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

user@hostname:~$ python3 --version
Python 3.13.5

```

## 手順

作業ディレクトリに移動する

```
cd /path/to/working/dir
```

Webサーバーを起動するコマンド

```
python -m http.server
```
しかし`python`ではコマンドが認識されず，以下のように`python3`とするとできた．

```
user@hostname:/path/to/working/dir$ python3 -m http.server
Serving HTTP on 0.0.0.0 port 8000 (http://0.0.0.0:8000/) ...

```

デフォルトでは8000番のポートになっている．ブラウザでローカルホストの8000にアクセスする．なお，httpsではアクセスできなかったのでhttpにする．

```
http://localhost:8000/
```

ポート番号を指定する

```
python -m http.server 8088
```

## 終わるには

WIP
とりあえず`Ctrl+C`

```
^C
Keyboard interrupt received, exiting.
```

## 参考

https://docs.python.org/3/library/http.server.html
https://docs.python.org/ja/3.8/library/http.server.html
https://zenn.dev/enken/articles/enken-python-http-server
