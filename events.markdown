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
            <a href="#" class="image featured">
              <img src="http://via.placeholder.com/350x350"/>
            </a>
            <h3><a href="{{event.url}}">{{event.date | date: "%d %b %Y"}}<br/>{{event.title}}</a></h3>        
          </section>
        </div>
      {% endfor %}
    </div>
  </article>
</div>
