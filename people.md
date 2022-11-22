---
layout: page
permalink: /people/
title: People
class: people
---

{:.hidden}
# Projects

{:.lead}
Meet the Team

<div class="grid">
  {% for person in site.data.people %}
    {% if person[1].role == "member" %}
      {% include person.html person=person %}
    {% endif %}
  {% endfor %}
</div>
