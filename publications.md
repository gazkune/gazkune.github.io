---
layout: page
title: Publications
label: Research output
description: Selected recent publications. For the complete and most up-to-date list, see Google Scholar.
permalink: /publications/
---
<div class="external-callout"><span>Complete publication list</span><a href="https://scholar.google.es/citations?user=_1wx6NoAAAAJ&hl=en&oi=ao">Google Scholar ↗</a></div>
{% assign years = site.data.publications | map: 'year' | uniq | sort | reverse %}{% for year in years %}<h2 class="year-heading">{{ year }}</h2><div class="publication-list full-list">{% for pub in site.data.publications %}{% if pub.year == year %}<article class="publication"><div class="pub-year">{{ pub.year }}</div><div><h3>{% if pub.url %}<a href="{{ pub.url }}">{{ pub.title }}</a>{% else %}{{ pub.title }}{% endif %}</h3><p>{{ pub.authors }}</p><p class="venue">{{ pub.venue }}</p></div></article>{% endif %}{% endfor %}</div>{% endfor %}
