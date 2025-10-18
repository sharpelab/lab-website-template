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
          <div class="card-media">
            <img src="{{ post.image | relative_url }}" alt="{{ post.title | escape }}">
          </div>
        {%- endif -%}

        <div class="card-text">
          <h3 class="card-title">{{ post.title | escape }}</h3>

          {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
          <p class="card-subtitle">{{ post.date | date: date_format }}</p>

          <div class="card-excerpt">
            {{ post.content }}
          </div>
        </div>
      </article>
    {%- endfor -%}
  </div>
{%- endif -%}