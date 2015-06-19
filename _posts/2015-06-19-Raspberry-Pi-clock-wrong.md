---
layout: post
title: What to do if your Raspberry Pi has the wrong time
published: true
---

Theoretically, your Raspberry Pi should set itself to the right time automatically using NTP (Network Time Protocol); however for me that hasn't worked on a number of occasions. I think it fails to sync correctly when the internal clock is too far adrift from the time reported by the NTP server, but anyway, this is how to fix it.

Find the right NTP pool servers for your location on the [NTP Pool Project](http://www.pool.ntp.org/), I use the [UK NTP Pool](http://www.pool.ntp.org/)

Edit your `/etc/ntp.conf` file, and replace the list of servers there with the ones that you found on the NTP Pool Project:

> server 0.uk.pool.ntp.org iburst
server 1.uk.pool.ntp.org iburst
server 2.uk.pool.ntp.org iburst
server 3.uk.pool.ntp.org iburst

Restart the NTP daemon with `sudo /etc/init.d/ntp restart`, and then check the time is correct with the `date` command - it might take a few minutes to straighten itself out.