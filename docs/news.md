---
title: News
layout: doc
permalink: /news/
---

FAIR-biomed was featured in the news!


## Blog posts

<table id="news-blog" class="news-table">
{% for item in site.data.news.blog %}
    <tr>
        <td><i class="fas fa-blog"></i>
            {% if item.tags contains "contributor" %}
                <i class="fas fa-user-edit"></i>
            {% endif %}
         </td>
        <td>{{item.date}}</td>
        <td><a href="{{item.link}}">{{item.title}}</a></td>
    </tr>
{% endfor %}
</table>

<div class="news-comment"><i>Note:</i> Items marked <i class="fas fa-user-edit pad-md"></i> were authored or co-authored by a FAIR-biomed contributor.</div>


## Social media 


<table id="news-social" class="news-table">
{% for item in site.data.news.social %}
    <tr>
        <td>
            {% if item.link contains "twitter.com" %}
                <i class="fab fa-twitter"></i>
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

<div class="news-comment"><i>Note:</i> Items marked <i class="fas fa-user-edit pad-md"></i> were authored or co-authored by a FAIR-biomed contributor.</div>

<div class="news-comment"><i>Note:</i> This list may be incomplete. Please update it via the github repository.</div>
