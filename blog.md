---
layout: page
title: Блог
permalink: blog/
---

<div class="posts">
{%for post in site.categories['blog']%}
  <section class="post">
    <header class="post-header">
      <h1 class="post-title"><a href="{{post.url}}">{{post.title}}</a></h1>

    </header>

    <div class="post-description">
      <p>
        {{post.content|strip_html|truncatewords:20,"..."}}
      </p>
    </div>
    <p class="post-meta">
      Дата: {{post.date|date:'%d.%m.%Y'}}. Слов: {{post.content|number_of_words}}.
      <a href="{{post.url}}">Читать >>...</a>
    </p>
  </section>
{%endfor%}
</div>
