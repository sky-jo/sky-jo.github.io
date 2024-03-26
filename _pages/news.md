---
layout: archive
title: "News"
permalink: /news/
author_profile: true
---

{% for announcement in in site.news %}
    <h1>{% announcement.title %}</h1>
    <h3>{% announcement.data %}</h3>
    <div>
        {{{ announcement.content | markdownify }}}
    </div>

{% endfor %}