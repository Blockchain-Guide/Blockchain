# Overview

* Install geth in the ubuntu OS

```
$ sudo add-apt-repository -y ppa:ethereum/ethereum
$ sudo apt-get update
$ sudo apt-get install ethereum
```

* Set static IP

```
sudo vi /etc/network/interfaces

```

auto eth0

iface eth0 inet static

address 192.168.1.150

netmask 255.255.255.0

gateway 192.168.0.1

```
sudo vi /etc/resolv.conf

```
nameserver 192.168.0.1


* Set static Permanent change

```
sudo vi /etc/resolvconf/resolv.conf.d/base
```

nameserver 192.168.0.1

