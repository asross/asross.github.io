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
</style>

<!--Most are also listed on <a href='https://scholar.google.com/citations?user=Lf-StbQAAAAJ&hl=en' target='_blank'>Google Scholar</a>.-->

{% for p in site.data.publications %}
  <div class='publication'>
    <strong class='publication-title'>
      {{ p.title }}
    </strong>
    <div class='publication-authors'> {{ p.authors }} </div>
    <div class='publication-venue'>
      <em>{{ p.venue }}</em>, {{ p.year }}
      {% if p.pdf %}
        <a href='{{p.pdf}}'>[pdf]</a>
      {% endif %}
      {% if p.link %}
        <a href='{{p.link}}'>[link]</a>
      {% endif %}
      {% if p.code %}
        <a href='{{p.code}}'>[code]</a>
      {% endif %}
    </div>
  </div>
{% endfor %}
