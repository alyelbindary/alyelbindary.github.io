---
layout: archive
title: "Publications"
permalink: /publications2/
author_profile: true
---

{% include citation-modal-scripts.html %}

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

{% for post in site.publications2 reversed %}
  {% include archive-single.html %}
{% endfor %}