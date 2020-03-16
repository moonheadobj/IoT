
## Overview  
### Laboratory Equipment 
#### GL-iNet 


Name | Paramater
----- | -----
Modle | GL-MIFI
WiFi Support | 802.11b/n/g, 2.4Ghz
Firmware | GL-iNet-6416A

* [gl-inet-6416A](https://downloads.openwrt.org/releases/18.06.6/targets/ar71xx/generic/openwrt-18.06.6-ar71xx-generic-gl-inet-6416A-v1-squashfs-sysupgrade.bin), *maybe i didn't figure it out.* 
***
#### Virtual Machine 
* VMware Workstation, 15.0.2 build-10952284
* Linux, Ubuntu 16.04 Lts

## Enviornment Building 
### Linux 
***
#### Install
> For Ubuntu 16.04
```cmd
sudo apt install 
sudo apt install gcc g++ binutils patch bzip2 flex bison make autoconf gettext texinfo unzip sharutils libncurses5-dev ncurses-term zlib1g-dev gawk asciidoc libz-dev git-core uuid-dev libacl1-dev liblzo2-dev pkg-config libc6-dev curl libxml-parser-perl ocaml-nox
``` 


No. | Terminals | No. | Terminals
----- | ----- | ----- |----- 
1 | gcc | 2 | g++ 
3 | binutils | 4 | patch 
5 | bzip2 | 6 | flex 
7 | bison | 8 | make 
9 | autoconf | 10 | gettext 
11 | texinfo | 12 | unzip 
13 | sharutils | 14 | libncurses5-dev 
15 | ncurses-term | 16 | zlib1g-dev 
17 | gawk | 18 | asciidoc 
19 | libz-dev | 20 | git-core 
21 | uuid-dev | 22 | libacl1-dev 
23 | liblzo2-dev | 24 | pkg-config 
25 | libc6-dev | 26 | curl 
27 | libxml-parser-perl | 28 | ocaml-nox

> For Ubuntu 18.04 
```cmd
sudo apt install subversion build-essential libncurses5-dev zlib1g-dev gawk git ccache gettext libssl-dev xsltproc zip
```


No. | Terminals | No. | Terminals
----- | ----- | ----- |----- 
1 | subversion | 2 | build-essential 
3 | libncurses5-dev | 4 | zlib1g-dev 
5 | gawk | 6 | git 
7 | ccache | 8 | gettext 
9 | libssl-dev | 10 | xsltproc 
11 | zip 

#### Update & Upgrade 
```cmd
sudo apt update 
sudo apt upgrade 
```
***
### Openwrt 
To download Openwrt [Lede](https://git.lede-project.org/source.git). 
According to your own reality checkout [git summary](https://git.archive.openwrt.org/openwrt.git).
```cmd
git clone https://git.lede-project.org/source.git lede 
git clone git://git.openwrt.org/openwrt.git 
cd  lede 
make menuconfig
```
***
### Compile System & Check Prerequisites 
```
make V=99 or else make -j2 | V=s 
make prereq 
```
## Reference
* CN Developer: `ForgotFun` 
    * [Github](https://github.com/forgotfun) 
    * [Blog](http://forgotfun.org)

* Offical Firmware: `Openwrt` 
    * [Website](https://openwrt.org/docs/guide-developer/build-system/install-buildsystem) 
    * [Repository](https://git.archive.openwrt.org/openwrt.git)
