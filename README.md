## RTL8812AU/21AU and RTL8814AU Wireless drivers
Only for use with Linux & Android

[![Monitor mode](https://img.shields.io/badge/monitor%20mode-working-brightgreen.svg)](#)
[![Frame Injection](https://img.shields.io/badge/frame%20injection-working-brightgreen.svg)](#)
[![GitHub version](https://raster.shields.io/badge/version-v5.6.4.2-lightgrey.svg)](#)
[![GitHub issues](https://img.shields.io/github/issues/aircrack-ng/rtl8812au.svg)](https://github.com/aircrack-ng/rtl8812au/issues)
[![GitHub forks](https://img.shields.io/github/forks/aircrack-ng/rtl8812au.svg)](https://github.com/aircrack-ng/rtl8812au/network)
[![GitHub stars](https://img.shields.io/github/stars/aircrack-ng/rtl8812au.svg)](https://github.com/aircrack-ng/rtl8812au/stargazers)
[![Build Status](https://travis-ci.org/aircrack-ng/rtl8812au.svg?branch=v5.6.4.2)](https://travis-ci.org/aircrack-ng/rtl8812au)
[![GitHub license](https://img.shields.io/github/license/aircrack-ng/rtl8812au.svg)](https://github.com/aircrack-ng/rtl8812au/blob/master/LICENSE)
<br>
[![Kali](https://img.shields.io/badge/Kali-supported-blue.svg)](https://www.kali.org)
[![Arch](https://img.shields.io/badge/Arch-supported-blue.svg)](https://www.archlinux.org)
[![Armbian](https://img.shields.io/badge/Armbian-supported-blue.svg)](https://www.armbian.com)
[![ArchLinux](https://img.shields.io/badge/ArchLinux-supported-blue.svg)](https://img.shields.io/badge/ArchLinux-supported-blue.svg)
[![aircrack-ng](https://img.shields.io/badge/aircrack--ng-supported-blue.svg)](https://github.com/aircrack-ng/aircrack-ng)
[![wifite2](https://img.shields.io/badge/wifite2-supported-blue.svg)](https://github.com/kimocoder/wifite2)


### Important!

```
* Use "ip" and "iw" instead of "ifconfig" and "iwconfig"
     It's described further down, READ THE README!
```

> **Note:**  
> It also works on Fedora 38 (for now).

### IPERF3 benchmark

**[Device]** Alfa Networks AWUS036ACH<br>
**[Chipset]** 88XXau (rtl8812au)<br>
**[Branch]** v5.6.4.1<br>
**[Distance]** 10m free sight

```
[ ID] Interval           Transfer     Bitrate         Retr  Cwnd
[  5]   0.00-1.00   sec  11.6 MBytes  97.4 Mbits/sec    0   96.2 KBytes
[  5]   1.00-2.00   sec  11.2 MBytes  93.8 Mbits/sec    0    100 KBytes
[  5]   2.00-3.00   sec  11.2 MBytes  93.8 Mbits/sec    0    100 KBytes
[  5]   3.00-4.00   sec  11.2 MBytes  93.8 Mbits/sec    0    100 KBytes
[  5]   4.00-5.00   sec  11.2 MBytes  93.8 Mbits/sec    0    100 KBytes
[  5]   5.00-6.00   sec  11.4 MBytes  95.9 Mbits/sec    0    105 KBytes
[  5]   6.00-7.00   sec  11.2 MBytes  93.8 Mbits/sec    0    105 KBytes
[  5]   7.00-8.00   sec  11.3 MBytes  94.9 Mbits/sec    0    157 KBytes
[  5]   8.00-9.00   sec  11.2 MBytes  93.8 Mbits/sec    0    157 KBytes
[  5]   9.00-10.00  sec  11.2 MBytes  94.3 Mbits/sec    0    157 KBytes
[  5]  10.00-11.00  sec  11.2 MBytes  93.8 Mbits/sec    0    157 KBytes
[  5]  11.00-12.00  sec  11.2 MBytes  93.8 Mbits/sec    0    157 KBytes
[  5]  12.00-13.00  sec  11.2 MBytes  94.4 Mbits/sec    0    157 KBytes
[  5]  13.00-14.00  sec  11.2 MBytes  93.8 Mbits/sec    0    157 KBytes
[  5]  14.00-15.00  sec  11.2 MBytes  94.4 Mbits/sec    0    157 KBytes
[  5]  15.00-16.00  sec  10.9 MBytes  91.7 Mbits/sec    0    157 KBytes
[  5]  16.00-17.00  sec  11.2 MBytes  94.4 Mbits/sec    0    157 KBytes
[  5]  17.00-18.00  sec  11.2 MBytes  94.4 Mbits/sec    0    157 KBytes
[  5]  18.00-19.00  sec  11.2 MBytes  94.4 Mbits/sec    0    157 KBytes
[  5]  19.00-20.00  sec  11.2 MBytes  93.8 Mbits/sec    0    157 KBytes
[  5]  20.00-21.00  sec  11.2 MBytes  93.8 Mbits/sec    0    157 KBytes
[  5]  21.00-22.00  sec  11.2 MBytes  93.8 Mbits/sec    0    157 KBytes
[  5]  22.00-23.00  sec  11.2 MBytes  93.8 Mbits/sec    0    157 KBytes
- - - - - - - - - - - - - - - - - - - - - - - - -
[ ID] Interval           Transfer     Bitrate         Retr
[  5]   0.00-23.15  sec   260 MBytes  94.2 Mbits/sec    0             sender
[  5]   0.00-23.15  sec  0.00 Bytes  0.00 bits/sec                  receiver
```

### DKMS
This driver can be installed using [DKMS]. This is a system which will automatically recompile and install a kernel module when a new kernel gets installed or updated. To make use of DKMS, install the `dkms` package, which on Debian (based) systems is done like this:
```
$ sudo apt-get install dkms
```

### Download
```
$ git clone -b v5.6.4.2 https://github.com/aircrack-ng/rtl8812au.git
cd rtl*
```

### Installation of Driver
In order to install the driver open a terminal in the directory with the source code and execute the following command:
```
$ sudo make dkms_install
```

### Removal of Driver
In order to remove the driver from your system open a terminal in the directory with the source code and execute the following command:
```
$ sudo make dkms_remove
```

### Make
For building & installing the driver with 'make' use
```
$ make && make install
```

Package / Build dependencies (Kali)
```
$ sudo apt-get update
$ sudo apt-get install bc mokutil build-essential libelf-dev linux-headers-`uname -r`
```
#### For Raspberry (RPI)

```
$ sudo apt-get install raspberrypi-kernel-headers
```

Then change the platform in Makefile to 32-bit `ARM` architecture (RPi 1/2/3/ & 0/Zero):
```
$ sed -i 's/CONFIG_PLATFORM_I386_PC = y/CONFIG_PLATFORM_I386_PC = n/g' Makefile
$ sed -i 's/CONFIG_PLATFORM_ARM_RPI = n/CONFIG_PLATFORM_ARM_RPI = y/g' Makefile
```

Or, for `ARM64` (RPI 3B+, 4B and Zero2) you will need to run:
```
$ sed -i 's/CONFIG_PLATFORM_I386_PC = y/CONFIG_PLATFORM_I386_PC = n/g' Makefile
$ sed -i 's/CONFIG_PLATFORM_ARM64_RPI = n/CONFIG_PLATFORM_ARM64_RPI = y/g' Makefile
```

In addition, if you receive an error message about `unrecognized command line option ‘-mgeneral-regs-only’` (i.e., Raspbian Buster), you will need to run the following commands for `ARM` architecture, then retry building and installing:
```
$ export ARCH=arm
$ sed -i 's/^MAKE="/MAKE="ARCH=arm\ /' dkms.conf
```

Or, for `ARM64` run the following before re-building:

```
$ export ARCH=arm64
$ sed -i 's/^MAKE="/MAKE="ARCH=arm64\ /' dkms.conf
```

Building the driver may exceed RAM on some RPi's resulting in a `gcc: fatal error: Killed signal terminated program cc1` error.  Swap space can be increased in `/etc/dphys-swapfile` e.g. to `2000` megabytes, followed by `/etc/init.d/dphys-swapfile restart`. Building on swap is very slow, however.

For setting monitor mode
  1. Fix problematic interference in monitor mode.
  ```
  $ airmon-ng check kill
  ```
  You may also uncheck the box "Automatically connect to this network when it is avaiable" in nm-connection-editor. This only works if you have a saved wifi connection.

  2. Set interface down
  ```
  $ sudo ip link set wlan0 down
  ```
  3. Set monitor mode
  ```
  $ sudo iw dev wlan0 set type monitor
  ```
  4. Set interface up
  ```
  $ sudo ip link set wlan0 up
  ```
For setting TX power
```
$ sudo iw wlan0 set txpower fixed 3000
```

### LED control

#### statically by module parameter in /etc/modprobe.d/8812au.conf or wherever, for example:

```sh
options 88XXau rtw_led_ctrl=0
```
value can be 0 or 1

#### or dynamically by writing to /proc/net/rtl8812au/$(your interface name)/led_ctrl, for example:

```sh
$ echo "0" > /proc/net/rtl8812au/$(your interface name)/led_ctrl
```
value can be 0 or 1

#### check current value:

```sh
$ cat /proc/net/rtl8812au/$(your interface name)/led_ctrl
```

### USB Mode Switch

0: doesn't switch, 1: switch from usb2.0 to usb 3.0 2: switch from usb3.0 to usb 2.0
```sh
$ rmmod 88XXau
$ modprobe 88XXau rtw_switch_usb_mode=int (0: no switch 1: switch from usb2 to usb3 2: switch from usb3 to usb2)
```

### NetworkManager

Newer versions of NetworkManager switches to random MAC address. Some users would prefer to use a fixed address.
Simply add these lines below
```
[device]
wifi.scan-rand-mac-address=no
```
at the end of file /etc/NetworkManager/NetworkManager.conf and restart NetworkManager with the command:
```
$ sudo service NetworkManager restart
```

### Credits / Contributors

```
Alfa Networks - https://www.alfa.com.tw/
Realtek.      - https://www.realtek.com
aircrack-ng   - https://www.aircrack-ng.org

astsam        - https://github.com/astsam
evilphish     - https://github.com/evilphish
fariouche     - https://github.com/fariouche
CGarces       - https://github.com/CGarces
ZerBea        - https://github.com/ZerBea
lwfinger      - https://github.com/lwfinger
Ulli-Kroll.   - https://github.com/Ulli-Kroll

```
