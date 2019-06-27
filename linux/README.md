These are the steps for dual-booting Linux with Windows. 
For any issues, refer to  troubleshooting guide. 

Note: Use Ubuntu version 16.04 as it supports Kinetic.

Requirements:
    A computer preinstalled with Windows
    Internet connection
    A 8GB+ USB stick
    
1.  Format your USB

    A.  Go to Library, select your USB, choose format.
    B.  Choose FAT32 for File System

Install Windows on your machine if it isn't installed already.

2.  Allocate space (around 75GB to 100GB is optimal) for Linux.
    (If you do not need more space, skip this step)

    A.  Go to Create and format hard disk partitions
    B.  Select one of the drives and choose Shrink Volume then enter the amount of space to shrink.

3.  Install Ubuntu

    A.  Make your flash drive an Ubuntu boot device.
        1.  Get the iso from http://old-releases.ubuntu.com/releases/16.04.4/
        2.  Make your USB drive bootable. I used Rufus https://rufus.ie/ but there are others that work too.
            Choose your USB drive, the ISO image, and make your file system FAT32.

    B.  Boot from the USB drive
        1.  In BIOS, enable Boot from USB and set it to boot from your USB. 
        2.  Restart. The computer should be showing various options such as Install Ubuntu, Try Ubuntu without Installing, etc.
        
    C. Download Ubuntu 
        1.  Choose Install Ubuntu
        2.  Follow instructions until Installation Type
        3.  For Installation type, choose Somthing Else
        4.  Select the Free Space. Click on the '+' button.
            a.  Make / 20GB
            b.  Make /swap 8-16GB (look in "Use as")
            c.  The rest of the space goes to /home
            
The rest of the installation instructions are fairly straightforward.
One bug with version 16.04 is that Ubuntu won't let you shutdown.
    
    How to fix:
        1.  Open Terminal
        2.  Run "sudo nano etc/default/grub" (no "")
        3.  Edit: GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"
            to    GRUB_CMDLINE_LINUX_DEFAULT="quiet splash acpi=force"
        4.  Save using ctrl + O
        5.  Exit using ctrl + X
        6. In Terminal, run "update-grub" (again, no "")         