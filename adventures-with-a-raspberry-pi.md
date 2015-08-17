---
layout: page
title: Adventures with a Raspberry Pi
---

<p class="message">
	I've had a lot of fun with my Raspberry Pi, and so I've written up some of my projects so you can join in!
	<br /><br />
	This is a list of the projects that I've completed so far.
</p>

{% for post in site.tags.raspberrypi limit: 20 %}
  * {{ post.date | date_to_string }} &raquo; [ {{ post.title }} ]({{ post.url }})
{% endfor %}
