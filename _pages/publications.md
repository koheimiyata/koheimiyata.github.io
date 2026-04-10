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

<ol>
{% for pub in site.data.publications %}
  {% assign authors_html = pub.authors | replace: "Miyata, K.", "<strong>Miyata, K.</strong>" %}

  <li style="margin-bottom: 1.5em;">
    <br>
    {% if pub.doi != "" %}
      <a href="{{ pub.doi }}"><strong>{{ pub.title }}</strong></a>.
    {% else %}
      <strong>{{ pub.title }}</strong>.
    {% endif %}
    <br>
    {{ authors_html }} ({{ pub.year }}) 
    <em>{{ pub.journal }}</em>{% if pub.volume %}, <em>{{ pub.volume }}</em>{% endif %}{% if pub.issue %}({{ pub.issue }}){% endif %}{% if pub.pages %}, {{ pub.pages }}{% endif %}.
  </li>
{% endfor %}
</ol>
