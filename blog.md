---
layout: page
title: Блог
profile: 1
permalink: blog/
---

### Мои сочинения

<ul class="list">
{%for post in site.categories['blog']%}
	<li>
		<a href="{{post.url}}">
			<div class="title">
				{{post.title}}
				<span class="date">{{post.date|date:'%d.%m.%Y'}}</span>
			</div>
		</a>
			<div class="cite">
				{{post.content|strip_html|truncatewords:20,"..."}}
				<br/><a href="{{post.url}}">Читать весь текст</a> (слов: {{post.content|number_of_words}}).
			</div>
	</li>
	<hr/>
{%endfor%}
</ul>
