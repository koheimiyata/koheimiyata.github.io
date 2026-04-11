---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>{% endif %}
{% include base_path %}

<ol>
{% for pub in site.data.publications %}
<li style="margin-bottom: 1.5em;">
{% if pub.doi != "" %}<a href="{{ pub.doi }}"><strong>{{ pub.title }}</strong></a>{% else %}<strong>{{ pub.title }}</strong>{% endif %}<br>
{% assign authors_with_bold = pub.authors | replace: "Miyata, K.", "**Miyata, K.**" %}{{ authors_with_bold | markdownify | remove: '<p>' | remove: '</p>' | strip }} ({{ pub.year }}).<br>
<em>{{ pub.journal }}</em>{% if pub.volume %}, <em>{{ pub.volume }}</em>{% endif %}{% if pub.issue %}({{ pub.issue }}){% endif %}, {{ pub.pages }}.
</li>
{% endfor %}
</ol>
