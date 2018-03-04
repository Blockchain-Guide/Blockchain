# Overview
1. VirtualBox After installing Ubuntu , the default should be to open a network card, the connection method according to the host computer to connect (if the physical machine is wired through the Internet, you need to use NAT network connection, if it is a wireless network, you need to use the bridge Way Internet), the network card is responsible for the virtual machine's Internet.
2. add a network card, connection options only host (Host-Only) adapter.
3. into the ubuntu system, ifconfig-a, view the current network card information, according to the HWaddr field to see if there are two NICs and VirtualBox inside

* Install geth in the ubuntu OS

```
$ sudo add-apt-repository -y ppa:ethereum/ethereum
$ sudo apt-get update
$ sudo apt-get install ethereum
```

* set network 

![network](/picture/Network.png)

* Set static IP

```
sudo vi /etc/network/interfaces

```

auto enp0s3

iface enp0s3 inet static

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

* restart network or restart computer

```
sudo /etc/init.d/networking restart
or
sudo reboot
```
**helplink:https://www.linuxidc.com/Linux/2016-09/134963.htm**
