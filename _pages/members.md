---
layout: page
permalink: /members/
title: Members
# description: Materials for courses you taught. Replace this text with your description.
nav: true
sortedIndex: 1
display_categories: [work]
---

{% assign groups = site.members | sort: "group_rank" | map: "group" | uniq %}
{% assign num_alumni = 0 %}
{% for group in groups %}
{% assign num = 0 %}

    {% assign members = site.members | sort: "lastname" | where: "group", group %}
    {% for member in members %}
    {% if member.alumni %}
    {% assign num_alumni = num_alumni | plus: 1 %}
    {% else %}
    {% assign num = num | plus: 1 %}
    {% if num == 1 %}
## {{ group }}
    {% endif %}
<p>
    <div class="card hoverable bg-custom-1 d-block">
        <div class="row no-gutters">
            <div class="col-sm-4 col-md-3">
                <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="img-fluid w-100 rounded-circle" alt="{{ member.profile.name }}" />
            </div>
            <div class="col-sm-8 col-md-9">
                <div class="card-body">
                    <a href="{{ member.url | relative_url }}">
                    <h5 class="card-title">{{ member.profile.name }}</h5>
                    {% if member.profile.position %}<h6 class="card-subtitle mb-2 text-muted">{{ member.profile.position }}</h6>{% endif %}
                    <p class="card-text" style="color: var(--global-text-color);opacity:.6">
                        {{ member.teaser }}
                    </p>
                    </a>
                    {% if member.profile.email %}
                        <a href="mailto:{{ member.profile.email }}" class="card-link"><i class="fas fa-envelope"></i></a>
                    {% endif %}
                    {% if member.profile.phone %}
                        <a href="tel:{{ member.profile.phone }}" class="card-link"><i class="fas fa-phone"></i></a>
                    {% endif %}
                    {% if member.profile.orcid %}
                        <a href="https://orcid.org/{{ member.profile.orcid }}" class="card-link" target="_blank"><i class="fab fa-orcid"></i></a>
                    {% endif %}
                    {% if member.profile.twitter %}
                        <a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank"><i class="fab fa-twitter"></i></a>
                    {% endif %}
                    {% if member.profile.facebook %}
                        <a href="https://facebook.com/{{ member.profile.facebook }}" class="card-link" target="_blank"><i class="fab fa-facebook"></i></a>
                    {% endif %}
                    {% if member.profile.linkedin %}
                        <a href="https://linkedin.com/in/{{ member.profile.linkedin }}" class="card-link" target="_blank"><i class="fab fa-linkedin"></i></a>
                    {% endif %}
                    {% if member.profile.github %}
                        <a href="https://github.com/{{ member.profile.github }}" class="card-link" target="_blank"><i class="fab fa-github"></i></a>
                    {% endif %}
                    {% if member.profile.website %}
                        <a href="{{ member.profile.website }}" class="card-link" target="_blank"><i class="fas fa-globe"></i></a>
                    {% endif %}
                    <p class="card-text">
                        <small class="test-muted"><i class="fas fa-thumbtack"></i> {{ member.profile.address | replace: '<br />', ', ' }}</small>
                    </p>
                </div>
            </div>
        </div>
    </div>
</p>
    {% endif %}
    {% endfor %}
<br/>
{% endfor %}


{% if num_alumni > 0 %}
## Alumni
<div class="project">
<div class="grid" >

<div class="container mt-5">
<!-- <div class="row row-cols-5"> -->
{% assign groups = site.members | sort: "group_rank" | map: "group" | uniq %}
{% for group in groups %}
    {% assign members = site.members | sort: "lastname" | where: "group", group %}
    {% for member in members %}
    {% if member.alumni %}

<div class="grid-item">

  <a href="{{ member.url | relative_url }}">

<div class="card hoverable bg-custom-1 d-block w-30 p-3">
    {% if member.profile.image %}
    <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="img-fluid" alt="{{ member.profile.name }}">
    {% endif %}
    <div class="card-body">
    <h5 class="card-title">{{ member.title }}</h5>
    <p class="card-text">{{ member.description }}</p>
    <div class="row mx-auto">
        {% if member.profile.email %}
            <a href="mailto:{{ member.profile.email }}" class="card-link"><i class="fas fa-envelope"></i></a>
        {% endif %}
        {% if member.profile.phone %}
            <a href="tel:{{ member.profile.phone }}" class="card-link"><i class="fas fa-phone"></i></a>
        {% endif %}
        {% if member.profile.orcid %}
            <a href="https://orcid.org/{{ member.profile.orcid }}" class="card-link" target="_blank"><i class="fab fa-orcid"></i></a>
        {% endif %}
        {% if member.profile.twitter %}
            <a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank"><i class="fab fa-twitter"></i></a>
        {% endif %}
        {% if member.profile.facebook %}
            <a href="https://facebook.com/{{ member.profile.facebook }}" class="card-link" target="_blank"><i class="fab fa-facebook"></i></a>
        {% endif %}
        {% if member.profile.linkedin %}
            <a href="https://linkedin.com/in/{{ member.profile.linkedin }}" class="card-link" target="_blank"><i class="fab fa-linkedin"></i></a>
        {% endif %}
        {% if member.profile.github %}
            <a href="https://github.com/{{ member.profile.github }}" class="card-link" target="_blank"><i class="fab fa-github"></i></a>
        {% endif %}
        {% if member.profile.website %}
            <a href="{{ member.profile.website }}" class="card-link" target="_blank"><i class="fas fa-globe"></i></a>
        {% endif %}
    </div>
    </div>
</div>
  </a>
</div>

{% endif %}
{% endfor %}
{% endfor %}
</div>
</div>
</div>
<!-- </div> -->
{% endif %}

