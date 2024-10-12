---
layout: glossary
title: Glossar
permalink: /glossary
---

{% for row in site.data.glossary %}
| {{ row.term }} | {{ row.definition }} | {{ row.sessionname }} |
{% endfor %}
