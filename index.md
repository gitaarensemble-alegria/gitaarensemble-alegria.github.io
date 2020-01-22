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
 
{% if events.size > 0 %} <!-- are there any upcoming events? -->
<section id="three" class="wrapper style3 special">
						<div class="inner">
							<ul class="features">
								<li class="icon fa-calendar-check-o">
									<h3>{{first_upcoming.title}}</h3>
									<a href="{{first_upcoming.url}}" class="button primary">Informatie</a>
								</li>
							</ul>
						</div>
					</section>
{% endif %}
<section id="one" class="wrapper style1 special">
    <div class="inner">
        <header class="major">
            <h2>Alegría</h2>
            <p>
                bestaat uit een 20-tal enthousiaste gitaristen die onder leiding van onze dirigenten Marleen Casteele en Charlotte Lammertijn een repertoire gaande van renaissance- tot popmuziek brengen. Naast de klassieke gitaar bespelen we bas- en octaafgitaar(evenals) en ook elektrische gitaar. Soms wordt daar percussie, blokfluit, dwarsfluit of cello aan toegevoegd.
            </p>
            <p>
                We doen vaak mee aan muzikale evenementen, zoals ‘Dag van de Gitaar’, ‘Cultuurmarkt Waregem’ en wedstrijden. Zo werden we in 2008 eerste laureaat van de Ottoboni-kamermuziekwedstrijd in Lier met 90 % en daar zijn we trots op! In 2011 namen we deel aan het internationale festival Mondomusica in Cremona (Italië) wat ook een onvergetelijke gebeurtenis was.
            </p>

            <p>
                Alegría maakt graag kennis met binnen- en buitenlandse gitaarensembles en koren, waarmee duoconcerten georganiseerd worden. Alegría was te gast in Cambridge (GB), Rheine (Duitsland), Mirandola (Italië) en Juvisy-sur-Orge (Frankrijk). We werkten samen met de gitaarensembles Cuerda (Antwerpen), Color (Schaarbeek), het gitaarduo Flâmas en met enkele koren, ondermeer La Gioia (Vichte) en Amaranthe (Oudenaarde).
            </p>

            <p>
                Indien u geïnteresseerd bent in een concert of een muzikale omlijsting van recepties, huwelijken of andere evenementen kan u contact opnemen via dit formulier.
            </p>
            <p>
                Met vriendelijke groeten, Gitaarensemble Alegria
            </p>
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