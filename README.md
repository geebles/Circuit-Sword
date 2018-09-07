# Circuit-Sword
Kite's Circuit Sword

Welcome to the software repository for Kite's Circuit Sword. This repo contains most/all of the software for the large all-in-one handheld gaming circuit boards, known as the Circuit Sword.

_PRE-ORDER SIGN UP NOTIFICATION: https://goo.gl/forms/e97uUvPOfUxPWdz82_

![](https://i.imgur.com/ibdWkuw.png) Follow me on Instagram: http://instagram.com/kiteretro

![](https://i.imgur.com/s4VyfJG.png) Like my work? Why not buy me a coffee: http://ko-fi.com/kiteretro

# Where do I start?
Start by reading the wiki! It contains everything from the software setup to the hardware guides, and also troubleshooting!

https://github.com/kiteretro/Circuit-Sword/wiki

# Installing the software
Pick ONE of the following:

## Downloading the pre-made images
The easiest way to start is to download the pre-built image from the 'releases' tab:

https://github.com/kiteretro/Circuit-Sword/releases

1. Download the appropriate image for your board, and then unzip and write the .img to an SD card (e.g. using win32diskimager)
2. That's it, power on and you are ready to go! No further steps required!

This image is provided to make it easier to debug and get the thing booted properly. The images were built using the scripts in the `build` directory. You can create your own images with the steps found inside. The source image came from https://retropie.org.uk/

## Installing on top of a fresh retropie installation
NOTE: You should upgrade the kernel to at least 4.14.y and install the RTL8723BS module for Wifi to work!
NOTE: You could do this by following the 'upgrade kernel' steps in the build folder.

1. Download retropie from the official retropie site
2. Unzip and write the .img to an SD card (e.g. using win32diskimager)
3. Boot with HDMI out or so
4. Enable WIFI and SSH (use USB wifi if onboard not detected)
5. `git clone https://github.com/kiteretro/Circuit-Sword`
6. `cd Circuit-Sword`
7. `sudo ./install.sh YES` 
8. `reboot`

## Building your own image
Follow the instructions in the 'build' directory.

# Updating your existing installation
## Updating RetroPie
Update retropie from the main retropie-setup. Once updated and rebooted, you will most likely also need to update the Circuit Sword software (see below) to re-apply any existing fixes that may have been undone by the update.

## Updating the Circuit Sword software
The installation includes an update script! This will perform the necessary actions to pull latest changes and apply them to your running installation.

1. Enable WIFI and SSH
2. `cd Circuit-Sword`
3. `sudo ./update.sh YES`
