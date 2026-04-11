---
layout: archive
title: "Talks"
permalink: /talks/
author_profile: true
---

{% include base_path %}

## Invited Talks
<ol>
{% assign invited = site.data.talks | where_exp: "item", "item.type contains 'invited'" %}
{% for talk in invited %}
<li style="margin-bottom: 1em;">
  <strong>{{ talk.title }}</strong><br>
  {{ talk.authors | markdownify | remove: '<p>' | remove: '</p>' | strip }}<br>
  <em>{{ talk.venue }}</em>, {{ talk.location }}, {{ talk.date }}.
</li>
{% endfor %}
</ol>

## International Conferences (Oral)
<ol>
{% assign int_oral = site.data.talks | where_exp: "item", "item.type contains 'int_oral'" %}
{% for talk in int_oral %}
<li style="margin-bottom: 1em;">
  <strong>{{ talk.title }}</strong><br>
  {{ talk.authors | markdownify | remove: '<p>' | remove: '</p>' | strip }}<br>
  <em>{{ talk.venue }}</em>, {{ talk.location }}, {{ talk.date }}.
</li>
{% endfor %}
</ol>

## International Conferences (Poster)
<ol>
{% assign int_poster = site.data.talks | where_exp: "item", "item.type contains 'int_poster'" %}
{% for talk in int_poster %}
<li style="margin-bottom: 1em;">
  <strong>{{ talk.title }}</strong><br>
  {{ talk.authors | markdownify | remove: '<p>' | remove: '</p>' | strip }}<br>
  <em>{{ talk.venue }}</em>, {{ talk.location }}, {{ talk.date }}.
</li>
{% endfor %}
</ol>

## Domestic Conferences in Japan (Oral)
<ol>
{% assign dom_oral = site.data.talks | where_exp: "item", "item.type contains 'dom_oral'" %}
{% for talk in dom_oral %}
<li style="margin-bottom: 1em;">
  <strong>{{ talk.title }}</strong><br>
  {{ talk.authors | markdownify | remove: '<p>' | remove: '</p>' | strip }}<br>
  <em>{{ talk.venue }}</em>, {{ talk.location }}, {{ talk.date }}.
</li>
{% endfor %}
</ol>

## Domestic Conferences in Japan (Poster)
<ol>
{% assign dom_poster = site.data.talks | where_exp: "item", "item.type contains 'dom_poster'" %}
{% for talk in dom_poster %}
<li style="margin-bottom: 1em;">
  <strong>{{ talk.title }}</strong><br>
  {{ talk.authors | markdownify | remove: '<p>' | remove: '</p>' | strip }}<br>
  <em>{{ talk.venue }}</em>, {{ talk.location }}, {{ talk.date }}.
</li>
{% endfor %}
</ol>
