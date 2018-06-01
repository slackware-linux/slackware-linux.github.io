---
layout: default
title: The Slackware Linux Project
---

{% for post in site.posts %}
  <div class="d-block p-2 bg-dark text-white">
    <a href="{{ post.url }}">{{ post.title }}</a>
  </div>
  <div><p><small>{{ post.day }}</small></p>
    {{ post.excerpt | remove: '<p>' | remove: '</p>' }}
    </div>
<br style="clear:both">
{% endfor %}
