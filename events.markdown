---
layout: page
title: Events
---
Event page listing
{% for event in site.data.events%}
<h2>{{event.title}}</h2>
{{event.date | date: "%a %d %b %Y %R"}}
<b>Price: </b> {{event.price_adult}}
{% if event.price_adult != event.price_kid %}
 {{event.price_kid}}
{% endif %}
{% if event.ticket_url %}
 <a href="{{event.ticket_url}}">Buy tickets</a>
{% endif %}
{% endfor %}
