---
layout: archive
title: "Team"
permalink: /team/
author_profile: true
---

{% for member in site.team %}
  <div class="team-member">
    <h2>{{ member.name }}</h3>
    <h3>{{ member.role }}</h3>
    <div>
      {{ member.content | markdownify }}
    </div>
  </div>
{% endfor %}
