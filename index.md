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
        <ul class="comic-nav">
            {% assign comicPosts = site.posts | reverse %}
            {% assign lastComicPost = comicPosts | last %}
            <li><a class="grad-button" href="{{ site.url }}{{ comicPosts[0].url }}" >First</a></li>
            {% if page.previous.url %}
            <li><a class="grad-button" href="{{ site.url }}{{ page.previous.url }}" >Previous</a></li>
            {% endif %}
            {% if page.next.url %}
            <li><a class="grad-button" href="{{ site.url }}{{ page.next.url }}" >Next</a></li>
            {% endif %}
            <li><a class="grad-button" href="{{ site.url }}{{ lastComicPost.url }}">Last</a></li>
        </ul>
    </div><!--comic div-->
    <div class="comic-blog center">
        {{post.content}}
    </div>
    {% endfor %}
</div>
