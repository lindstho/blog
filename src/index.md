---
layout: base.njk
permalink: index.html
title: /blog
description: This blog is a blog
featured_image: favicon.png
---
Welcome to my blog! This is mostly here because I wanted to learn how to make a page with eleventy. I'm not sure what I want to put here just yet.

--- 
<!-- This next part will show your top three most recent posts. You can change how readableDate looks in your .eleventy.js file-->
## Recent Blog Posts

<div id="recentpostlistdiv">
  <ul>
  {% assign top_posts = collections.posts | reverse %}
	{%- for post in top_posts limit:6 -%}
		<li><a href="{{ post.data.permalink }}">{{ post.data.date | readableDate }} » {{ post.data.title }}</a></li>
	{% endfor %}<li class="moreposts"><a href="archives.html">» Archives</a></li><li class="moreposts"><a href="rss.xml">» RSS feed</a></li></ul>
</div>
