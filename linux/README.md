# Ubuntu Dual Boot Steps

* We will be installing Ubuntu 18.04 so we can use ROS melodic.

## Requirements:
* A computer preinstalled with Windows
* Internet connection
* A 8GB+ USB stick
* [Rufus](https://rufus.ie/)

## Steps:

### 1. Format your USB
* Go to Library, select your USB, choose format.
* Choose FAT32 for File System then format.

### 2. Allocate space for Linux.
* Try to allocated around 75GB to 100GB total.
* Go to Create and format hard disk partitions.
* On your volume choose Shrink Volume then enter the amount of space to shrink.

### 3. Install Ubuntu
#### Make your flash drive a boot device.
* Get the [.iso](https://ubuntu.com/download/desktop).
* Use Rufus and burn the iso image to the stick. Make your file system FAT32.

#### Boot from the USB drive
* In BIOS, enable Boot from USB and set it to boot from your USB. 
* Restart to enter Ubuntu.
* Once it loads, choose Install Ubuntu.
* Continue following instructions until "Installation Type". Once you're there, choose "Something Else".

#### Custom Partitioning
* Select the free space you allocated in Step 2.
* Click on the "+" button, select "/" and give it about 20GB.
* Repeat this for /home and /swap. Give /swap around 8-16GB and give /home the rest.
* Complete installation by following the rest of the instructions.
            
## After Installation and Troubleshooting
Now you should be able to dual boot Windows and Linux!. I recommend you to check out the [troubleshooting guide](TROUBLESHOOT.md) after if you have any errors while following the steps above or would like to fix any bugs you may have in Ubuntu.
