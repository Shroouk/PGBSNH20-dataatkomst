---
layout: lecture
title: Introduktion till kursen och C# refresh
lectureDate: Måndag den 1:a Mars 2021
permalink: /lectures/introduction
---


Denna lektion är en introduktion till kursen, samt dom första steg med projektet. Fastsällning av grupper.

## Lektionsplan











  <div class="card schedule-card">
          <div class="card-body">
            <div class="row">
                <h5 class="pl-3"><i class="bi bi-calendar-week"></i> Lektion från kl. 8:30 till kl. 16:30 </h5>
            </div>

            
{% for activity in site.data.schedule.weeks[0].days[0].activities %}
            <div class="row">
              <div class="col-sm-1 ">
                <div class="circle"></div>

              
              <div class="col-sm-11 schedule-txt">
               * {{ activity.start-full | date: "%R"}} - {{ activity.end-full | date: "%R"}} : {% if activity.discussion %}<i class="fa fa-comments" aria-hidden="true"></i> [{{activity.title}}]({{activity.discussion}}) (delta aktivt i diskussionen){% else %}{{activity.title}} {% endif %}
{% endfor %}
              </div>
            </div>

{% endfor %}
          </div>
        </div>
