---
layout: page
title: Muziek
permalink: /repertoire
menu: true
menu-order: 20
---
<section class="wrapper style1">
  <div id="repertoire" class="inner">

    <table>
        <thead>
        <tr>
            <th>Titel</th>
            <th>Componist</th>
            <th>Periode</th>
        </tr>
        </thead>
    {% for piece in site.data.repertoire %}
    {% assign length = piece.arranger | size %}
    <tr>
        <td>{{piece.title}}</td>
        <td>{{piece.composer}}{% if length > 0 %}, arrangement door {{piece.arranger}}{% endif %}
        </td>
        <td>{{piece.period}}</td>
    </tr>

          {% endfor %}
          </table>
  </div>
</section>
