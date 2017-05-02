## Connect to Raspberry Pi 3 using SSH on a Mac or Linux

This is a guide that will show you how to connect to a Raspberry Pi 3, Headless [Using SSH]. 

### What you'll need
* Raspberry Pi 3
* Ethernet Cable [For sometime]
* A laptop / desktop with Linux or Mac operating system, Which is also connected to the network. 
* A SD card with an OS installed in it
* Micro USB cable

### STEP 1 - SETUP
* Plugin your SD card to your Raspberry Pi 3
* Connect the Ethernet cable to your Raspberry Pi 3
* Connect the Micro USB cable to the Raspberry Pi 3
* There will be a ![#f03c15](https://placehold.it/15/f03c15/000000?text=+) RED LIGHT which indicates the Raspberry Pi 3 is powered up. 
* The ![#c5f015](https://placehold.it/15/c5f015/000000?text=+) GREEN LIGHT indicates that the OS is booting up

## STEP 2 - TERMINAL COMMANDS 
The following steps should be continued on your laptop / desktop which is connected to the same network as your Raspberry Pi 3. 
* To find the IP ADDRESS of your Raspberry Pi 3
```bash
ping raspberrypi.local
```
* The keyword: *raspberrypi.local* depends on each operating system, Since I am using *Rasbian OS*, it is *raspberrypi.local*. 
* This will return some IP ADDRESSES
```bash 
PING raspberrypi.local (192.168.xx.xx): 56 data bytes
64 bytes from 192.168.xx.xx: icmp_seq=0 ttl=64 time=89.882 ms
64 bytes from 192.168.xx.xx: icmp_seq=1 ttl=64 time=6.234 ms
64 bytes from 192.168.xx.xx: icmp_seq=2 ttl=64 time=5.680 ms
64 bytes from 192.168.xx.xx: icmp_seq=3 ttl=64 time=7.551 ms
```
* In place of xx.xx you will have some number, Which will look something like 192.168.1.11, That is the IP ADDRESS of your Raspberry Pi 3. 
* You have to connect to that IP ADDRESS using `ssh`
```bash
ssh pi@192.168.xx.xx
```
* Here the `pi` from `pi@192.168.xx.xx` can differ according to the OS, Since the default username of *Rasbian OS* is `pi`, I am using `pi` here, If you are using any other operating system, Please do check what the default username is. It will look something like `ssh <username>@IP-ADDRESS-OF-YOUR-PI`
* They might ask you a *yes-or-no* question, Answer *yes* by typing it on your keyboard
* That will be followed by a propmpt to enter the password, The default password of *Rasbian OS* is `raspberry`, Please do check what the default password of your OS is and enter it over there. 
* It will look something like. 
```bash
pi@192.168.1.11's password: ▓
```
* Enter the password there
* You will be logged into the Raspberry Pi
