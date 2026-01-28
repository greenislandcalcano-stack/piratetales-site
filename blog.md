---
layout: default
title: Cantos del Mar
permalink: /blog/
description: Fragments, meditations, and lost pages from the world of Pirate Tales.
---

<section class="cin-hero">
  <div class="cin-hero__bg"></div>
  <div class="cin-hero__vignette"></div>
  <div class="cin-hero__grain"></div>

  <div class="cin-hero__fog cin-hero__fog--a"></div>
  <div class="cin-hero__fog cin-hero__fog--b"></div>

  <div class="cin-hero__wreck-light"></div>

  <div class="container cin-hero__content">
    <p class="cin-hero__kicker">Pirate Tales • Cantos del Mar</p>
    <h1 class="cin-hero__title">Cantos del Mar</h1>
    <p class="cin-hero__lead">
      Fragments, meditations, and lost pages—where destiny dreams in salt and steel.
    </p>

    <div class="cin-hero__cta">
      <a class="btn btn--gold" href="{{ '/tales/begin/' | relative_url }}">Begin the Journey</a>
      <a class="btn" href="{{ '/' | relative_url }}#saga">Return to the Saga</a>
    </div>

    <a class="cin-hero__scroll" href="#posts" aria-label="Scroll to posts">
      <span class="cin-hero__scroll-line"></span>
      <span class="cin-hero__scroll-text">Scroll</span>
    </a>
  </div>
</section>

<section id="posts" class="section">
  <div class="container">
    <h2 class="sr-only">Posts</h2>

    {% for post in site.posts %}
      <article class="blog-canto">
        <p class="blog-canto__meta">
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
        </p>

        <h2 class="blog-canto__title">
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </h2>

        {% if post.description %}
          <p class="blog-canto__desc">{{ post.description }}</p>
        {% endif %}

        <a class="blog-canto__read" href="{{ post.url | relative_url }}">Read the canto →</a>
      </article>
    {% endfor %}
  </div>
</section>
