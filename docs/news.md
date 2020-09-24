---
title: In the news
layout: doc
permalink: /news/
---

FAIR-biomed was featured in the news!

<div class="news-comment"><i>Note:</i> Items marked <i class="fas fa-user-edit pad-md"></i> were authored or co-authored by a FAIR-biomed contributor.</div>

<div class="news-comment"><i>Note:</i> These lists may be incomplete. Please update them via the github repository.</div>


## Blogs, videos

<table id="news-blog" class="news-table">
{% for item in site.data.news.presentations %}
    <tr>
        <td>
            {% if item.link contains "twitter.com" %}
                <i class="fab fa-twitter"></i>
            {% endif %}
            {% if item.link contains "youtube.com" %}
                <i class="fab fa-youtube"></i>
            {% endif %}
            {% if item.tags contains "blog" %}
                <i class="fas fa-blog"></i>
            {% endif %}
            {% if item.tags contains "contributor" %}
                <i class="fas fa-user-edit"></i>
            {% endif %}
         </td>
        <td>{{item.date}}</td>
        <td><a href="{{item.link}}">{{item.title}}</a><br/>{{item.medium}}</td>
    </tr>
{% endfor %}
</table>


## Social media 

<table id="news-social" class="news-table">
{% for item in site.data.news.social %}
    <tr>
        <td>
            {% if item.link contains "twitter.com" %}
                <i class="fab fa-twitter"></i>
            {% endif %}
            {% if item.link contains "youtube.com" %}
                <i class="fab fa-youtube"></i>
            {% endif %}
            {% if item.tags contains "contributor" %}
                <i class="fas fa-user-edit"></i>
            {% endif %}
         </td>
        <td>{{item.date}}</td>
        <td><a href="{{item.link}}">{{item.title}}</a></td>
    </tr>
{% endfor %}
</table>

