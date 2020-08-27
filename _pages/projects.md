---
layout: page
title: projects
permalink: /Projects/
description: A collection of projects.
---

{% for project in site.projects %}

{% if project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="_blank">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

<div class="card mb-3">
  <div class="row no-gutters">
    
        <div class="col-md-4">
        {% if project.img %}
        <img src="{{ project.img | prepend: site.baseurl | prepend: site.url }}" class="card-img" alt="{{ project.title }}">
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}  
        
        </div>
        <div class="col-md-8">
        <div class="card-body">
            <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}"><h3 class="card-title">{{ project.title }}</h3></a>
            <p class="card-text">{{ project.description }}</p>
            <!-- <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p> -->
        </div>
        </div>
    
  </div>
</div>

{% endif %}

{% endfor %}
