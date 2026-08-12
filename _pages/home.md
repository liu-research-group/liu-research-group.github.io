---
title: "Liu Research Group"
layout: homelay
excerpt: "Liu Research Group at the University of Alabama."
sitemap: false
permalink: /
---

# Intelligent building energy systems

We design intelligent, low-carbon building energy systems &mdash; uniting physics-based modeling, machine learning, and predictive control to make buildings efficient, flexible, and grid-interactive.

## Research

Our work spans four connected thrusts.

<div class="row">
{% assign n = 0 %}
{% for theme in site.data.research_themes %}
{% if theme.highlight == 1 %}
{% assign even_odd = n | modulo: 2 %}
{% if even_odd == 0 %}<div class="clearfix visible-sm-block visible-md-block visible-lg-block"></div>{% endif %}
<div class="col-sm-6 clearfix">
<div class="well" style="min-height: 215px;">
<h3 style="margin-top:0; font-size:18px;"><a href="{{ site.url }}{{ site.baseurl }}/research#{{ theme.key }}">{{ theme.title }}</a></h3>
<p>{{ theme.description }}</p>
</div>
</div>
{% assign n = n | plus: 1 %}
{% endif %}
{% endfor %}
</div>

More detail, with representative papers for each thrust, is on the [Research page]({{ site.url }}{{ site.baseurl }}/research).

## Where we sit

We are a new group in the [Department of Civil, Construction and Environmental Engineering](https://cce.eng.ua.edu/) at the [University of Alabama](https://www.ua.edu/), in Tuscaloosa, Alabama. Our work sits at the intersection of thermal systems, machine learning, and control, and we collaborate across building science, energy systems, and computing.

**We are actively recruiting our founding members &mdash; fully funded PhD students starting Spring 2027 or later, plus motivated MS and undergraduate students** [(more info)]({{ site.url }}{{ site.baseurl }}/openings)**!**
