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

{%- if site.posts.size > 0 -%}
  <ul class="post-list">
    {%- assign reversed_posts = site.posts | reverse -%}
    {%- for post in reversed_posts limit: 3 -%}
    <li class="post-item">
      <h3>{{ post.title | escape }}</h3>
      {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
      <span class="post-meta">{{ post.date | date: date_format }}</span>
      {{ post.content }}
    </li>
    {%- endfor -%}
  </ul>
{%- endif -%}
