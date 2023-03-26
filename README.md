# Rocky Linux Settings

``` bash
$ sudo dnf update kernel && sudo dnf install kernel-devel kernel-headers make bzip2 gcc
```

``` bash
$ sudo dnf group list
```

``` bash
$ sudo dnf groupinstall "Development Tools"
```

``` bash
$ LANG=C xdg-user-dirs-gtk-update
```

``` bash
# as root
rpm --import https://packages.microsoft.com/keys/microsoft.asc
sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'
dnf check-update
dnf install -y code
```

## Refs

[Rocky Linux](https://rockylinux.org/)

[How to Install Visual Studio Code on Rocky Linux EL9 or EL8 - LinuxCapable](https://www.linuxcapable.com/how-to-install-visual-studio-code-on-rocky-linux/)

[GitHub - pyenv/pyenv: Simple Python version management](https://github.com/pyenv/pyenv#switch-between-python-versions)

[【 dnf 】コマンド（応用編その7）――リポジトリを追加する：Linux基本コマンドTips（375） - ＠IT](https://atmarkit.itmedia.co.jp/ait/articles/2001/31/news006.html)

[Virtualbox6.1のGuest AdditionsをOracle Linux 8.6にインストールする - DENの思うこと](https://den2sn.hatenablog.com/entry/2022/06/02/190913)
[VirtualBox Guest Addition がまた壊れたよ。 - Qiita](https://qiita.com/shimon_haga/items/ab416332bdf1481eef00)

[Linuxホームディレクトリの日本語表記を英語表記に変更する | リナスク](https://linuc.spa-miz.com/2021/11/03/changing-the-japanese-representation-of-the-linux-home-directory-to-english-notation/)

[pyenvでのPython仮想環境の作り方まとめ - Qiita](https://qiita.com/ysdyt/items/5008e607343b940b3480)

[WindowsでVSCode+pyenv+venv+pipを使い、Pythonの開発環境を構築する](https://zenn.dev/sion_pn/articles/4418eeda7c62d0)
