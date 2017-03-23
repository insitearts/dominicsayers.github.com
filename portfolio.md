---
layout: portfolio
title: Projects
---
<div class="portfolio-items">
  {% for portfolio_data in site.portfolio %}
  <div class="portfolio-item{% if portfolio_data.status == 'complete' %} complete{% endif %}">
    <h3><a href="{{ portfolio_data.url }}" target="portfolio">
      {{ portfolio_data.name }}{% if portfolio_data.status == 'complete' %} <span class="prompt">(complete)</span>{% endif %}
    </a></h3>
    <h4><span class="prompt">Client:</span> {{ portfolio_data.client }}</h4>
    {% if portfolio_data.thumbnail %}
    <div class="thumbnail" itemprop="image" itemscope itemtype="https://schema.org/ImageObject">
      <a href="{{ portfolio_data.url }}" target="portfolio">
        <img itemprop="url" src="https://res.cloudinary.com/insite-arts/image/upload/c_scale,h_178,w_308/v1490175894/website/{{ portfolio_data.thumbnail }}">
      </a>
    </div>
    {% endif %}
    {% if portfolio_data.note %}<p>{{ portfolio_data.note }}</p>{% endif %}
    {% if portfolio_data.artists %}
      <dl>
        <dt class="prompt">Artist{% if portfolio_data.artists.length > 1 %}s{% endif %}:</dt>
        {% for artist in portfolio_data.artists %}
        <dd>{{ artist }}</dd>
        {% endfor %}
      </dl>
    {% endif %}
  </div>
  {% endfor %}

  <div class="portfolio-item">
    <h3>Other recent projects</h3>
    <p>Call for more details</p>

    <ul>
      <li><a href="/live-the-life-you-imagine">One St Peter’s Square</a></li>
      <li>North West Cambridge</li>
      <li>London 2012 Olympic Delivery Authority</li>
      <li><a href="/olympic-park">London 2012 Olympic Park</a></li>
    </ul>

    <dl>
      <dt class="prompt">Artists:</dt>
      <dd>Mark Titchner</dd>
      <dd>Kenny Hunter</dd>
      <dd>Neville Gabie</dd>
      <dd>Clare Woods</dd>
      <dd>DJ Simpson</dd>
    </dl>
  </div>

  <div class="portfolio-item">
    <h3>Past projects</h3>
    <p>Call for more details</p>

    <ul>
      <li><a href="/cabotcircus">Bristol Cabot Circus</a></li>
      <li>Exeter Princesshey</li>
      <li>Leicester High Cross</li>
      <li>Canterbury Whitefriars</li>
      <li>Sainsbury Laboratory</li>
      <li>Forest of Dean Sculpture Trust</li>
      <li>Trumpington Meadows Art Programme</li>
    </ul>
  </div>

  <div class="portfolio-item">
    <h3>Other artists we've commissioned</h3>
    <p>Call for more details</p>
    <dl>
      <dd>Bedwry Williams</dd>
      <dd>Clare Morgan</dd>
      <dd>Clare Twomey</dd>
      <dd>Dan Perjovski</dd>
      <dd>David Ward</dd>
      <dd>Dryden Goodwin</dd>
      <dd>Esther Rolinson</dd>
      <dd>Grennan and Sperandio</dd>
      <dd>Heinrich and Palmer</dd>
      <dd>Jacqui Poncelet</dd>
      <dd>Janet Hodgson</dd>
      <dd>John Newling</dd>
      <dd>Josh Portaway</dd>
      <dd>Julie Westerman</dd>
      <dd>Lulu Quinn</dd>
      <dd>Marie Jean Hoffner</dd>
      <dd>Marion Kalmus</dd>
      <dd>Martin Richman</dd>
      <dd>Martine Neddam</dd>
      <dd>Muf art and architecture</dd>
      <dd>Nayan Kulkarni</dd>
      <dd>Pope and Guthrie Somewhere</dd>
      <dd>Ralph Hoyte</dd>
      <dd>Ruth Proctor</dd>
      <dd>Studio Rosso</dd>
      <dd>Susanna Heron</dd>
      <dd>Tania Kovats</dd>
      <dd>Timorous Beasties</dd>
      <dd>Tony Sinden</dd>
      <dd>William Pye</dd>
      <dd>Winter and Horbelt</dd>
    </dl>
  </div>
</div>
