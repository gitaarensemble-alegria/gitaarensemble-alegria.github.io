---
layout: page
title: Alegria 10
tracks:
  - title: Minor Swing
    composer: Django Reinhart
    arranger: Marleen Casteele & Pieter-Jan Drouillon
  - title: Theme of Schindler's list
    composer: John Williams
---
{{title}}<br/>
Tracks:
<ol>
{% for t in page.tracks%}
<li><i>{{t.title}}</i> written by <i>{{t.composer}}</i></li>
{% endfor %}
</ol>
