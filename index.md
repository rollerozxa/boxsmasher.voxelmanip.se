---
no_title: true
---

# Box Smasher
Box Smasher is a physics-based puzzle game where you shoot balls to smash structures of boxes off the screen and into the void. The objective is to clear each level of all boxes in a limited amount of balls.

Currently the game has 12 levels (as of v1.0.1), with more coming soon. Do you have what it takes to complete them all?

<p style="text-align:center"><a class="dl-button" href="/download/">Download</a></p>

## Latest news

<ul class="latest-news">
{% for post in site.posts %}
	<li>
		<time>{{ post.date | date:"%d %b %Y" }}</time>
		<a href="{{ post.url }}">{{ post.title }}</a>
	</li>
{% endfor %}
</ul>

## Screenshots

<div class="image-gallery">
	<a href="/media/screenshots/1.webp" target="_blank"><img src="/media/screenshots/1.webp" alt="Screenshot of the main menu of Box Smasher, with a title screen, play button and boxes falling down in the backgrounds."></a>
	<a href="/media/screenshots/2.webp" target="_blank"><img src="/media/screenshots/2.webp" alt="(alt text pending)"></a>
	<a href="/media/screenshots/3.webp" target="_blank"><img src="/media/screenshots/3.webp" alt="(alt text pending)"></a>
	<a href="/media/screenshots/4.webp" target="_blank"><img src="/media/screenshots/4.webp" alt="(alt text pending)"></a>
</div>

## More information
Box Smasher was originally developed by ROllerozxa as the final assignment for his programming course in upper secondary school during Spring of 2023. After version v1.0.0 was finished for the assignment, ROllerozxa has since continued working on the game throughout the years and is hoping to release new updates in the future.

Box Smasher is written in Lua using the [LÖVE](https://love2d.org/) game framework and runs on anywhere LÖVE exists, including Windows, macOS, Linux and Android. However it was originally intended as a mobile game, and is best played on a touchscreen device or even with a drawing tablet!

The game is Free software and licensed under the GPLv3 license, the game's development can be followed in the [Box Smasher repository on GitHub](https://github.com/rollerozxa/boxsmasher).
