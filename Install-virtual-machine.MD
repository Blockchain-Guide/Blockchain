# Overview
* Download virtualbox
* Download ubuntu OS 
* Download Ethereum-Wallet-linux64-0-9-3.zip and  Mist-linux64-0-9-3.zip</br>
https://github.com/ethereum/mist/releases 

ubuntu-16.04.4-desktop-amd64.iso
* Installing 
* Setting share folder between host and virtual host </br>
Then Device-> Insert Guest Addtion CD

Set in the virtualbox -> shared files -> fixed allocation -> right, get the following figure
![path](/picture/Sharefolder-path.png)

* Command
```
kevin@kevin-VirtualBox:~$ sudo mount -t vboxsf share /mnt
[sudo] password for kevin: 
kevin@kevin-VirtualBox:~$ cd /mnt
kevin@kevin-VirtualBox:/mnt$ ls
kevin@kevin-VirtualBox:/mnt$ ls
Ethereum-Wallet-linux64-0-9-3(1).zip
kevin@kevin-VirtualBox:/mnt$ cd /
kevin@kevin-VirtualBox:/$ ls
bin    dev   initrd.img  lost+found  opt   run   srv  usr
boot   etc   lib         media       proc  sbin  sys  var
cdrom  home  lib64       mnt         root  snap  tmp  vmlinuz
kevin@kevin-VirtualBox:/$ cd mnt
kevin@kevin-VirtualBox:/mnt$ ls
Ethereum-Wallet-linux64-0-9-3(1).zip
kevin@kevin-VirtualBox:/mnt$ sudo service ssh restart
[sudo] password for kevin: 
Failed to restart ssh.service: Unit ssh.service not found.
kevin@kevin-VirtualBox:/mnt$ sudo apt-get install openssh-server

kevin@kevin-VirtualBox:/mnt$ sudo service ssh restart
kevin@kevin-VirtualBox:/mnt$ sudo service ssh status
● ssh.service - OpenBSD Secure Shell server
   Loaded: loaded (/lib/systemd/system/ssh.service; enabled; vendor preset: enab
   Active: active (running) since 六 2018-03-03 11:08:31 CST; 13s ago
 Main PID: 3244 (sshd)
   CGroup: /system.slice/ssh.service
           └─3244 /usr/sbin/sshd -D
kevin@kevin-VirtualBox:/mnt$ sudo apt-get install lrzsz -y


```
  
  
