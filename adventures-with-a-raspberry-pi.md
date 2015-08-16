---
layout: page
title: Adventures with a Raspberry Pi
---

<p class="message">
	I’ve had a lot of fun with my raspberry pi, and I decided that it would be helpful to write up how I completed each of my projects.

	This is a list of all the projects that I’ve done so far, and I’ll add to them as and when I complete more!
</p>

{% for post in site.tags.raspberrypi limit: 20 %}
  * {{ post.date | date_to_string }} &raquo; [ {{ post.title }} ]({{ post.url }})
{% endfor %}