{% for project in include.projects %}
  <div class="project{% if project.status == 'complete' %} complete{% endif %}">
    <h3><a href="{{ project.url }}" target="project">
      {{ project.name }}{% if project.status == 'complete' %} <span class="prompt">(complete)</span>{% endif %}
    </a></h3>
    <h4><span class="prompt">Client:</span> {{ project.client }}</h4>
    {% if project.thumbnail %}
    <div class="thumbnail" itemprop="image" itemscope itemtype="https://schema.org/ImageObject">
      <a href="{{ project.url }}" target="project">
        <img itemprop="url" src="https://res.cloudinary.com/insite-arts/image/upload/c_scale,h_178,w_308/v1490175894/website/{{ project.thumbnail }}">
      </a>
    </div>
    {% endif %}
    {% if project.note %}<p>{{ project.note }}</p>{% endif %}
    {% if project.artists %}
      <dl>
        <dt class="prompt">Artist{% if project.artists.length > 1 %}s{% endif %}:</dt>
        {% for artist in project.artists %}
        <dd>{{ artist }}</dd>
        {% endfor %}
      </dl>
    {% endif %}
  </div>
{% endfor %}
