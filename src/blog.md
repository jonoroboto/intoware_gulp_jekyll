---
title: Blog
permalink: "/blog/"
layout: page
---

<div class="home">

  <ul class="post-list">
    {% for post in site.posts %}
    <div class="Container__outer">
      <li class="Blog__meta">
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
      </li>
      <div class="BG__overlay"></div>
      <div class="Container__image js-tilt" style="background: url({{ site.baseurl }}/assets/images/imagens/{{ post.image }}); background-position: center; background-size: cover; background-blend-mode: screen;"></div>
    </div>
    {% endfor %}
  </ul>

  <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>
</div>
