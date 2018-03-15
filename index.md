---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: page
---
<!-- Home -->
  <div class="wrapper style1">
    <article class="container">
      <div>

          {% include home-intro.html%}

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
