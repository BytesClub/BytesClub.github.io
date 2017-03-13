---
layout: page
title: Projects
---


### Battery Manager

A python script to notify when the battery is fully charged.

![scr](https://raw.githubusercontent.com/BytesClub/Battery_Manager/master/branding/screenshot.png)

[Project Link](https://github.com/BytesClub/Battery_Manager)

**How to contribute**: Read [README](https://github.com/BytesClub/Battery_Manager/blob/master/README.md)

**Contributors**

* [Rudra Nil Basu](https://github.com/RudraNilBasu)
* [Amit Tiwary](https://github.com/amitiwary999)

### Simulator

Simulate Standard algorithms

![scr](https://raw.githubusercontent.com/BytesClub/Simulator/master/branding/screen.gif)

[Project Link](https://github.com/BytesClub/Simulator)

**How to contribute**: Read [README](https://github.com/BytesClub/Simulator/blob/master/README.md)

**Contributors**

* [Rudra Nil Basu](https://github.com/RudraNilBasu)


{% for projecs in site.project %}
	<p>Hello!</p>
	{% if projects.title != null %}
		{% if projects.layout == "projects" %}
			<p>Hello!</p>
			<a href="#">{{ projects.title }}</a>
		{% endif %}
	{% endif %}
{% endfor %}
