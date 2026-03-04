<link rel="shortcut icon" type="image/x-icon" href="./Uroboro.ico">

<style>
.hero-card {
  position: relative;
  overflow: hidden;   /* keeps background inside rounded corners */
}

/* background layer only for the homepage */
.hero-card::before {
  content: "";
  position: absolute;
  inset: 0;

  background-image: url("/Tololo-Chile-final.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;

  opacity: 0.25;
  z-index: 0;
}

/* keep text and avatar above background */
.hero-card > * {
  position: relative;
  z-index: 1;
}
</style>


<div class="hero-card">

  <img src="/Perfil-PennState-circle.png"
       alt="Mauricio's profile picture"
       class="hero-avatar">

  <div class="hero-text">
    <h2 style="text-align:left; margin-top:0;">Mauricio Gamonal</h2>
    <ul style="list-style:none; padding-left:0; line-height:1.5;">
    <li><strong>Theoretical Physicist</strong></li>
    <li>PhD 2026, Penn State (Advisor: <a href="https://ebianchi.org" target="_blank">Eugenio Bianchi</a>)</li>
    <li>MSc 2021, PUC Chile (Advisor: <a href="https://www.fis.uc.cl/~academiasenior/web/JA/JA.html" target="_blank">Jorge Alfaro</a>)</li>
    <div style="margin-top:14px;"></div>
    <li> My research lies at the interface of quantum gravity and cosmology. I aim to explore how classical spacetime emerges from quantum geometry and how this process can leave observable imprints in the primordial Universe. </li>
  </ul>
  </div>
  
</div>


  <!-- News -->
<div class="news-card">
  <h2>Updates</h2>

  <ul class="news-list">
  {% for item in site.data.updates %}
    <li style="margin-bottom: 16px;">
  <strong>{{ item.date }}</strong> — {{ item.title }}

  {% if item.links %}
    &nbsp;
    {% for l in item.links %}
      <a href="{{ l.url }}" target="_blank" rel="noopener">[{{ l.label }}]</a>
    {% endfor %}
  {% endif %}

  {% if item.image %}
    <div style="margin-top:8px;">
      <img src="{{ item.image }}" 
           style="max-width:100%; border-radius:8px;">
    </div>
  {% endif %}

  {% if item.youtube_id %}
    <div style="margin-top:8px;">
      <iframe width="100%" height="300"
        src="https://www.youtube-nocookie.com/embed/{{ item.youtube_id }}"
        frameborder="0"
        allowfullscreen>
      </iframe>
    </div>
  {% endif %}
</li>
  {% endfor %}
  </ul>
</div>

  <!-- Collaborators -->
  <div class="collab-card">
   I’m always happy to discuss the early Universe, foundational and phenomenological aspects of quantum gravity, and related questions in philosophy of science—and, more broadly, the creative process, current affairs, and other interesting facets of life. 
  </div>
