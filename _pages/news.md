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
        <div class="announcement-content" id="announcement-{{ forloop.index }}">
            {{ announcement.content | markdownify }}
        </div>
        <button onclick="toggleContent('announcement-{{ forloop.index }}')" class="view-more-btn">View More</button>
    </div>
{% endfor %}

<script>
function toggleContent(id) {
    var content = document.getElementById(id);
    var btn = content.nextElementSibling;

    if (content.classList.contains('truncate')) {
        content.classList.remove('truncate');
        btn.textContent = 'View Less';
    } else {
        content.classList.add('truncate');
        btn.textContent = 'View More';
    }
}
</script>

<style>
.announcement-content.truncate {
    max-height: 100px;
    overflow: hidden;
}
.view-more-btn {
    background-color: #007bff;
    color: white;
    padding: 5px 10px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}
.view-more-btn:hover {
    background-color: #0056b3;
}
</style>
