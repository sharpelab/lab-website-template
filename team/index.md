---
title: Team
nav:
  order: 3
  tooltip: About our team
---

# Team

{% include section.html %}

{% include list.html data="members" component="portrait-nolink" filter="role == 'pi'" %}
{% include list.html data="members" component="portrait-nolink" filter="role == 'postdoc'" %}
{% include list.html data="members" component="portrait-nolink" filter="role == 'grad'" %}
{% include list.html data="members" component="portrait-nolink" filter="role == 'undergrad'" %}

