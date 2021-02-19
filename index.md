---
layout: default
title: About
permalink: /index.html
---
<div>
    {% for post in site.posts limit:1 %}
    <div class="comic-panel center">
        <img src="{{ site.url }}{{ post.comic }}" alt="{{post.comicalt}}"/>
        <ul class="pager">
            <li><a class="btn btn-outline-secondary" href="{{ site.url }}{{ post.previous.url }}">PREVIOUS</a></li>
        </ul>
    </div><!--comic div-->
    <div class="comic-blog center">
        {{post.content}}
    </div>
    {% endfor %}
</div>
