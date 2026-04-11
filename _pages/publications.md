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
  <li style="margin-bottom: 1.5em;">
    {% comment %} 1. タイトル（DOIリンク） {% endcomment %}
    {% if pub.doi != "" %}
      <a href="{{ pub.doi }}"><strong>{{ pub.title }}</strong></a>
    {% else %}
      <strong>{{ pub.title }}</strong>
    {% endif %}
    <br>
    {% comment %} 
      2. 著者名：HTMLタグを有効にするために「markdownify」フィルタを通します 
    {% endcomment %}
    {{ pub.authors | markdownify | remove: '<p>' | remove: '</p>' }} ({{ pub.year }}).<br>
    {% comment %} 3. 雑誌名, 巻(号), ページ. {% endcomment %}
    <em>{{ pub.journal }}</em>{% if pub.volume %}, <em>{{ pub.volume }}</em>{% endif %}{% if pub.issue %}({{ pub.issue }}){% endif %}, {{ pub.pages }}.
  </li>
{% endfor %}
</ol>
