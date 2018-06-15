---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: page
---
<!-- Home -->
  <div class="wrapper style1">
    <article class="container" id="intro">
      <div>

          {% include home-intro.html%}

      </div>
    </article>
  </div>
  <div class="wrapper style1">
    <article class="container" id="wanted">
      <div>
        <h1>Alegria zoekt gitaristen!</h1>
        <p>
        Zin om mee te spelen bij een enthousiaste groep gitaristen? Zin om er het beste van je muzikale en gitaristieke kunnen te geven? Zin om mee te genieten van de sfeer en van onze dirigentes Charlotte en Marleen?
        </p>
        Heb je de Middelbare graad 3 in de academie afgewerkt of ben je afgestudeerd aan de muziekacademie? Stuur dan ‘presto’ een mailtje naar <a href="mailto:charlottelammertijn@yahoo.com">charlottelammertijn@yahoo.com</a>
        of <a href="mailto:marleencasteele@gmail.com">marleencasteele@gmail.com</a> en kom proef-repeteren bij de plezantste groep van ’t land!
      </div>
    </article>
  </div>

  <!-- optredens -->
  <div class="wrapper style2">
    <article id="events">
      {% include home-events.html %}
    </article>
  </div>

  <!-- muziek -->
  <div class="wrapper style1">
    <article id="music">
      {% include home-music.html %}
    </article>
  </div>

  <!-- links -->
  <div class="wrapper style2">
    <article id="links">
      {% include home-links.html %}
    </article>
  </div>

  <!-- contact -->
  <div class="wrapper style3">
    <article id="contact">
      {% include home-contact.html %}
    </article>
  </div>

  <!-- fotos -->
  <div class="wrapper style1">
    <article id="fotos">
      Fancy link to fotogallerijen
    </article>
  </div>
