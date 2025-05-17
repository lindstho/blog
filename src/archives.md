---
layout: base.njk
permalink: archives.html
title: Archives
description: These are where old posts go!
featured_image: layout/favicon.png
---
Excuse the mess

---

## Journal

<!--This next part shows all of your posts tagged "journal" in reverse chronological order-->

<ul class="none">
{% assign top_journal = collections.journal | reverse %}
{%- for post in top_journal -%}
  <li><a href="{{ post.data.permalink }}">{{ post.data.date | readableDate }} » {{ post.data.title }}</a></li>
{% endfor %}
</ul>

---

## Reads

<!--This next part shows all of your posts tagged "reads" in reverse chronological order-->

<ul class="none">
{% assign top_reads = collections.reads | reverse %}
{%- for post in top_reads -%}
  <li><a href="{{ post.data.permalink }}">{{ post.data.date | readableDate }} » {{ post.data.title }}</a></li>
{% endfor %}
</ul>

---

## All Posts

<!--This next part shows all of your posts tagged "posts" in reverse chronological order-->

<ul class="none">
{% assign top_posts = collections.posts | reverse %}
{%- for post in top_posts -%}
  <li><a href="{{ post.data.permalink }}">{{ post.data.date | readableDate }} » {{ post.data.title }}</a></li>
{% endfor %}
</ul>