---
layout: portfolio
title: Projects
---
<div class="portfolio-items">
  {% for portfolio_data in site.portfolio %}
  <div class="portfolio-item">
    <h3><a href="{{ portfolio_data.url }}" target="portfolio">{{ portfolio_data.name }}</a></h3>
    <h4>Client: {{ portfolio_data.client }}</h4>
    {% if portfolio_data.thumbnail %}
    <div class="thumbnail" itemprop="image" itemscope itemtype="https://schema.org/ImageObject">
      <a href="{{ portfolio_data.url }}" target="portfolio">
        <img itemprop="url" src="/assets/article_images{{ page.url }}{{ portfolio_data.thumbnail }}">
      </a>
    </div>
    {% endif %}
    {% if portfolio_data.note %}<p>{{ portfolio_data.note }}</p>{% endif %}
    {% if portfolio_data.artists %}
      <p>Artist{% if portfolio_data.artists.length > 1 %}s{% endif %}:</p>
      <ul>
        {% for artist in portfolio_data.artists %}
          <li>{{ artist }}</li>
        {% endfor %}
      </ul>
    {% endif %}
  </div>
  {% endfor %}

  <div class="portfolio-item">
    <h3>Other recent projects</h3>
    <p>Call for more details</p>
    <h4>One St Peter’s Square</h4>
    <h4><a href="http://www.lsqlondon.com/">LSQLONDON</a></h4>
    <h4>North West Cambridge</h4>
    <h4>London 2012 Olympic Delivery Authority</h4>
    <h4>London 2012 Olympic Park</h4>
    <p>Artists:</p>
    <ul>
      <li>Mark Titchner</li>
      <li>Kenny Hunter</li>
      <li>Neville Gabie</li>
      <li>Clare Woods</li>
      <li>DJ Simpson</li>
    </ul>
  </div>

  <div class="portfolio-item">
    <h3>Past projects</h3>
    <p>Call for more details</p>
    <h4>Bristol Cabot Circus</h4>
    <h4>Exeter Princesshey</h4>
    <h4>Leicester High Cross</h4>
    <h4>Canterbury Whitefriars</h4>
    <h4>Sainsbury Laboratory</h4>
    <h4>Forest of Dean Sculpture Trust</h4>
    <h4>Trumpington Meadows Art Programme</h4>
  </div>

  <div class="portfolio-item">
    <h3>Artists we've commisioned</h3>
    <p>Call for more details</p>
    <ul>
      <li>Dryden Goodwin</li>
      <li>Grennan and Sperandio</li>
      <li>Henirch and Palmer</li>
      <li>Susanna Heron</li>
      <li>Janet Hodgson</li>
      <li>Marie Jean Hoffner</li>
      <li>Ralph Hoyte</li>
      <li>Kenny Hunter</li>
      <li>Marion Kalmus</li>
      <li>Tania Kovats</li>
      <li>Nayan Kulkarni</li>
      <li>Clare Morgan</li>
      <li>Muf art and architecture</li>
      <li>Martine Neddam</li>
      <li>John Newling</li>
      <li>Dan Perjovski</li>
      <li>Jacqui Poncelet</li>
      <li>Josh Portaway</li>
      <li>Ruth Proctor</li>
      <li>William Pye</li>
      <li>Lulu Quinn</li>
      <li>Martin Richman</li>
      <li>Esther Rolinson</li>
      <li>DJ Simpson</li>
      <li>Tony Sinden</li>
      <li>Emma Smith</li>
      <li>Pope and Guthrie Somewhere</li>
      <li>Studio Rosso</li>
      <li>Timorous Beasties</li>
      <li>Mark Titchner</li>
      <li>Clare Twomey</li>
      <li>David Ward</li>
      <li>Julie Westerman</li>
      <li>Bedwry Williams</li>
      <li>Winter and Horbelt</li>
      <li>Clare Woods</li>
      <li>Caroline Wright</li>
      <li>Gordon Young</li>
    </ul>
  </div>
</div>
