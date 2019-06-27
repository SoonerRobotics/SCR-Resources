# Ubuntu Dual Boot Steps

* Note: Use Ubuntu version 16.04 as it supports Kinetic.

## Requirements:
* A computer preinstalled with Windows
* Internet connection
* A 8GB+ USB stick
* Rufus https://rufus.ie/

## Steps:

### 1. Format your USB
* Go to Library, select your USB, choose format.
* Choose FAT32 for File System then format

### 2. Allocate space for Linux.
* Try to allocated around 75GB to 100GB total
* Go to Create and format hard disk partitions
* On your volume choose Shrink Volume then enter the amount of space to shrink.

### 3. Install Ubuntu
#### Make your flash drive a boot device.
* Get the .iso file from http://old-releases.ubuntu.com/releases/16.04.4/
* Use Rufus and burn Ubuntu .iso to the USB using your USB stick and the iso image. Make your file system FAT32

#### Boot from the USB drive
* In BIOS, enable Boot from USB and set it to boot from your USB. 
* Restart to enter Ubuntu
* Once it loads, choose Install Ubuntu
* Continue following instructions until "Installation Type". Once you're there, choose "Something Else"

#### Custom Partitioning
* Select the free space you allocated in Step 2.
* Click on the "+" button, select "/" and give it about 20GB
* Repeat this for /home and /swap. Give /swap around 8-16GB and give /home the rest.
* Complete installation by following the rest of the instructions.
            
### 4. After installation

A bug that you may have with Ubuntu 16.04 is that Ubuntu freezes when you try to shutdown.
#### How to fix:
* Open Ubuntu's Terminal
* Run ```sudo nano etc/default/grub```
* Edit ```GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"``` to ```GRUB_CMDLINE_LINUX_DEFAULT="quiet splash acpi=force"```
* Save using Ctrl+O
* Exit using Ctrl+X
* Run ```update-grub```
        
