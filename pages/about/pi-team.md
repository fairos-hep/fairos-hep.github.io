---
permalink: /about/pi-team.html
layout: default
title: PI Team
---

<div class="container-fluid">
  <h1>PI Team</h1><br>
  <p><b>The Principal Investigators for the NSF-funded FAIROS-HEP project are.</b></p>
  <div class="row">
  {% for member in site.data.orgs.pi-team.personnel  %}
     {% assign person = site.data.people[member] %}
       <div class="card" style="width: 12rem;">
         <img class="card-img-top" src="{{person.photo}}" alt="Card image cap">
         <div class="card-body d-flex flex-column">
         <div class="card-text">
         <b><a href="{{person.website}}">{{person.name}}</a></b><br>
         <small>{{person.institution}}</small><br><br>
         {% if person.e-mail %}
           <small>
             <a href="mailto:{{person.e-mail}}">
               <em>{{person.e-mail}}</em>
             </a>
           </small><br><br>
         {% endif %}
         </div>
         <div class="card-text mt-auto"><i>{{person.title}}</i><br></div>
         </div>
       </div>
  {% endfor %}
  </div>
  <br>
</div>
