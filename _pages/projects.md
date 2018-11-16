---
layout: talk
title: "Projects"
permalink: /projects/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

Some of my projects are listed here. The first three projects have reports in their Github Links. For more information, click on them. 

{% for post in site.projects %}
  {% include archive-project.html %}
{% endfor %}
