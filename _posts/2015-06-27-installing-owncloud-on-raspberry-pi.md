---
layout: post
title: Installing OwnCloud on a Raspberry Pi
published: false
tags:
- raspberrypi
---

I got tired of manually managing my backups on multiple hard disks, and constantly forgetting to put files that I wanted to share on multiple computers in to DropBox. 

I realised that I could get quite a lot of free backup space online using Google Drive or Microsoft OneDrive, but this gave me a couple of other issues:

 - I don't have a fantastic internet connection (not quick enough to upload and download multiple Gigabytes of data before I got bored, at any rate)
 - I don't trust cloud storage services with access to all of my most sensitive data (I scan my bank statements, for example). I could encrypt them, but that's just another step for me to manage.
 
So, I decided to set up an [OwnCloud](https://owncloud.org/) server, using my RaspberryPi. This would mean that I could easily store **all** of the files that I want to be backed up on cloud storage, without worrying about the time it would take to upload or any storage limits.

In the future, I also intend to set my Raspberry Pi up as a VPN server, so that I can remotely access my files when I'm out of the house... but one thing at a time!

This is the guide that I used:
 
http://unixetc.co.uk/2015/02/21/simple-owncloud-installation-on-raspberry-pi-2/


External storage (eg DropBox): https://doc.owncloud.org/server/7.0/admin_manual/configuration/external_storage_configuration_gui.html
