---
layout: page
title: Optredens
---

<div class="wrapper style1 first">
  <header>
	   <h2>Optredens</h2>
						<!-- if you want to add a subtitle or description, use a paragraph-->
	</header>
  <article class="container">
    <div class="row">
      {% for event in site.events%}
        <div class="4u 12u(mobile)">
          <section class="box style1">
            <!--
            Example icon
            <span class="icon featured fa-thumbs-o-up"></span>
            -->
            <h3>{{event.title}}</h3>
            <p>{{event.date | date: "%d %b %Y"}} <br/><a href="{{event.url}}">Meer informatie</a></p>

          </section>
        </div>
      {% endfor %}
    </div>
  </article>
</div>
