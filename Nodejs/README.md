# Node.js

## Install nodejs npm latest

``` bash
$ dnf info nodejs
Rocky Linux 9 - BaseOS                          1.5 MB/s | 1.8 MB     00:01    
Rocky Linux 9 - AppStream                       2.2 MB/s | 6.6 MB     00:03    
Rocky Linux 9 - Extras                          7.3 kB/s | 8.5 kB     00:01    
packages.microsoft.com                          173  B/s | 481  B     00:02    
packages.microsoft.com                          2.2 kB/s | 983  B     00:00    
GPG 鍵 0xBE1229CF をインポート中:
 Userid     : "Microsoft (Release signing) <gpgsecurity@microsoft.com>"
 Fingerprint: BC52 8686 B50D 79E3 39D3 721C EB3E 94AD BE12 29CF
 From       : https://packages.microsoft.com/keys/microsoft.asc
これでよろしいですか? [y/N]: y
packages.microsoft.com                          2.4 MB/s |  33 MB     00:13    
利用可能なパッケージ
名前         : nodejs
エポック     : 1
バージョン   : 16.18.1
リリース     : 3.el9_1
Arch         : x86_64
サイズ       : 111 k
ソース       : nodejs-16.18.1-3.el9_1.src.rpm
リポジトリー : appstream
概要         : JavaScript runtime
URL          : http://nodejs.org/
ライセンス   : MIT and ASL 2.0 and ISC and BSD
説明         : Node.js is a platform built on Chrome's JavaScript runtime
             : for easily building fast, scalable network applications.
             : Node.js uses an event-driven, non-blocking I/O model that
             : makes it lightweight and efficient, perfect for data-intensive
             : real-time applications that run across distributed devices.
```

``` bash
$ cd ~ && \
curl -sL https://rpm.nodesource.com/setup_18.x -o nodesource_setup.sh
```

``` bash
$ sudo bash nodesource_setup.sh 
[sudo] rocky のパスワード:

## Installing the NodeSource Node.js 18.x repo...


## Inspecting system...

+ rpm -q --whatprovides redhat-release || rpm -q --whatprovides centos-release || rpm -q --whatprovides cloudlinux-release || rpm -q --whatprovides sl-release || rpm -q --whatprovides fedora-release
+ uname -m

## Confirming "el9-x86_64" is supported...

+ curl -sLf -o /dev/null 'https://rpm.nodesource.com/pub_18.x/el/9/x86_64/nodesource-release-el9-1.noarch.rpm'

## Downloading release setup RPM...

+ mktemp
+ curl -sL -o '/tmp/tmp.F6Ubh96dBo' 'https://rpm.nodesource.com/pub_18.x/el/9/x86_64/nodesource-release-el9-1.noarch.rpm'

## Installing release setup RPM...

+ rpm -i --nosignature --force '/tmp/tmp.F6Ubh96dBo'

## Cleaning up...

+ rm -f '/tmp/tmp.F6Ubh96dBo'

## Checking for existing installations...

+ rpm -qa 'node|npm' | grep -v nodesource

## Run `sudo yum install -y nodejs` to install Node.js 18.x and npm.
## You may run dnf if yum is not available:
     sudo dnf install -y nodejs
## You may also need development tools to build native addons:
     sudo yum install gcc-c++ make
## To install the Yarn package manager, run:
     curl -sL https://dl.yarnpkg.com/rpm/yarn.repo | sudo tee /etc/yum.repos.d/yarn.repo
     sudo yum install yarn
```

``` bash
$ make --version
GNU Make 4.3
このプログラムは x86_64-redhat-linux-gnu 用にビルドされました
Copyright (C) 1988-2020 Free Software Foundation, Inc.
ライセンス GPLv3+: GNU GPL バージョン 3 以降 <http://gnu.org/licenses/gpl.html>
これはフリーソフトウェアです: 自由に変更および配布できます.
法律の許す限り、　無保証　です.
```

