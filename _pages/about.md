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

The Mobility and Machine Intelligence Lab (M&sup2; Lab) at Stony Brook University brings together game theory and data-driven optimization to develop **next-generation modeling and computational tools** for mobility and logistics systems, with a focus on connectivity, electrification, and automation. See [Research](/research/) for details.

We are recruiting **fully funded PhD students** beginning Spring/Fall 2027, as well as motivated MS and BS students. See [Openings](/openings/) for details.

</div>
</div>
</div>

<div class="page-section page-section--band">
<div class="wrap">
<h2 class="page-title">News</h2>

{%- comment -%}
  Items from the last 18 months are shown; anything older collapses into the
  "Earlier news" disclosure. 18 months = 47,347,200 seconds. The window is
  evaluated against site.time, so it advances on each rebuild.
{%- endcomment -%}
{%- assign cutoff = site.time | date: '%s' | plus: 0 | minus: 47347200 -%}
{%- assign news = site.data.news | sort: 'date' | reverse -%}

{%- assign archived_count = 0 -%}
{%- for item in news -%}
  {%- assign ts = item.date | date: '%s' | plus: 0 -%}
  {%- if ts < cutoff -%}{%- assign archived_count = archived_count | plus: 1 -%}{%- endif -%}
{%- endfor -%}

<ul class="news-list">
{%- for item in news -%}
  {%- assign ts = item.date | date: '%s' | plus: 0 -%}
  {%- if ts >= cutoff %}
  <li>
    <span class="news-date">{{ item.date | date: '%Y.%m.%d' }}</span>
    {{ item.body }}
  </li>
  {%- endif -%}
{%- endfor %}
</ul>

{%- if archived_count > 0 %}
<details class="news-archive">
  <summary><span>Earlier news</span><span class="news-archive__count">{{ archived_count }}</span></summary>
  <ul class="news-list">
  {%- for item in news -%}
    {%- assign ts = item.date | date: '%s' | plus: 0 -%}
    {%- if ts < cutoff %}
    <li>
      <span class="news-date">{{ item.date | date: '%Y.%m.%d' }}</span>
      {{ item.body }}
    </li>
    {%- endif -%}
  {%- endfor %}
  </ul>
</details>
{%- endif %}

</div>
</div>
