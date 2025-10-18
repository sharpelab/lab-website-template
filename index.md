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

<!-- posts start -->

{%- if site.posts and site.posts.size > 0 -%}
  {%- for post in site.posts limit:3 -%}
    <div class="post-highlight">
      <h3>{{ post.title | escape }}</h3>
      {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
      <p class="post-date">{{ post.date | date: date_format }}</p>
      <div class="post-content">
        {{ post.content }}
      </div>
    </div>
    {%- unless forloop.last -%}
      <hr class="post-separator">
    {%- endunless -%}
  {%- endfor -%}
{%- endif -%}

{% include section.html %}