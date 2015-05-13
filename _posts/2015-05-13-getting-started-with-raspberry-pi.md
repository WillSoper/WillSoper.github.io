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

You *might* need the following, it depends how adventurous you're feeling (it would probably be easier /with/ these):

- HDMI cable (and a monitor or TV to plug it in to)
- USB keyboard and mouse

I've also used the following software, because I'm on Windows:

- [Raspbian image] (https://www.raspberrypi.org/downloads/) 
- [Win32DiskImager](http://sourceforge.net/projects/win32diskimager/)
- [PuTTY] (http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html)

I explain what each software tool is as it is used in the guide.

##What to do:

###Download and install Raspbian on to the MicroSD card

You can find up to date instructions for installing an operating system on the [Raspberry Pi website](https://www.raspberrypi.org/). 

The simplest option is to use NOOBS (there's a great guide with multiple options for getting [NOOBS directly on the Raspberry Pi website](https://www.raspberrypi.org/help/noobs-setup/)); it gives you multiple operating systems, and it's really simple to configure on your computer.

I'm not using NOOBS however, I'm installing Raspbian directly, because I don't need any of the alternative Operating Systems that NOOBS offers, and I'd like to save the space that it takes up.

I'm using Windows to prepare my SD card, and on the Raspberry Pi Website you can find the full detail of the steps to follow for [installing operating system images using windows](https://www.raspberrypi.org/documentation/installation/installing-images/windows.md). Simplified though, you need to do the following:

- Download an image to your PC; I got the [Raspbian image from the Raspberry Pi website](https://www.raspberrypi.org/downloads/)
- Insert an SD card in to your reader
- Run [Win32DiskImager](http://sourceforge.net/projects/win32diskimager/) as Administrator
- Select the Raspbian image that you downloaded, and the drive letter of the SD card you inserted (be careful - you're going to irreversibly overwrite which ever drive you select!)
- Click 'Write', wait for the disk imager to finish, Exit the application, and Eject the card

###Turn on the Pi, assign it an IP address, and get connected to it

You'll need to put the SD card that you just wrote in to the Raspberry Pi, and then turn it on. Now, you need to get connected to it! 

If you're following along and doing this 'headless' (that is, without having plugged in a keyboard and mouse), then the next puzzle that you need to solve is how to find the IP address of the Raspberry Pi. At this stage, you'll need to be plugged in using a Wired network connection, as we've not yet configured a Wireless adapter. 

There are lots of ways to find the IP address of your Pi, but I prefer to do this only once, and then never think about it again. The exact steps will vary by router, but I prefer to set up a static IP address using my router's DHCP feature; this means I can tie one IP address to one piece of hardware forever, and never think about configuring an IP address again.

- Log in to your network router
- Find the 'DHCP' feature (you're looking for currently assigned IP addresses)
- Look for entry that has been assigned to your Raspberry Pi automatically (it will have a hostname of 'raspberrypi' by default), and then copy the MAC address
- Add a new static IP reservation (on my router this is called 'Address Reservation'). You'll need to enter the MAC address that you copied earlier, and then set an IP address that you'd like this device to use permanently.
- You may need to reboot your router, and will definitely need to reboot your Raspberry Pi before the static IP address allocation takes effect.

Once you've assigned a static IP address, you'll always know what your Raspberry Pi IP address is!

Next up, *connecting to your Pi*.

I'm on Windows, and it doesn't have an SSH client installed by default. My preference is to use tools that don't require much installation or configuration, and so I use the standalone executable version of [PuTTY] (http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html). 

Once you've opened PuTTY - enter the IP address that you assigned to your Pi earlier, and leave Port as 22, and hit open. Provided you have the right IP address, and your Pi is responsive, you should see a 'login as:' prompt.

The default username is 'pi' and the default password is 'raspberry' - the very next step that we need to take is to change that!

###Change default credentials, edit hostname, update

Once you're connected to the Pi, things get a lot easier. The first command you should execute is:

> sudo raspi-config

Here you'll see a simple user interface that allows you to perform some of the most common configuration tasks on your Pi. Select option 2, and change your password. 

You might also want to change the hostname of the Pi - this is it's name on your local network, and also the name that the Pi uses to identify itself when you log on to it using SSH; if you want to change the hostname, it's under (8) Advanced Options and then (A2) Hostname.

Once you've done all that, the next step is to update all of your packages and the Raspbian distribution itself. To do that, execute the following commands:

> sudo apt-get update && sudo apt-get dist-upgrade

This is actually two commands combined, (update and dist-upgrade), if you're interested, you can read more about them by executing `man apt-get`.


still to come
- WIFI
