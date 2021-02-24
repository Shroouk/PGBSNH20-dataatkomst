---
layout: page
title: Schema
permalink: /lectures/
---

# Lektioner







 <div class="row">
  {% for week in site.data.schedule.weeks %}                         
<div class="col-lg-4">
<div class="card lectures-card">
      <div class="card-header text-center">
      <h4>Vecka: {{week.week}}</h4>
      </div>
       {% for day in week.days %}
      {% if day.activities %}
      {% for activity in day.activities %}
      {% if activity.activity == "lecture" %}
      <div class="card-body">
     
      <div class="row mt-3">

      <h6 class="card-subtitle mb-2 text-muted postlower ml-3">{{ activity.start-full | date: "%F"}} - {{day.weekday}}</h6>
            <ul class="list-group lectures-list lec-first">
            <li class="list-group-item"><i class="bi bi-chevron-double-right lec-icon"></i> <a href="{{ activity.slug | prepend: site.baseurl }}">{{ activity.title }}</a>
            {% if activity.discussion %}(<i class="fa fa-comments" aria-hidden="true"></i> <a href="{{activity.discussion}}">{{activity.title}}</a>)<br>{% endif %}
                  <p class="description"> {{ activity.description }}</p>
                  </li>
            </ul>

      </div>
     
      


     

      </div>
     
        {% endif %}
      {% endfor %}
           
       
</div>
{% endif %}
      {% endfor %}
</div>
{% endfor %}
</div>

