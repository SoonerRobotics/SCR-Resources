# Troubleshoting Guide
Read this for solutions to your Linux installation errors

## Errors while creating live USB
#### Check for following:
* Make sure your image is an .iso file. If it's .iso.torrent, use BitTorrent https://www.bittorrent.com/ to obtain the image.
* Your USB is formatted

## Errors while freeing space for Linux
* Ensure you have enough space to free on your computer.
* Freed space doesn't need to be formatted or used to create a new volume

## Ubuntu won't launch on startup
* Make sure the USB is to be booted in BIOS
* Make sure the USB is created correctly

## Ubuntu's "Installation Type" is empty
* Go to cmd
* Run ```bcdedit /set {current} safeboot minimal``` to enable safe boot
* Go to BIOS
* Switch SATA Controller to AHCI
* Reboot computer
* Go to cmd and run ```bcdedit /deletevalue {current} safeboot``` to disable safe boot
* Restart and Windows should start with AHCI drivers

## Ubuntu freezes when you shut down
* Open Ubuntu's Terminal
* Run ```sudo nano etc/default/grub```
* Edit ```GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"``` to ```GRUB_CMDLINE_LINUX_DEFAULT="quiet splash acpi=force"```
* Save using Ctrl+O
* Exit using Ctrl+X
* Run ```update-grub```

## Switching from Ubuntu to Windows changes Windows time
// TODO

