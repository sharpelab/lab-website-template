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

{% assign reversed_posts = site.posts | reverse %}

{% for post in reversed_posts limit: 3 %}
  {% capture text %}
    {{ post.content }}
  {% endcapture %}

  {%
    include feature.html
    title=post.title
    text=text
  %}
{% endfor %}
