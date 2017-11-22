rtl8188eu
=========

Repository for the stand-alone RTL8188EU driver.

Compiling & Building
---------
### Dependencies
To compile the driver, you need to have make and a compiler installed. In addition,
you must have the kernel headers installed. If you do not understand what this means,
consult your distro.
### Compiling

> make all

### Installing

> sudo make install

DKMS
---------
The module can also be installed with DKMS. Make sure to install the `dkms` package first.

    sudo dkms add ./rtl8188eu
    sudo dkms build 8188eu/1.0
    sudo dkms install 8188eu/1.0

Submitting Issues
---------

Frequently asked Questions
---------

### The network manager says: "Device is not ready"!
Make sure you copied the firmware (rtl8188eufw.bin) to /lib/firmware/rtlwifi/


### Ubuntu 16.04 with kernel 4.4-4.8 Install Method
```
sudo apt-get update
sudo apt-get install git dkms git make build-essential
cd /usr/src
sudo git clone https://github.com/izor/rtl8188eu.git
sudo dkms add ./rtl8188eu
sudo dkms build 8188eu/1.0
sudo dkms install 8188eu/1.0
sudo modprobe 8188eu

