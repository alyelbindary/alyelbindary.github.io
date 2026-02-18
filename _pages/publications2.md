layout: archive
title: "Publications"
permalink: /publications2/
author_profile: true
---

{% include base_path %}

{% for post in site.publications2 reversed %}
  {% include archive-single.html %}
{% endfor %}