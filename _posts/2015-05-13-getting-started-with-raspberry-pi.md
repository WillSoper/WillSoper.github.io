---
layout: post
title: Getting started with Raspberry Pi
---
This is part of a series of posts detailing my adventures with a raspberry pi. [You can find the whole series here.]({% post_url 2015-05-13-adventures-with-raspberry-pi %})
##What you'll need:

- Raspberry Pi (I'm using the version 2)
- 8GB MicroSD card (or bigger)
- USB MicroSD reader (for writing Raspbian to the SD card)
- Micro USB charger (for powering the Raspberry Pi)

You *might* need the following, it depends how well things go:

- HDMI cable (and a monitor or TV to plug it in to)
- USB keyboard and mouse

##What to do:

###Download and install Raspbian on to the MicroSD card

You can find up to date instructions for installing an operating system on the [Raspberry Pi website](https://www.raspberrypi.org/). 

The simplest option is to use NOOBS (there's a great guide with multiple options for getting [NOOBS directly on the Raspberry Pi website](https://www.raspberrypi.org/help/noobs-setup/)); it gives you multiple operating systems, and it's really simple to configure on your computer.

I'm not using the simplest option however, I'm installing Raspbian directly without using NOOBS, because I don't need any of the alternative Operating Systems that NOOBS offers, and I'd like to save the space that it takes up.

I'm using Windows to prepare my SD card, and on the Raspberry Pi Website you can find the full detail of the steps to follow for [installing operating system images using windows](https://www.raspberrypi.org/documentation/installation/installing-images/windows.md). Simplified though, you need to do the following:

- Download an image to your PC; I got the [Raspbian image from the Raspberry Pi website](https://www.raspberrypi.org/downloads/)
- Insert the SD card in to your reader
- Run [Win32DiskImager](http://sourceforge.net/projects/win32diskimager/) as Administrator
- Select the Raspbian image that you downloaded, and the drive letter of the SD card you inserted (be careful - you're going to irreversibly overwrite which ever drive you select!)
- Click 'Write', wait for the disk imager to finish, Exit the application, and Eject the card

###Turn on the Pi, and get connected to it

You'll need to put the SD card that you just wrote in to the Raspberry Pi, and then turn it on.


- Updating
- DHCP
- WIFI
- Connecting from a Windows PC