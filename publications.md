---
layout: default
title: "Publications"
description: "Journal articles and conference proceedings by Sabita Karki on AI, digital marketing, consumer behavior, airline booking, and service quality."
permalink: /publications/
---

# Publications

## Journal Articles

{% assign journals = site.data.publications | where: "type", "journal" %}
{% for item in journals %}<article class="publication"><p class="meta">{{ item.year }}</p><h3>{% if item.url %}<a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">{{ item.title }}</a>{% else %}{{ item.title }}{% endif %}</h3><p>{{ item.authors }}</p><p><em>{{ item.venue }}</em></p></article>{% endfor %}

## Conference Proceedings

{% assign conferences = site.data.publications | where: "type", "conference" %}
{% for item in conferences %}<article class="publication"><p class="meta">{{ item.year | default: "Conference proceeding" }}</p><h3>{{ item.title }}</h3><p>{{ item.authors }}</p><p><em>{{ item.venue }}</em></p></article>{% endfor %}
