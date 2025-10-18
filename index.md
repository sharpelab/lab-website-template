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
  {%- assign reversed_posts = site.posts | reverse -%}
  <div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 20px;">
    {%- for post in reversed_posts limit: 3 -%}
      <div class="card">
        <div class="card-text">
          <h3 class="card-title">{{ post.title | escape }}</h3>
          {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
          <p class="card-subtitle">{{ post.date | date: date_format }}</p>
          <div class="post-content">
            {{ post.content }}
          </div>
        </div>
      </div>
    {%- endfor -%}
  </div>
{%- endif -%}
