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

### Current Members
<div class="grid">
  {% for person in site.data.people %}
    {% if person[1].role == "member" %}
      {% include person.html person=person %}
    {% endif %}
  {% endfor %}
</div>

### Alumni
<div class="grid">
  {% for person in site.data.people %}
    {% if person[1].role == "alumni" %}
      {% include person.html person=person %}
    {% endif %}
  {% endfor %}
</div>
