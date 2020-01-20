---
layout: page
title: Optredens
---

<section class="wrapper style1">
  <div id="portfolio" class="inner">
  {% assign now = site.time %}
  {% assign events = site.events | where: 'published',true %}
    <table>
    {% for event in events %}
    <tr>
        <td>{{event.date_start| date: "%d %b %Y"}}</td>
        <td>{{event.title}}</td>
        <td><a href="{{event.url}}">Meer informatie</a></td>   
        <td></td>
              
    </tr>
          
          {% endfor %}
          </table>
  </div>
</section>
