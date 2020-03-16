---
layout: page
---
{% assign events = site.events | where: 'published',true %}


{% assign first_upcoming = events[0] %}
{% assign first_performance = first_upcoming.performances[0] %}
{% for event in events %}
  {% for performance in event.performances %}
    {% assign first_upcoming_seconds = first_upcoming | date: "%s" %}
    {% assign performance_seconds = performance | date: "%s" %}
    {% assign now = site.time | date: "%s" %}
    {% if performance_seconds < first_upcoming_seconds and performance_seconds>now%}
      {% assign first_upcoming = event %}
      {% assign first_performance = performance %}
    {% endif %}
  {% endfor %}
{% endfor %}
 
 <section id="three" class="wrapper style3 special">
    <div class="inner">
        <header class="major">
        <h2>Concertweekend uitgesteld</h2>
        <p>
        Om de verspreiding van het coronavirus in te dijken zal de Stedelijke Kunstacademie (hoofdschool en vestigingen) alle lessen en activiteiten schrappen vanaf zaterdag 14 maart tot en met 4 april.
        </p>
        <p>
        Daarom wordt het concertweekend van 21 en 22 maart 2020 uitgesteld.
        </p>
        </header>
    </div>
</section>
 
{% if events.size > 0 %} <!-- are there any upcoming events? -->
<section id="three" class="wrapper style3 alt">
<section class="spotlight">
<div class="image">
  <img src="{{first_upcoming.asset}}" />
</div>
						<div class="content">
							
								
									<h2>{{first_upcoming.title}}</h2>
									<p>{{first_upcoming.description}}</p>
									<p><a href="{{first_upcoming.url}}" class="button primary">Informatie</a></p>
								
						</div>
					</section>
					</section>
{% endif %}
<section id="one" class="wrapper style1 special">
    <div class="inner">
        <header class="major">
        <!-- Adding the markdown attribute to the div, no trailing whitespace!!! -->
        <div markdown="1">
## Alegría
            
is een enthousiaste groep gitaristen die onder leiding van [Charlotte Lammertijn]({% link charlotte.md %}) wekelijks mag doen wat het graag doet, namelijk samen muziek maken. Diverse muziekstijlen passeren de revue, van klassiek tot modern. Naast onze klassieke gitaren wordt er aanvullend ook basgitaar, octaafgitaar, elektrische gitaar en soms ook percussie gespeeld.
            
Daarnaast nemen we graag deel aan muzikale evenementen zoals 'dag van de gitaar' en  cultuurmarkten. Wedstrijden gaan we eveneens niet uit de weg zoals de Ottoboni-kamermuziekwedstrijd te Lier en Mondomusica in Cremona (Italië).
            
Alegría maakt graag kennis met binnen- en buitenlandse gitaarensembles en koren, waarmee duoconcerten georganiseerd worden. Alegría was reeds te gast in Cambridge (GB), Rheine (Duitsland), Mirandola (Italië), Juvisy-sur-Orge (Frankrijk), Hongarije en Groningen (Nederland). We werkten samen met de gitaarensembles Cuerda (Antwerpen), Color (Schaarbeek), het gitaarduo Flâmas en met enkele koren, ondermeer La Gioia (Vichte) en Amaranthe (Oudenaarde).            

Dit jaar is Alegría te gast in Rheine (Duitsland) en in maart 2021 komt het Hongaarse gitaarensemble naar België om samen met Alegría een duoconcertweekend te spelen.            

Indien u geïnteresseerd bent in een concert of een muzikale omlijsting van recepties, huwelijken of andere evenementen kan u [contact met ons opnemen](mailto:info@gitaarensemble-alegria.be?subject=Meer info over een concert).

Met vriendelijke groeten, Gitaarensemble Alegria
</div>
        </header>
        <!--
        <ul class="icons major">
            <li><span class="icon fa-gem major style1"><span class="label">Lorem</span></span></li>
            <li><span class="icon fa-heart major style2"><span class="label">Ipsum</span></span></li>
            <li><span class="icon solid fa-code major style3"><span class="label">Dolor</span></span></li>
        </ul>
        -->
    </div>
</section>  