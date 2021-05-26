---
layout: single
title : Produção bibliográfia e técnica
date  : 2020-04-28
permalink: /biblio/
---
{% include group-by-array.html collection=site.data.biblio.references field='type' %}

<ul style="list-style: none;">
  {% for tag in group_names %}
    {% assign posts = group_items[forloop.index0] %}
    <li>
    {% assign posts_title = site.data.bibtypes | find: "type", tag %}
      <h2 id="{{ tag }}">{{ posts_title.name }}</h2>
      <ol>
        {% for post in posts %}
        <li>
          <a href='{{ site.baseurl }}{{ post.url }}'>{{ post.title }}</a>
        </li>
        {% endfor %}
      </ol>
    </li>
  {% endfor %}
</ul>
