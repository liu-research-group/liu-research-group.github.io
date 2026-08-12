---
title: "Liu Research Group - Team"
layout: gridlay
excerpt: "Team members"
sitemap: false
permalink: /team/
---

<style>

.button {
    clear: left;
    background-color: #4CAF50; /* Green */
    border: none;
    color: white;
    padding: 4px 20px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 12px;
    margin: 4px 2px;
    -webkit-transition-duration: 0.4s; /* Safari */
    transition-duration: 0.4s;
    cursor: pointer;
}

.black {
    background-color: white;
    color: black;
    border: 2px solid #555555;
}

</style>

# Group Members

## Staff
{% for member in site.data.team_members %}

<div class="row">

<div class="col-sm-3 col-xs-6">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" style="width:100%; max-width:200px;" alt="Portrait of {{ member.name }}" />
</div>

<div class="col-sm-9">
  <div>
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}</i>
  <br><a href="mailto:{{ member.email }}">{{ member.email }}</a>
  {% if member.education1 %}<br><small>{{ member.education1 }}</small>{% endif %}
  {% if member.education2 %}<br><small>{{ member.education2 }}</small>{% endif %}
  {% if member.education3 %}<br><small>{{ member.education3 }}</small>{% endif %}
  
  <p style="font-size:.8em">{{ member.short_bio }}</p>
  </div>

  <p style="clear:both;"></p>
  <button class="button black" onclick="window.location.href='{{ member.website }}'" type="button">
  {{ member.name }} on Google Scholar</button>
  {% if member.linkedin %}<button class="button black" onclick="window.location.href='{{ member.linkedin }}'" type="button">LinkedIn</button>{% endif %}
  {% if member.github %}<button class="button black" onclick="window.location.href='{{ member.github }}'" type="button">GitHub</button>{% endif %}

</div>

</div>


{% endfor %}




<p>&nbsp;</p>

## Our team is forming

The Liu Research Group is brand new and actively recruiting its founding members. We have multiple fully funded PhD positions open, starting Spring 2027 or later, and we welcome motivated MS and undergraduate researchers.

If you are a prospective PhD, MS or undergraduate researcher, we would love to hear from you &mdash; see [Openings](/openings) for what we look for and how to apply.
