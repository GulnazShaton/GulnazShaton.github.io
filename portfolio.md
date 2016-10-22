---
layout: page
title: Портфолио
permalink: portfolio/
---

<ul class="list">
{%for post in site.categories['portfolio']%}
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
