---
permalink: /
title: "Mobility and Machine Intelligence Lab at Stony Brook"
hero_title: "Mobility and Machine Intelligence Lab"
hero_tagline: "Game theory and data-driven optimization for next-generation mobility and logistics systems — connectivity, electrification, and automation."
hero_cta_url: "/openings/"
hero_cta_text: "We are recruiting"
hero_image: "/images/hero.jpg"
excerpt: "Game theory and data-driven optimization for next-generation mobility and logistics systems."
redirect_from:
  - /about/
  - /about.html
---

<div class="page-section">
<div class="wrap">
<div class="page__content" markdown="1">

The Mobility and Machine Intelligence Lab (M2 Lab) at Stony Brook University brings together game theory and data-driven optimization to develop **next-generation modeling and computational tools** for mobility and logistics systems, with a focus on connectivity, electrification, and automation. See [Research](/research/) for details.

We are recruiting **fully funded PhD students** beginning Spring/Fall 2027, as well as motivated MS and BS students. See [Openings](/openings/) for details.

</div>
</div>
</div>

<div class="page-section page-section--band">
<div class="wrap">
<h2 class="page-title">News</h2>

{%- comment -%}
  The six most recent entries are shown; everything older collapses into the
  "Earlier news" disclosure, which only renders when it has something in it.
{%- endcomment -%}
{%- assign shown = 6 -%}
{%- assign news = site.data.news | sort: 'date' | reverse -%}
{%- assign archived_count = news.size | minus: shown -%}

<ul class="news-list">
{%- for item in news limit: shown %}
  <li>
    <span class="news-date">{{ item.date | date: '%Y.%m.%d' }}</span>
    {{ item.body }}
  </li>
{%- endfor %}
</ul>

{%- if archived_count > 0 %}
<details class="news-archive">
  <summary><span>Earlier news</span></summary>
  <ul class="news-list">
  {%- for item in news offset: shown %}
    <li>
      <span class="news-date">{{ item.date | date: '%Y.%m.%d' }}</span>
      {{ item.body }}
    </li>
  {%- endfor %}
  </ul>
</details>
{%- endif %}

</div>
</div>
