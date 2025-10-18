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
  {%- for post in site.posts limit:3 -%}
    {%
      include card.html
      image=post.image
      title=post.title
      subtitle=post.date
      description=post.content
      style="full-width"
    %}
  {%- endfor -%}
{%- endif -%}