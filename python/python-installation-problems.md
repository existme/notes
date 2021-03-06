# Python-Installation-Problems.Md                                               

## ImportError: No module named 'apt_pkg'
This problem can occur when upgrading to Ubuntu 19:

This solutions worked: 
[linux - python-dev installation error: ImportError: No module named apt_pkg - Stack Overflow][LPDIEINMNASO]

``` sh
sudo apt-get install python3-apt --reinstall
cd /usr/lib/python3/dist-packages
ll apt_pkg*
```
After reinstalling you should have at least a file simlar the following:
``` sh
-rw-r--r-- 1 root 347K Mar 11 12:49 apt_pkg.cpython-37m-x86_64-linux-gnu.so
```
python3-apt checks the highest python version, instead of the current python version in use. So I linked that file to other possible variations:
```
s ln -s apt_pkg.cpython-37m-x86_64-linux-gnu.so apt_pkg.cpython-34m-x86_64-linux-gnu.so
s ln -s apt_pkg.cpython-37m-x86_64-linux-gnu.so apt_pkg.cpython-35m-x86_64-linux-gnu.so
s ln -s apt_pkg.cpython-37m-x86_64-linux-gnu.so apt_pkg.cpython-36m-x86_64-linux-gnu.so
```
so `ls -la apt_pkg` shows:
``` sh
lrwxrwxrwx 1 root   39 May 30 00:52 apt_pkg.cpython-36m-x86_64-linux-gnu.so -> apt_pkg.cpython-37m-x86_64-linux-gnu.so
lrwxrwxrwx 1 root   39 May 30 00:51 apt_pkg.cpython-35m-x86_64-linux-gnu.so -> apt_pkg.cpython-37m-x86_64-linux-gnu.so
lrwxrwxrwx 1 root   39 May 30 00:51 apt_pkg.cpython-34m-x86_64-linux-gnu.so -> apt_pkg.cpython-37m-x86_64-linux-gnu.so
-rw-r--r-- 1 root 9.6K Mar 11 12:49 apt_pkg.pyi
-rw-r--r-- 1 root 347K Mar 11 12:49 apt_pkg.cpython-37m-x86_64-linux-gnu.so
```

##  Installing pygobject
``` bash                                                                          
sudo -H pip install pygobject --upgrade
sudo apt install libgirepository1.0-dev
sudo apt install python3-cairo-dev
```                                                                              

## Using email.Parser
``` bash
sudo -H easy_install --upgrade setuptools
sudo -H easy_install email
```
Also you should change the import from
``` python
import email.Parser
```
to
``` python
from email6.parser import Parser
```

# No module named 'apt_pkg' 
```
sudo apt install --reinstall --purge python-apt
cd /usr/lib/python3/dist-packages
ls -la apt_pkg.cpython-*


sudo ln -s apt_pkg.cpython-37m-x86_64-linux-gnu.so apt_pkg.cpython-34m-x86_64-linux-gnu.so
sudo ln -s apt_pkg.cpython-37m-x86_64-linux-gnu.so apt_pkg.cpython-36m-x86_64-linux-gnu.so
```
# No module named 'dist-util'
``` sh
sudo apt-get install python-distutils python3-distutils python-distutils-extra
```
```
s dpkg -s python3-distutils

Package: python3-distutils
Status: install ok installed
Priority: optional
Section: python
Installed-Size: 1366
Maintainer: Ubuntu Developers <ubuntu-devel-discuss@lists.ubuntu.com>
Architecture: all
Multi-Arch: foreign
Source: python3-stdlib-extensions
Version: 3.7.3-1ubuntu1
Replaces: libpython3.6-stdlib (<< 3.6.4~rc1-2), libpython3.7-stdlib (<< 3.7.0~a3-2)
Provides: python3.7-distutils, python3.8-distutils
Depends: python3 (>= 3.7.1-1~), python3 (<< 3.9), python3-lib2to3 (>= 3.6.4)
Breaks: libpython3.6-stdlib (<< 3.6.5~rc1-3), libpython3.7-stdlib (<< 3.7.0~b2-2)
Description: distutils package for Python 3.x
 Distutils package for Python 3.x.  This package contains the distutils module
 from the Python standard library.
Original-Maintainer: Matthias Klose <doko@debian.org>
```
as you see `python3-distutils` is now broken for this distro so forget running python3.6 on this computer
# Install/uninstalling using specific python settings
``` sh
/usr/bin/python3.6 -m pip install -U pep8 --user 
```

# cannot import name `_gi` from `gi`
``` sh
s -H python3 -m pip uninstall pygobject --upgrade
```
# Othe common python installation problems
[a short guide to install python3 and pip3 on Ubuntu Server · GitHub][ASGTIPAPOUSG]

[LPDIEINMNASO]: https://stackoverflow.com/a/36232975/161312
[ASGTIPAPOUSG]: https://gist.github.com/hadisfr/5c055c2d850cabeecaf51d1b599bd363