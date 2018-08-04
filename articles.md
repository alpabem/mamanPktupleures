---
layout: page
title: Articles
permalink: "/articles/"
image: assets/images/pic11.jpg
---

<br><br>

{% for post in site.posts %}
  <article class="">
		<div class="article-head">
    <a href="{{ post.url }}" class="image"><img src="{{ post.image | absolute_url }}" alt="" /></a>
			<h2 class="title">{{ post.title }}</h2>
			<p class="date">{{ post.date | date: "%b %d, %Y" }}</p>
		</div><!--/.article-head-->
		<div class="article-content">
		{{ post.description | strip_html | truncatewords: 100 }}
		<br><a href="{{ post.url }}" class="full-post-link js-pjax">En savoir plus</a>	
    <hr>
		</div><!--/.article-content-->
	</article>
	
{% endfor %}