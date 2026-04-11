---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>{% endif %}
{% include base_path %}

## Journal Articles
<ol>
{% assign journals = site.data.publications | where: "type", "journal" %}
{% for pub in journals %}
<li style="margin-bottom: 1.5em;">
{% if pub.doi != "" %}<a href="{{ pub.doi }}"><strong>{{ pub.title }}</strong></a>{% else %}<strong>{{ pub.title }}</strong>{% endif %}<br>
{{ pub.authors | replace: "Miyata, K.", "<b>Miyata, K.</b>" }} ({{ pub.year }}).<br>
<em>{{ pub.journal }}</em>{% if pub.volume %}, <em>{{ pub.volume }}</em>{% endif %}{% if pub.issue %}({{ pub.issue }}){% endif %}, {{ pub.pages }}.
</li>
{% endfor %}
</ol>

## Conference Proceedings
<ol>
{% assign proceedings = site.data.publications | where: "type", "proceeding" %}
{% for pub in proceedings %}
<li style="margin-bottom: 1.5em;">
{% if pub.doi != "" %}<a href="{{ pub.doi }}"><strong>{{ pub.title }}</strong></a>{% else %}<strong>{{ pub.title }}</strong>{% endif %}<br>
{{ pub.authors | replace: "Miyata, K.", "<b>Miyata, K.</b>" }} ({{ pub.year }}).<br>
<em>{{ pub.journal }}</em>{% if pub.pages %}, {{ pub.pages }}{% endif %}.
</li>
{% endfor %}
</ol>
