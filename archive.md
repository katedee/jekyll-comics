---
layout: default
title: About
permalink: /archive
---
# Archive

<ul class="post-list archive-ul">
  {% for post in site.categories.page %}
    <li class="archive-li">
      <a class="post-link" href="{{ post.url | prepend: site.baseurl }}"><img src="{{ post.comic | prepend: site.baseurl }}"/></a>
    </li>
  {% endfor %}
</ul>
