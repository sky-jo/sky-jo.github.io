---
layout: archive
title: "News"
permalink: /news/
author_profile: true
---

{% for announcement in site.news %}
    <div class="news">
        <h1>{{ announcement.title }}</h1>
        <h3>{{ announcement.date }}</h3>
        <div class="announcement-content">
            {% capture content %}{% raw %}{{ announcement.content | markdownify }}{% endraw %}{% endcapture %}
            {% if content | size > 300 %}
                {{ content | truncatewords: 50, '...' }}
                <a href="{{ announcement.url }}" style="background-color: #007bff; color: white; padding: 5px 10px; border: none; border-radius: 5px; text-decoration: none;">View More</a>
            {% else %}
                {{ content }}
            {% endif %}
        </div>
    </div>
{% endfor %}
