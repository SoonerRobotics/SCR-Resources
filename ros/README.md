# ROS

## Raspbian Strech Image w/ ROS and OpenCV
https://medium.com/@rosbots/ready-to-use-image-raspbian-stretch-ros-opencv-324d6f8dcd96

### Installation Instructions Link
https://github.com/ROSbots/rosbots_setup_tools
* Use ```dd if="location-of-rosbots-info-file.img" of="/dev/xyz"``` to install the image to SD card. This might take a while and there probably won't be any output until it's done
* Add a file named "ssh" to the boot partition after the above installation completes
* Boot up like the instructions say
* To connect to the pi, use an ethernet cable. On Ubuntu, click on the wifi icon and click `Edit Connections...`. Find the Wired Connection and edit it. Change the IPv4 setting from `Automatic (DHCP)` to `Shared to other computers`.
* Next, we need to find the IP address. Do this by running the `arp` command on Ubuntu (install if needed).
* Follow the link's instructions from step 6 onwards
