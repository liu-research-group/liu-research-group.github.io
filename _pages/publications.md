---
title: "Liu Research Group - Publications"
layout: gridlay
excerpt: "Liu Research Group -- Publications."
sitemap: false
years: [2026, 2025, 2024, 2020, 2019]
permalink: /publications/
---
<!-- _pages/publications.md -->

# Publications

Peer-reviewed journal articles, newest first. Conference papers, ASHRAE and Modelica proceedings and presentations are on [Google Scholar](https://scholar.google.com/citations?user=FRH4bwcAAAAJ&hl=en).

## Group Highlights

A few papers that best represent what the group works on. The complete list follows [below](#list-of-publications).


{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

{% if publi.long == 1 %}
<div class="col-md-6 clearfix">
 <div class="well">
  <h3 class="pubtit">{{ publi.title }}</h3>
  {% if publi.image %}<img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="20%" style="float: left" alt="Illustration for {{ publi.title | escape }}" />{% endif %}
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  {% if publi.link.url %}<p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>{% endif %}
  {% if publi.news1 %}<p class="text-danger"><strong>{{ publi.news1 }}</strong></p>{% endif %}
  {% if publi.news2 %}<p>{{ publi.news2 }}</p>{% endif %}
 </div>
</div>
{% else %}
<div class="col-md-6 clearfix">
 <div class="well">
  <h3 class="pubtit">{{ publi.title }}</h3>
  {% if publi.image %}<img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="40%" style="float: left" alt="Illustration for {{ publi.title | escape }}" />{% endif %}
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  {% if publi.link.url %}<p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>{% endif %}
  {% if publi.news1 %}<p class="text-danger"><strong>{{ publi.news1 }}</strong></p>{% endif %}
  {% if publi.news2 %}<p>{{ publi.news2 }}</p>{% endif %}
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## List of Publications

<div class="publications">

{%- for y in page.years %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
