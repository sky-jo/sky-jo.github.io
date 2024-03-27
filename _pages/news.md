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
            {% if announcement.content | size > 300 %}
                {{ announcement.content | markdownify | truncatewords: 50, '...' }}
                <a href="{{ announcement.url }}" class="view-more-btn">View More</a>
            {% else %}
                {{ announcement.content | markdownify }}
            {% endif %}
        </div>
    </div>
{% endfor %}

<style>
.view-more-btn {
    background-color: #007bff;
    color: white;
    padding: 5px 10px;
    border: none;
    border-radius: 5px;
    text-decoration: none;
}
.view-more-btn:hover {
    background-color: #0056b3;
}
</style>
