---
layout: archive
title: "Team"
permalink: /team/
author_profile: true
---

{% for member in site.team %}
  <div class="team-member">
    <h3>{{ member.name }}</h3>
    <p>{{ member.role }}</p>
    <a href="{{ member.url }}">Read more</a>
  </div>
{% endfor %}
