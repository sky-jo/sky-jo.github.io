---
layout: archive
title: "Team"
permalink: /team/
author_profile: true
---

{% include base_path %}
{% for post in site.researchers %}
    {% include archive-single.html %}
{% endfor %}
