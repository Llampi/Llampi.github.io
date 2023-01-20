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
    <button onclick="checked('tag1')"> <input type="checkbox" id="tag1" disabled="disabled" checked=checked>Tag 1</button>
    <button onclick="checked('tag2')"> <input type="checkbox" id="tag2" disabled="disabled" checked=checked>Tag 2</button>
    <button onclick="checked('tag3')"> <input type="checkbox" id="tag3" disabled="disabled" checked=checked>Tag 3</button>
    <button onclick="checked('tag4')"> <input type="checkbox" id="tag4" disabled="disabled" checked=checked>Tag 4</button>
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


<script> 
  
  function checked(tag){
         
          let chec = document.getElementById(tag);
          
  
          if (chec.checked == false){
              chec.checked = true; 
              toggle(tag,'block');
              
          }
          else if (chec.checked == true) {
              chec.checked = false;
              toggle(tag,'none');
              
          }
  }
  
  function toggle(className, displayState){
          
          var elements = document.getElementsByClassName(className);
          for (var i = 0; i < elements.length; i++){
               elements[i].style.display = displayState;
          }
  }
            
</script>
