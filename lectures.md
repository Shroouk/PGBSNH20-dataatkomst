---
layout: page
title: Schema
permalink: /lectures/
---

# Lektioner

<!-- <ul id="archive">
{% for week in site.data.schedule.weeks %}
      <b>Vecka</b>: {{week.week}}<br/>
      
      
<li class="archiveposturl">
        <span class="postlower">{{ activity.start-full | date: "%F"}} - {{day.weekday}}</span><br>
        <span><a href="{{ activity.slug | prepend: site.baseurl }}">{{ activity.title }}</a></span><br>
        {% if activity.discussion %}(<i class="fa fa-comments" aria-hidden="true"></i> <a href="{{activity.discussion}}">{{activity.title}}</a>)<br>{% endif %}
<span class = "postlower">
{{ activity.description }}</span>
      </li>
      {% endif %}
      {% endfor %}
            {% endif %}
      {% endfor %}
      
{% endfor %}
</ul> -->





 <div class="row ">
  {% for week in site.data.schedule.weeks %}                         
<div class="col-lg-4">
<div class="card lectures-card">
      <div class="card-header text-center">
      <h4>Vecka: {{week.week}}</h4>
      </div>
       
      

      <div class="card-body">
        {% for day in week.days %}
        {% if day.activities %}
      <div class="row mt-3">
        
      <h6 class="card-subtitle mb-2 text-muted postlower ml-3">{{ activity.start-full | date: "%F"}} - {{day.weekday}}</h6>
            <ul class="list-group lectures-list lec-first">
                     
{% for activity in day.activities %}
{% if activity.activity == "lecture" %}
            <li class="list-group-item"><i class="bi bi-chevron-double-right lec-icon"></i> <a href="{{ activity.slug | prepend: site.baseurl }}">{{ activity.title }}</a>
            {% if activity.discussion %}(<i class="fa fa-comments" aria-hidden="true"></i> <a href="{{activity.discussion}}">{{activity.title}}</a>)<br>{% endif %}
                  <p class="description"> {{ activity.description }}</p>
                  </li>
                  {% endif %}
                  {% endfor %}
            </ul>

            
     

      </div>
      {% endif %}
            {% endfor %}
      </div>
      
     
           
       
</div>

      
</div>
{% endfor %}
</div>

