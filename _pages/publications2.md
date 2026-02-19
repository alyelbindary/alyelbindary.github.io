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
  background-color: #fefefe;
  margin: 5% auto;
  padding: 20px;
  border: 1px solid #888;
  border-radius: 8px;
  width: 60%;
  max-width: 550px;
  position: relative;
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
  color: #000;
}

.citation-tabs {
  display: flex;
  gap: 10px;
  margin: 20px 0;
  border-bottom: 2px solid #ddd;
}

.citation-tab-button {
  background-color: transparent;
  border: none;
  padding: 10px 20px;
  cursor: pointer;
  font-size: 16px;
  border-bottom: 3px solid transparent;
  transition: all 0.3s;
}

.citation-tab-button:hover {
  background-color: #f0f0f0;
}

.citation-tab-button.active {
  border-bottom: 3px solid #007bff;
  font-weight: bold;
}

.citation-format-content {
  margin: 20px 0;
}

.citation-format-content pre {
  background-color: #f5f5f5;
  padding: 15px;
  border-radius: 5px;
  overflow-x: auto;
  border: 1px solid #ddd;
}

.citation-format-content code {
  font-family: 'Courier New', monospace;
  font-size: 14px;
  color: #000;
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

<script>
document.addEventListener('DOMContentLoaded', function() {
  console.log('DOM loaded, defining citation functions...');
  
  window.openCitationModal = function(id) {
    console.log('Opening modal for:', id);
    var modal = document.getElementById('citation-modal-' + id);
    console.log('Modal element:', modal);
    if (modal) {
      modal.style.display = 'block';
    } else {
      alert('Modal not found: citation-modal-' + id);
    }
  };

  window.closeCitationModal = function(id) {
    document.getElementById('citation-modal-' + id).style.display = 'none';
  };

  window.showCitationFormat = function(id, format) {
    var contents = document.querySelectorAll('#citation-modal-' + id + ' .citation-format-content');
    contents.forEach(function(content) {
      content.style.display = 'none';
    });
    
    var tabs = document.querySelectorAll('#citation-modal-' + id + ' .citation-tab-button');
    tabs.forEach(function(tab) {
      tab.classList.remove('active');
    });
    
    document.getElementById('citation-' + format + '-' + id).style.display = 'block';
    event.target.classList.add('active');
  };

  window.copyCitation = function(id, format) {
    var text = document.querySelector('#citation-' + format + '-' + id + ' code').textContent;
    navigator.clipboard.writeText(text).then(function() {
      var button = event.target;
      var originalText = button.textContent;
      button.textContent = 'Copied!';
      button.classList.add('copied');
      setTimeout(function() {
        button.textContent = originalText;
        button.classList.remove('copied');
      }, 2000);
    });
  };

  window.onclick = function(event) {
    if (event.target.classList.contains('citation-modal')) {
      event.target.style.display = 'none';
    }
  };
  
  console.log('Citation functions defined!');
});
</script>

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

{% for post in site.publications2 reversed %}
  {% include archive-single.html %}
{% endfor %}