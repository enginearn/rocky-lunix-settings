# Installl pyenv

``` bash
$ sudo dnf install bzip2-devel libffi-devel   libuuid-devel ncurses-devel openssl-devel readline-devel   sqlite-devel xz-devel zlib-devel tk-devel
```

[CentOS 環境のPython: Python環境構築ガイド - python.jp](https://www.python.jp/install/centos/index.html)

``` bash
$ curl https://pyenv.run | bash
```

``` bash
# .bashrc
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(pyenv init -)"' >> ~/.bashrc
```

``` bash
# .bash_profile or .profile
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bash_profile
echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bash_profile
echo 'eval "$(pyenv init -)"' >> ~/.bash_profile
```

``` bash
source ~/.bashrc ~/.bash_profile
```

``` bash
$ pyenv install 3.11.2
$ pyenv global 3.11.2
```

``` bash
$ python
Python 3.11.2 (main, Mar 26 2023, 18:50:30) [GCC 11.3.1 20220421 (Red Hat 11.3.1-2)] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 
```

---

## Refs

[Rocky Linux - 9.0 - 開発環境 Visual Studio Code](https://freebsd.sing.ne.jp/linux/03/15/13.html)

[GitHub - pyenv/pyenv: Simple Python version management](https://github.com/pyenv/pyenv#installation)

[Building Packages - Rocky Linux Wiki](https://wiki.rockylinux.org/special_interest_groups/sig_guide/build/#dist-tags)

[Projects · Explore · GitLab](https://git.rockylinux.org/explore/projects?non_archived=true&page=2&sort=latest_activity_desc)

[Common build problems · pyenv/pyenv Wiki · GitHub](https://github.com/pyenv/pyenv/wiki/Common-build-problems)

[Install GCC on Rocky Linux PROPERLY [Step-by-Step] | GoLinuxCloud](https://www.golinuxcloud.com/install-gcc-on-rocky-linux/)

[【pyenv】pythonビルド後のModuleNotFoundError: No module named '_sqlite3'](https://zerofromlight.com/blogs/detail/127/)

[RHEL 9 の採用における考慮事項 Red Hat Enterprise Linux 9 | Red Hat Customer Portal](https://access.redhat.com/documentation/ja-jp/red_hat_enterprise_linux/9/html-single/considerations_in_adopting_rhel_9/index)
