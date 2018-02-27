---
layout: page
title: Events
---
{% for event in site.events%}
<a href="{{event.url}}">{{event.title}}</a><br/>
{% endfor %}
