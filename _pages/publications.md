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
  {% comment %} 名前の太字処理（英語・日本語両方に対応） {% endcomment %}
  {% assign authors_bold = pub.authors | replace: "Kohei Miyata", "**Kohei Miyata**" | replace: "宮田 康平", "**宮田 康平**" %}

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
