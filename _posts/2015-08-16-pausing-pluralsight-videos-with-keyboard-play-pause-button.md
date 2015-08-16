---
layout: post
title: Pausing pluralsight videos with keyboard play/pause button
published: true
---

I've got a [pluralsight](www.pluralsight.com) subscription, which is great for learning new technologies.

Quite often I code along to the tutorials, as typing the code out myself seems to help me understand how it all hangs together, and I feel more able to amend the code afterward to really cement the learning.

Frequently, I like to pause the tutorial (or even rewind it), either to allow me to catch up or to allow me to play around with the code that I've just written.

Whilst [Pluralsight's HTML5 player does have Keyboard Shortcuts](http://support.pluralsight.com/forums/136402-feature-requests/suggestions/2478678-keyboard-shortcuts-for-video-player), I find it quite frustrating to either alt+tab across from Visual Studio and back, or to use the mouse to go and pause the video. I wanted a way to just hit the 'Play/Pause' media key on my keyboard and have it automatically pause the tutorial without losing my current place.

I've written a short AutoHotKey script to do this (if you've never used AutoHotKey, go have a [read about it on wikipedia](https://en.wikipedia.org/wiki/AutoHotkey) or [give it a try](http://www.autohotkey.com/)). I thought I'd share this script, so you don't have to write it yourself!

The script does two things:

 1. Pressing the Play/Pause media key on the keyboard will play or pause any Pluralsight Player window that's currently open, and will then return the window focus immediately to the current window
 2. Pressing Ctrl+Play/Pause will rewind the tutorial by 8 seconds, and then return the focus to the current window

Here's the script:

{% highlight js %}
Media_Play_Pause::
WinGet, winid ,, A
IfWinNotExist, Pluralsight Player
{
	return
}
WinActivate
ControlSend,ahk_parent,{space}
WinActivate ahk_id %winid%
return


^Media_Play_Pause::
WinGet, winid ,, A
IfWinNotExist, Pluralsight Player
{
	return
}
WinActivate
ControlSend,ahk_parent,b
WinActivate ahk_id %winid%
return
{% endhighlight %}

Enjoy!