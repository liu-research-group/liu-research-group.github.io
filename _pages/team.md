---
title: "Liu Research Group - Team"
layout: gridlay
excerpt: "Team members"
sitemap: false
permalink: /team/
---

# Group Members

## Principal Investigator
{% for member in site.data.team_members %}

<div class="row">

<div class="col-xs-12 col-sm-3">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" style="width:100%; max-width:200px;" alt="Portrait of {{ member.name }}" />
</div>

<div class="col-xs-12 col-sm-9">
  <div>
  <h3>{{ member.name }}</h3>
  <i>{{ member.info }}</i>
  <br><a href="mailto:{{ member.email }}">{{ member.email }}</a>
  {% if member.education1 %}<br><small>{{ member.education1 }}</small>{% endif %}
  {% if member.education2 %}<br><small>{{ member.education2 }}</small>{% endif %}
  {% if member.education3 %}<br><small>{{ member.education3 }}</small>{% endif %}
  
  <p>{{ member.short_bio }}</p>
  </div>

  <a class="profile-link" href="{{ member.website }}" target="_blank" rel="noopener">Google Scholar</a>
  {% if member.linkedin %}<a class="profile-link" href="{{ member.linkedin }}" target="_blank" rel="noopener">LinkedIn</a>{% endif %}

</div>

</div>


{% endfor %}




## Our team is forming

The Liu Research Group is brand new and actively recruiting. We are looking for fully funded PhD students starting Spring 2027 or later, and we welcome motivated MS and undergraduate students.

If you are a prospective PhD, MS or undergraduate student, we would love to hear from you &mdash; see [Openings](/openings) for what we look for and how to apply.
