---
layout: page
permalink: /projects/
title: Projects
class: projects
---

{:.hidden}
# Projects


<div class="grid">
  {% for project in site.data.projects %}
    {% include project.html project=project %}
  {% endfor %}
</div>
