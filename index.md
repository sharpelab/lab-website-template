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
    {% include post-excerpt.html post=post %}
    
    {%
      include button.html
      link=post.url
      text="Read more"
      icon="fa-solid fa-arrow-right"
      flip=true
      style="bare"
    %}
  {% endcapture %}

  {%
    include feature.html
    image=post.image
    link=post.url
    title=post.title
    text=text
    flip=forloop.index0
  %}
{% endfor %}
