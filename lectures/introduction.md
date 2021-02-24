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

              </div>
              <div class="col-sm-2 p-0 schedule-txt">
             {{ activity.start-full | date: "%R"}} - {{ activity.end-full | date: "%R"}} 
              </div>
              <div class="col-sm-9 schedule-txt">
              {% if activity.discussion %}<i class="fa fa-comments" aria-hidden="true"></i> 
              * [{{activity.title}}]({{activity.discussion}}) (delta aktivt i diskussionen){% else %}{{activity.title}} {% endif %}
              </div>
            </div>

{% endfor %}
          </div>
        </div>




## Lektionsteori
*Detta är material (artiklar, videoer, blogs, podcasts etc) som är den teoretiska bas för denna lektion, det antas att du har läst/set/lystnad detta innan lektionen starter.*





 
{% for topic in site.data.lecture_csharp_refresh.topics %}
  <div class="accordion" id="accordionExample">

  <div class="card">
                <div class="card-header" id="headingOne">
                  <h2 class="mb-0 w-100">
                    <button class="btn btn-link btn-block text-left" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="false" aria-controls="collapseOne">
                      <h3 id="object-oriented-programming-and-c"><i class="bi bi-caret-right-fill"></i> 
                      ### {{topic.topic}}
                      </h3>
                    </button>
                  </h2>
                </div>

                <div id="collapseOne" class="collapse show" aria-labelledby="headingOne" data-parent="#accordionExample">
                  <div class="card-body">
                    <ul>
                    {% for mandatory in topic.literature %}
                      <li>
                       
                        <p>
                       <a href="[{{mandatory.title}}]({{mandatory.url}})">{{mandatory.title}}</a>
                       
                        
                            <span class="badges">
                            <span class="badge badge-info">article</span><span class="badge badge-secondary">12 min</span>
                          </span>
                          </p>
                          
                      </li>
                      {% endfor %}
                      
                    </ul>


                   <details markdown="1">
                    <summary>Frivillig fördjupningslitteratur innom {{topic.topic}} (klicka för att visa)</summary>
                    {% for optional in topic.optionalLiterature %}
                    * [{{optional.title}}]({{optional.url}})
                    {% endfor %}
                    </details>
                  </div>
                </div>
              </div>

             
              
             </div>   
              {% endfor %}
