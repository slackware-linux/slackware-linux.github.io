---
title: The Slackware Linux Project
layout: default
---

{% for post in site.posts %}
<div class="row">
  <div class="d-block p-2 bg-dark text-white">
    <a href="{{ post.url }}">{{ post.title }}</a>
  </div>
  <div><p><small>{{ post.day }}</small></p>
    {{ post.excerpt | remove: '<p>' | remove: '</p>' }}
    </div>
</div>
<br style="clear:both">
{% endfor %}
