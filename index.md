---
title: The Slackware Linux Project
subtitle: Slackware 14.2 is released!
layout: default
---

{% for post in site.posts %}
<div class="row">
<div class="d-block p-2 bg-dark text-white"><a href="{{ post.url }}">{{ post.title }}</a></div>
<div>{{ post.excerpt | remove: '<p>' | remove: '</p>' }}</div>
</div>
<br style="clear:both">
{% endfor %}
