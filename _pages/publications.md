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
  <li>
    **{{ pub.title }}**<br>
    {{ pub.authors }}<br>
    *{{ pub.journal }}*, {{ pub.year }} 
    {% if pub.link %}[[Link]({{ pub.link }})]{% endif %}
  </li>
{% endfor %}
</ol>
