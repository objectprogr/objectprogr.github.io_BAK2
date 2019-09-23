---
layout: archive
permalink: /archive
title: "Archive"
author_profile: false
toc: true
toc_label: "Table of content"
toc_icon: "file-text"
---
## Chronological

<section class="archive-post-list">
   {% for post in site.posts %}
       {% assign currentDate = post.date | date: "%Y" %}
       {% if currentDate != myDate %}
           {% unless forloop.first %}</ul>{% endunless %}
            <h3> {{ currentDate }} </h3>
           <ul>
           {% assign myDate = currentDate %}
       {% endif %}
       <li><a href="{{ post.url }}">{{ post.title }}<span style="color:blue;font-size:10px"> {{ post.date | date: "%B %-d" }}</span></a></li>
       {% if forloop.last %}</ul>{% endif %}
   {% endfor %}
</section>
