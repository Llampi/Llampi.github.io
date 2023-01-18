---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}
<div> Working Paper </div>
{% for post in site.research reversed %}
  {% if post.working == 1 %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
 
 
 <div> Not Working Paper </div>
{% for post in site.research reversed %}
  {% if post.working == 1 %}
  {% else %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
