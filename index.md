---
layout: default
title: About
permalink: /index.html
---
<div>
    {% for post in site.posts limit:1 %}
    <div class="comic-panel center">
        <img src="{{ site.url }}{{ post.comic }}" alt="{{post.comicalt}}"/>
        <ul class="comic-nav">
            {% assign comicPosts = site.posts | reverse %}
            {% assign lastComicPost = comicPosts | last %}
            <li><a class="grad-button" href="{{ site.url }}{{ comicPosts[0].url }}" >First</a></li>
            {% if post.previous.url %}
            <li><a class="grad-button" href="{{ site.url }}{{ post.previous.url }}" >Previous</a></li>
            {% endif %}
            <li><a class="grad-button" href="{{ site.url }}{{ lastComicPost.url }}">Last</a></li>
        </ul>
    </div><!--comic div-->
    <div class="comic-blog center">
        {{post.content}}
    </div>
    {% endfor %}
</div>
