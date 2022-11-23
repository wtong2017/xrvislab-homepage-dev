---
layout: page
title: "Home"
class: home
---

<picture>
  <source srcset='/images/welcome_0.jpg' type='image/png' />
  <img
    src='/images/welcome_0.jpg'
    alt='HKUST XRVislab'>
</picture>

<!-- <div class="columns" markdown="1"> -->

## Introduction

<div class="intro" markdown="1">

Extended reaily (XR), including augmented reality (AR) and virtual reality (VR), are the next mainstream computing platforms. Although they have become increasingly accessible in recent years, they have not been widely adopted in daily use. The XR team of HKUST VisLab is devoted to bringing XR into real life and enriching everyone’s XR experience. Our research mission is to design and develop effective XR techniques and user-friendly applications to improve productivity and creativity.

We use human-centered design and data-driven methods to innovate XR technology. We have been developing XR applications to facilitate big data analysis for decision making, resulting in novel visualization techniques, interactions, and authoring tools. Our research has contributed to solving various critical real-world challenges, including social media marketing, urban planning, and education. We are cooperating with local communities as living labs to enrich their living experience using XR. Specifically, we are building the HKUST campuses into XR-enhanced campuses to showcase how people in the future can use XR to break the constraints of time and space to live, study, and play together.

</div>

<!-- <div class="me" markdown="1">
<picture>
  <source srcset='/images/linping_profile.png' type='image/png' />
  <img
    src='/images/linping_profile.png'
    alt='Linping YUAN'>
</picture> -->

<!-- {:.no-list} -->
<!-- find icons here: https://www.angularjswiki.com/fontawesome/ -->
<!-- * <i class="fa fa-envelope"></i> <a href="mailto:{{ site.email }}"> {{ site.email }}</a>
* <i class="fab fa-github"></i> <a href="{{site.github_url}}"> GitHub</a>
* <i class="fab fa-google"></i> <a href="{{site.google_scholar_url}}">Google Scholar</a> -->

<!-- </div> -->

<!-- </div> -->

<!-- <div class="columns" markdown="1">
<div class="intro" markdown="1">
Aiming to explore more unknowns and challenge myself, I shifted my interests to XR and have been exploring the intersection of XR, HCI, and visualization since 2020 summer. Currently, I am a core member of [VisLab XR Team](http://vis.cse.ust.hk/groups/xr-vis/). My ongoing research projects aim to build an XR-enhanced campus and enrich HKUST members' living experience with XR techniques and applications.
</div>
</div> -->

## Latest News

<div class="news" markdown="1">
<table>
<tbody>
{% for news in site.data.news limit:10 %}
  {% include news.html travel=news %}
{% endfor %}
</tbody>
</table>
</div>

## Featured Projects

<div class="featured-projects">
  {% assign sorted_projects = site.data.projects | sort: 'highlight' %}
  {% for project in sorted_projects %}
    {% if project.highlight %}
      {% include project.html project=project %}
    {% endif %}
  {% endfor %}
</div>
<a href="{{ "/projects/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show More Projects
</a>

## Featured Publications

<!-- style 1: with border -->
<div class="pubs">
  {% assign sorted_publications = site.publications | sort: 'year' | reverse %}
  {% for pub in sorted_publications %}
    {% if pub.highlight and pub.visible %}
      {% include publication.html pub=pub %}
    {% endif %}
  {% endfor %}
</div>

<!-- style 2: simple; don't delete-->
<!-- <div class="featured-publications">
  {% assign sorted_publications = site.publications | sort: 'year' | reverse %}
  {% for pub in sorted_publications %}
    {% if pub.highlight%}
      <div class="publication pubs">
        {% if pub.doi %}
        <a href="https://doi.org/{{ pub.doi }}" target="_blank"><span class="pub-title">{{ pub.title }}</span>.</a>
        {% elsif pub.pdf %}
        <a href="{{ pub.pdf }}" target="_blank"><span class="pub-title">{{ pub.title }}</span>.</a>
        {% endif %}
        <div class="authors">
          {% for author in pub.authors %}
            {% include person.html person=author %}
            {% unless forloop.last %}, {% endunless %}
          {% endfor %}.
          <br/><i>{{ pub.venue }}</i>, {{ pub.year }}.
          {% if pub.type[0]=="Poster" %} (Poster)
          {% elsif pub.type[0] == "Notes" %} (Notes)
          {% elsif pub.note %} ({{ pub.note }})
          {% endif %}
          {% for award in pub.awards %}
            <br/><span class="award"><i class="fas fa-{% if award == "Best Paper Award" %}trophy{% else %}award{% endif %}" aria-hidden="true"></i> {{ award }}</span>
          {% endfor %}
        </div>
      </div>
    {% endif %}
  {% endfor %}
</div> -->

<a href="{{ "/publications/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show All Publications
</a>