``` bash
$ sudo dnf install gcc-c++
Node.js Packages for Enterprise Linux 9 - x86_6 871 kB/s | 538 kB     00:00    
依存関係が解決しました。
================================================================================
 パッケージ            Arch         バージョン            リポジトリー    サイズ
================================================================================
インストール:
 gcc-c++               x86_64       11.3.1-2.1.el9        appstream        13 M
依存関係のインストール:
 libstdc++-devel       x86_64       11.3.1-2.1.el9        appstream       2.2 M

トランザクションの概要
================================================================================
インストール  2 パッケージ

ダウンロードサイズの合計: 15 M
インストール後のサイズ: 45 M
これでよろしいですか? [y/N]: y
パッケージのダウンロード:
(1/2): libstdc++-devel-11.3.1-2.1.el9.x86_64.rp 2.2 MB/s | 2.2 MB     00:00    
(2/2): gcc-c++-11.3.1-2.1.el9.x86_64.rpm        4.3 MB/s |  13 MB     00:02    
--------------------------------------------------------------------------------
合計                                            4.3 MB/s |  15 MB     00:03     
トランザクションの確認を実行中
トランザクションの確認に成功しました。
トランザクションのテストを実行中
トランザクションのテストに成功しました。
トランザクションを実行中
  準備             :                                                        1/1 
  インストール中   : libstdc++-devel-11.3.1-2.1.el9.x86_64                  1/2 
  インストール中   : gcc-c++-11.3.1-2.1.el9.x86_64                          2/2 
  scriptletの実行中: gcc-c++-11.3.1-2.1.el9.x86_64                          2/2 
  検証             : libstdc++-devel-11.3.1-2.1.el9.x86_64                  1/2 
  検証             : gcc-c++-11.3.1-2.1.el9.x86_64                          2/2 

インストール済み:
  gcc-c++-11.3.1-2.1.el9.x86_64      libstdc++-devel-11.3.1-2.1.el9.x86_64     

完了しました!
```

``` bash
$ sudo dnf install nodejs
メタデータの期限切れの最終確認: 0:04:56 時間前の 2023年03月25日 00時15分25秒 に実施しました。
依存関係が解決しました。
================================================================================
 パッケージ   Arch         バージョン                    リポジトリー     サイズ
================================================================================
インストール:
 nodejs       x86_64       2:18.15.0-1nodesource         nodesource        34 M

トランザクションの概要
================================================================================
インストール  1 パッケージ

ダウンロードサイズの合計: 34 M
インストール後のサイズ: 99 M
これでよろしいですか? [y/N]: y
パッケージのダウンロード:
nodejs-18.15.0-1nodesource.x86_64.rpm           3.3 MB/s |  34 MB     00:10    
--------------------------------------------------------------------------------
合計                                            3.3 MB/s |  34 MB     00:10     
Node.js Packages for Enterprise Linux 9 - x86_6 1.5 MB/s | 1.6 kB     00:00    
GPG 鍵 0x34FA74DD をインポート中:
 Userid     : "NodeSource <gpg-rpm@nodesource.com>"
 Fingerprint: 2E55 207A 95D9 944B 0CC9 3261 5DDB E8D4 34FA 74DD
 From       : /etc/pki/rpm-gpg/NODESOURCE-GPG-SIGNING-KEY-EL
これでよろしいですか? [y/N]: y
鍵のインポートに成功しました
トランザクションの確認を実行中
トランザクションの確認に成功しました。
トランザクションのテストを実行中
トランザクションのテストに成功しました。
トランザクションを実行中
  準備             :                                                        1/1 
  scriptletの実行中: nodejs-2:18.15.0-1nodesource.x86_64                    1/1 
  インストール中   : nodejs-2:18.15.0-1nodesource.x86_64                    1/1 
  scriptletの実行中: nodejs-2:18.15.0-1nodesource.x86_64                    1/1 
  検証             : nodejs-2:18.15.0-1nodesource.x86_64                    1/1 

インストール済み:
  nodejs-2:18.15.0-1nodesource.x86_64                                           

完了しました!
```

``` bash
$ npm -v
9.5.0
$ sudo npm install -g npm@latest
[sudo] rocky のパスワード:

changed 29 packages in 6s

16 packages are looking for funding
  run `npm fund` for details
$ npm -v
9.6.2
```

``` bash
$ which node
/usr/bin/node
```

``` bash
$ which npm
/usr/bin/npm
```

---

## Refs

[nodesource/distributions ](https://github.com/nodesource/distributions)

[How To Install Node.js on Rocky Linux 8](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-rocky-linux-8)