---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

## Journal Articles & Presentations

<ol>
{% for pub in site.data.publications %}
  {% assign authors_bold = pub.authors | replace: "Miyata, K.", "**Miyata, K.**" %}

  <li>
    {% if pub.doi != "" %}
      <a href="{{ pub.doi }}"><strong>{{ pub.title }}</strong></a>
    {% else %}
      <strong>{{ pub.title }}</strong>
    {% endif %}
    <br>
    {{ authors_bold }}<br>
    <em>{{ pub.journal }}</em>, {{ pub.year }}
  </li>
{% endfor %}
</ol>
