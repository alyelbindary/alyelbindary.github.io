---
layout: archive
title: "Publications"
permalink: /publications2/
author_profile: true
---

<style>
.citation-modal {
  display: none;
  position: fixed;
  z-index: 1000;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: rgba(0,0,0,0.4);
}

.citation-modal-content {
  background-color: #2a2a2a;
  margin: 5% auto;
  padding: 20px;
  border: 1px solid #555;
  border-radius: 8px;
  width: 60%;
  max-width: 550px;
  position: relative;
  color: #e0e0e0;
}

.citation-modal-content h2 {
  color: #ffffff;
  margin-top: 0;
}

.citation-close {
  color: #aaa;
  float: right;
  font-size: 28px;
  font-weight: bold;
  cursor: pointer;
  line-height: 20px;
}

.citation-close:hover,
.citation-close:focus {
  color: #fff;
}

.citation-tabs {
  display: flex;
  gap: 10px;
  margin: 20px 0;
  border-bottom: 2px solid #555;
}

.citation-tab-button {
  background-color: transparent;
  border: none;
  padding: 10px 20px;
  cursor: pointer;
  font-size: 16px;
  border-bottom: 3px solid transparent;
  transition: all 0.3s;
  color: #e0e0e0;
}

.citation-tab-button:hover {
  background-color: #3a3a3a;
}

.citation-tab-button.active {
  border-bottom: 3px solid #007bff;
  font-weight: bold;
  color: #ffffff;
}

.citation-format-content {
  margin: 20px 0;
}

.citation-format-content pre {
  background-color: #1e1e1e;
  padding: 15px;
  border-radius: 5px;
  overflow-x: auto;
  border: 1px solid #555;
}

.citation-format-content code {
  font-family: 'Courier New', monospace;
  font-size: 14px;
  color: #e0e0e0;
}

.copy-button {
  background-color: #007bff;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
  font-size: 14px;
  margin-top: 10px;
}

.copy-button:hover {
  background-color: #0056b3;
}

.copy-button.copied {
  background-color: #28a745;
}
</style>

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

{% for post in site.publications2 reversed %}
  {% include archive-single.html %}
{% endfor %}