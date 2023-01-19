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
<div>
    <button class="boton_alert"> <input type="checkbox" id="tag1" disabled="disabled" checked=checked>Tag 1</button>
    <button onclick="checked('tag2')"> <input type="checkbox" id="tag2" disabled="disabled" checked=checked>Tag 2</button>
    <button onclick="checked('tag3')"> <input type="checkbox" id="tag3" disabled="disabled" checked=checked>Tag 3</button>
</div>
  <div><h2> Publications </h2></div>
{% for post in site.research reversed %}
  {% if post.working == 0 %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}


<div><h2> Working Papers </h2> </div>
{% for post in site.research reversed %}
  {% if post.working == 1 %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
 
 
 <div><h2> Work in Progress </h2></div>
{% for post in site.research reversed %}
  {% if post.working == 2 %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}


{% include tags-script.html %}


<script src="{{ site.baseurl }}{% link assets/js/tags-script %}" </script>
