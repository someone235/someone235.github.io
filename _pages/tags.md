---
title: Tags
description: "All of my blog posts sorted by tag"
permalink: /blog/tags
---

{%- assign sortedTags = site.tags | sort -%}

<div class="tag-list">

{% for tag in sortedTags %}

	<a href="#{{tag[0]}}" class="internal-link">{{ tag[0] }}&nbsp;({{ tag[1] | size }})</a>

{% endfor %}

</div>

{% for tag in sortedTags %}

<section class="posts-by-tag">

<h2 id="{{ tag[0] }}">{{ tag[0] }}</h2>

{% for post in tag[1] %}
<a href="{{ post.url }}" title="{{ post.title }}" class="internal-link">{{post.title}}</a>
{% endfor %}
<a href="#" class="internal-link">All Tags &#8593;</a>
</section>

{% endfor %}
