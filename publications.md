---
layout: default
title: Publications
---

<style>
.publication + .publication {
  margin-top: 1rem;
}

.publication-authors {
  opacity: 0.75;
  font-size: 1rem;
}

.scholar {
  margin-top: -1rem;
}
</style>

<p class='scholar'>
  Most are also listed on <a href='https://scholar.google.com/citations?user=Lf-StbQAAAAJ&hl=en' target='_blank'>Google Scholar</a>.
</p>

{% for p in site.data.publications %}
  <div class='publication'>
    <strong class='publication-title'>
      {{ p.title }}
    </strong>
    <div class='publication-authors'> {{ p.authors }} </div>
    <div class='publication-venue'>
      <em>{{ p.venue }}</em>, {{ p.year }}
      {% if p.pdf %}
        <a href='{{p.pdf}}' target='_blank'>[pdf]</a>
      {% endif %}
      {% if p.link %}
        <a href='{{p.link}}' target='_blank'>[link]</a>
      {% endif %}
      {% if p.code %}
        <a href='{{p.code}}' target='_blank'>[code]</a>
      {% endif %}
      {% if p.preprint %}
        <a href='{{p.preprint}}' target='_blank'>[preprint]</a>
      {% endif %}
      {% if p.long_version %}
        <a href='{{p.long_version}}' target='_blank'>[extended version]</a>
      {% endif %}
      {% if p.slides %}
        <a href='{{p.slides}}' target='_blank'>[slides]</a>
      {% endif %}
      {% if p.poster %}
        <a href='{{p.poster}}' target='_blank'>[poster]</a>
      {% endif %}
    </div>
  </div>
{% endfor %}
