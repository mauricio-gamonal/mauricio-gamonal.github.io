<link rel="shortcut icon" type="image/x-icon" href="./Uroboro.ico">

<div class="hero-card">

  <img src="/Perfil-PennState-circle.png"
       alt="Mauricio's profile picture"
       class="hero-avatar">

  <div class="hero-text">
    <h2 style="text-align:center; margin-top:0;">Mauricio Gamonal</h2>
    <ul style="list-style:none; padding-left:0; line-height:1.5;">
    <li><strong>Theoretical Physicist</strong></li>
    <li>PhD in Physics, Penn State (Advisor: <a href="https://ebianchi.org" target="_blank">Eugenio Bianchi</a>)</li>
    <li>MSc in Physics, PUC Chile (Advisor: <a href="https://www.fis.uc.cl/~academiasenior/web/JA/JA.html" target="_blank">Jorge Alfaro</a>)</li>
    <div style="margin-top:14px;"></div>
    <li> My research lies at the interface of quantum gravity and cosmology. I aim to explore how classical spacetime emerges from quantum geometry and how this process can leave observable imprints in the primordial Universe. </li>
  </ul>
  </div>
  
</div>


  <!-- News -->
<div class="news-card">
  <h2>News</h2>

  <ul class="news-list">
  {% for item in site.data.news %}
    <li style="margin-bottom: 12px;">
      <strong>{{ item.date }}</strong> — {{ item.title }}
      {% if item.kind == "link" or item.kind == "paper" %}
        {% if item.url %}
          &nbsp;<a href="{{ item.url }}" target="_blank" rel="noopener">(link)</a>
        {% endif %}
        {% if item.extra_links %}
          &nbsp;
          {% for l in item.extra_links %}
            <a href="{{ l.url }}" target="_blank" rel="noopener">[{{ l.label }}]</a>
          {% endfor %}
        {% endif %}
      {% elsif item.kind == "assets" %}
        {% if item.assets %}
          <div style="margin-top:6px;">
            {% for a in item.assets %}
              <a href="{{ a.url }}">[{{ a.label }}]</a>
            {% endfor %}
          </div>
        {% endif %}
      {% elsif item.kind == "youtube" %}
        {% if item.youtube_id %}
          <div style="margin-top:8px;">
            <iframe width="100%" height="220"
              src="https://www.youtube-nocookie.com/embed/{{ item.youtube_id }}"
              title="YouTube video"
              frameborder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
              allowfullscreen>
            </iframe>
          </div>
        {% endif %}
      {% endif %}
    </li>
  {% endfor %}
  </ul>
</div>

  <!-- Collaborators -->
  <div class="collab-card">
   I’m always happy to discuss the early Universe, foundational and phenomenological aspects of quantum gravity, and related questions in philosophy of science—and, more broadly, the creative process, current affairs, and other interesting facets of life. 
  </div>
