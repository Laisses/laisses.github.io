---
layout: default
---

# Ponto de Vista

## Artigos

<ol class="lista-de-artigos">
{% for post in site.posts %}
  <li>
    {% assign m = post.date | date: "%m" | minus: 1 %}
    {{ post.date | date: "%d de " }}{{ site.months[m] }}{{ post.date | date: " de %Y" }}
    <br />
    <a href="{{ post.url }}">{{ post.title }}</a>
    {{ post.excerpt }}
  </li>
{% endfor %}
</ol>
