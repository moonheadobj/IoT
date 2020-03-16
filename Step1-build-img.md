# IoT Learninng 
## Declear 
* This article is for **academic only** not for **any commerical** use and **only represent** my study. 
* If you have **any** questions, **please feel free** to contact my [Github](https://github.com/moonheadobj) and leave me a message, I will reply one by one. 

#### Keywords 
`Build`, `Compile`, `Openwrt`, `Shell`, `Linux`, `ubuntu`. 

## Enviornment 
If you **not complete** the environment yet, you can read [this](https://github.com/moonheadobj/IoT-Openwrt-Develop/blob/master/README.md) artical.

## About Feeds 
### Introduction
According to  the introduction on the [Openwrt.org](https://openwrt.org/docs/guide-developer/feeds) feeds is a some kind of connector many softwares' resource gather together which are not offical packages `(Third party)`. 
> * In OpenWrt, a “feed” is a collection of packages which share a common location. Feeds may reside on a remote server, in a version control system, on the local filesystem, or in any other location addressable by a single name (path/URL) over a protocol with a supported feed method. 
> * Feeds are additional predefined package build recipes for OpenWrt Buildroot. They may be configured to support custom feeds or non-default feed packages via a feed configuration file. 

## Compile 
Change your Dir to **lede** and **makefile** your config file.

```shell
cd lede
make menuconfig
exit
```

## Install LuCi and Others
**LuCi**: LuCi is an third package, so we use feeds to install it.
```shell
cd lede/scripts 
./feeds update -a 
./feeds install -a
cd ..
make menuconfig
make V=99
```
When it completed you can get your img in your list.

If you need other command you can input: 
```shell
./feeds --help
```
