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
  {% comment %} 
    名前の置換：HTMLタグを直接使い、最後に「| markdownify」を通さず
    そのまま出力されるように調整します。
  {% endcomment %}
  {% assign authors_html = pub.authors | replace: "Miyata, K.", "<strong>Miyata, K.</strong>" %}

  <li style="margin-bottom: 1.5em;">
    {% comment %} 1. 著者名 (発行年). {% endcomment %}
    {{ authors_html }} ({{ pub.year }}). <br>

    {% comment %} 2. 論文タイトル（リンク） {% endcomment %}
    {% if pub.doi != "" %}
      <a href="{{ pub.doi }}"><strong>{{ pub.title }}</strong></a>.
    {% else %}
      <strong>{{ pub.title }}</strong>.
    {% endif %}
    <br>

    {% comment %} 3. 雑誌名, 巻(号), ページ. {% endcomment %}
    <em>{{ pub.journal }}</em>{% if pub.volume %}, <em>{{ pub.volume }}</em>{% endif %}{% if pub.issue %}({{ pub.issue }}){% endif %}{% if pub.pages %}, {{ pub.pages }}{% endif %}.
  </li>
{% endfor %}
</ol>
