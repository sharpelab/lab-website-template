---
---

# Welcome to the Sharpe Lab!

Hello and welcome. The website is still under construction, but a few of the sections are complete. Please feel to reach out if you are excited about the work we do!

{%
  include button.html
  link="contact"
  text="Join Us!"
  icon="fa-solid fa-users"
  style="filled"
%}

{% include section.html %}

## Highlights

{%- if site.posts and site.posts.size > 0 -%}
  <div class="cards">
    {%- for post in site.posts limit:3 -%}
      <article class="card">
        {%- if post.image -%}
          <a class="card-media" href="{{ post.url | relative_url }}">
            <img src="{{ post.image | relative_url }}" alt="{{ post.title | escape }}">
          </a>
        {%- endif -%}

        <div class="card-text">
          <h3 class="card-title">
            <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
          </h3>

          {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
          <p class="card-subtitle">{{ post.date | date: date_format }}</p>

          {%- assign blurb = post.excerpt | strip_html | strip_newlines | truncate: 180 -%}
          <p class="card-excerpt">{{ blurb }}</p>

          <a class="card-cta" href="{{ post.url | relative_url }}">Read more →</a>
        </div>
      </article>
    {%- endfor -%}
  </div>
{%- endif -%}