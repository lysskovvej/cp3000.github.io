---
title: Coding Pirates Helsingør
---

# Coding Pirates "Helsingør"

We are the Elsinore chapter of [CodingPirates](https://codingpirates.dk/).

- [Public Facebook Group](https://www.facebook.com/groups/CodingPiratesHelsingoer/)

- [Mobile](./mobile.md)

<div class="posts">
  {% for post in site.posts %}
    <article class="post">

      <h1><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>

      <div class="entry">
        {{ post.excerpt }}
      </div>

      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
    </article>
  {% endfor %}
</div>
<div>

</div>
