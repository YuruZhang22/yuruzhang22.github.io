---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}

Journal Paper
======
Y. Zhang, Q. Liu, H. Wang, D. Chen, and K. Han, “CrowdSourcing Live High Definition Map via Collaborative Computation in Automotive Edge Computing”, IEEE Transactions on Vehicle Technology (TVT), Under Review



Conferences
======

Posters
======