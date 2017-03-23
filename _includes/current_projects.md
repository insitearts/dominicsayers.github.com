{% for project in site.projects %}
<div class="project{% if project.status == 'complete' %} complete{% endif %}" markdown="1">
### [{{ project.name }}{% if project.status == 'complete' %} <span class="prompt">(complete)</span>{% endif %}]({{ project.url }}){:target="projects"}

#### <span class="prompt">Client:</span> {{ project.client }}

  {% if project.thumbnail %}
  <div class="thumbnail" itemprop="image" itemscope itemtype="https://schema.org/ImageObject" markdown="1">
[![](https://res.cloudinary.com/insite-arts/image/upload/c_scale,h_178,w_308/v1490175894/website/{{ project.thumbnail }}){:itemprop="url"}]({{ project.url }}){:target="projects"}
  </div>
  {% endif %}
  {% if project.note %}
{{ project.note }}
  {% endif %}

  {% if project.artists %}
    {% assign artist_count = project.artists | size %}
Artist{% if artist_count > 1 %}s{% endif %}:{% for artist in project.artists %}
: {{ artist }}{% endfor %}
  {% endif %}
</div>
{% endfor %}
