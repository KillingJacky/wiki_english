---
name: ODYSSEY - X86J4105
category: ODYSSEY
bzurl: https://www.seeedstudio.com/ODYSSEY-X86J4105800-p-4445.html
wikiurl: http://wiki.seeedstudio.com/ODYSSEY-X86J4105-Installing-OS/
sku: 102110399
---

# Creating Bootable USB and Installing OS (Ubuntu Desktop 18.04)

This tutorial demonstrates how to create a bootable USB drive and install Linux OS(Ubuntu Desktop 18.04) onto the ODYSSEY - X86J4105.

## Hardware Requirements

- A Working Computer

- A USB Drive(<8GB is recommended)

- A Monitor

- Keyboard and Mouse

## Creating a Bootable USB

### Step 1 - Download the Operating System Image

Download your required OS Image to your local drive. In this tutorial, *Ubuntu Desktop 18.04* is used to demonstrate to install into the ODYSSEY - X86J4105.

- You can download [Ubuntu](https://ubuntu.com/download/desktop) OS Image from here.

### Step 2 - Prepare your Bootable USB

Format the USB drive. If you are a Windows user, you can format the USB drive by right-clicking the USB Drive and select `Format`.  

**Note:** Choose `FAT32` for the File System.

<div align=center><img width=450 src="https://github.com/SeeedDocument/ODYSSEY-X86J4105864/raw/master/img/InstallingOS/formatUSB.png"/></div>

### Step 3 - Download Flash Burner

Download the Open Source Flash burner [balenaEtcher](https://www.balena.io/etcher/). Download the version according to your operating system(Windows/macOS/Linux).

<div align=center><img width=500 src="https://github.com/SeeedDocument/ODYSSEY-X86J4105864/raw/master/img/InstallingOS/etcher.jpg"/></div>

### Step 4 - Writing the OS Image into USB

Select the downloaded Operating System Image, select the formatted USB Drive and Flash! Now, the bootable USB is all set to go.

<div align=center><img width=500 src="https://github.com/SeeedDocument/ODYSSEY-X86J4105864/raw/master/img/InstallingOS/etcherDone.png"/></div>

## Installing Operating System (Ubuntu)

### Step 1 - Selecting Bootable USB as Boot Device

Plug in your bootable USB, Monitor and keyboard to ODYSSEY - X86J4105, and power up. When booting up, keep pressing **`F7`** to enter the Boot Manager Screen. And use  &#8593; and &#8595; Key on keyboard to select your bootable USB.

In this Tutorial, `UEFI: Mass Storage Device 1.00` is the bootable USB.

<div align=center><img width = 600 src="https://github.com/SeeedDocument/ODYSSEY-X86J4105864/raw/master/img/InstallingOS/bios.png"/></div>

### Step 2 - Installing the OS

Select the **`Install ubuntu`** and press Enter. Follow through the installing instructions on the screen, i.e. system language, user name, location and etc.

**Note:** For detail steps of Installing ubuntu, you can follow [this](https://www.youtube.com/watch?v=vt5Lu_ltPkU) video for more information. *The Installing part starts at 3:20 in the video.*

<div align=center><img width = 600 src="https://github.com/SeeedDocument/ODYSSEY-X86J4105864/raw/master/img/InstallingOS/install.png"/></div>

### Step 3 - Reboot and Enjoy New OS!

If everything goes well, ubuntu should be installed on the ODYSSEY - X86J4105 and you can start enjoying your new OS!

<div align=center><img width = 600 src="https://github.com/SeeedDocument/ODYSSEY-X86J4105864/raw/master/img/InstallingOS/result.jpg"/></div>

## How to Upgrade the BIOS

BIOS is also like an OS and can be upgraded to fix bugs and enhance performance of the RODYSSEY - X86J4105. Here is the instruction how to upgrade the BIOS verison on ODYSSEY - X86J4105:

### Step 1 - Download the newest version of BIOS

Download the newest verison of BIOS from here.

### Step 2 -  Prepare bootable USB

Just like creating a bootable USB for installing OS, format the USB into `FAT32` file system. This time, just unzip the downloaded file and copy the unzipped folder into the USB.

### Step 3 - Upgrading BIOS

Plug the USB into ODYSSEY - X86J4105 and boot up and follow steps below:

- Keep pressing `F7` Key to Enter Boot Manager Screen. Select the `UEFI: Built-in EFI Shell` as boot device and press `Enter`.

<div align=center><img width= 500 src="https://github.com/SeeedDocument/ODYSSEY-X86J4105864/raw/master/img/InstallingOS/upgrading-bios.png"/></div>

- Enter the shell by pressing any key.

<div align=center><img width = 600 src="https://github.com/SeeedDocument/ODYSSEY-X86J4105864/raw/master/img/InstallingOS/process1.png"/></div>

- Enter the USB drive by typing `fs1:` and press `Enter`. Then, use `dir` to check the directories. The folder name will appear and use `cd SD-BS-CJ41G-M101-A` to go into the folder.

**Note:** Can use `tab` to autofill the folder name

<div align=center><img width = 600 src="https://github.com/SeeedDocument/ODYSSEY-X86J4105864/raw/master/img/InstallingOS/process2.png"/></div>

- Once inside this folder, use `dir` again to list out all the files in the folder and use `cd SD-BS-CJ41G-M-101-A` to go in this folder. Use `dir` one more time to list out files in this secondary folder.

<div align=center><img width = 600 src="https://github.com/SeeedDocument/ODYSSEY-X86J4105864/raw/master/img/InstallingOS/process3.png"/></div>

- Run the `BIOS.nsh` and the updating process will begin.

<div align=center><img width = 600 src="https://github.com/SeeedDocument/ODYSSEY-X86J4105864/raw/master/img/InstallingOS/process4.png"/></div>

- The BIOS update will finish in few moments.

<div align=center><img width = 600 src="https://github.com/SeeedDocument/ODYSSEY-X86J4105864/raw/master/img/InstallingOS/biosDone.png"/></div>

### Step 4 - Reboot

When the BIOS is upgraded, reboot the ODYSSEY - X86J4105(Switch on and off the power).

***Note: The first boot up from the BIOS upgrade is relatively long, please be patient to wait, and the installed OS will launch eventually.***

## Notes

- **Ubuntu 16 is not supported by ODYSSEY - X86J4105**

## Tech Support
Please submit any technical issue into our [forum](http://forum.seeedstudio.com/)<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>