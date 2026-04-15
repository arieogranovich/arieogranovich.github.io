---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

You can also find my articles on <u><a href="https://scholar.google.com/citations?user=jnYTz5IAAAAJ&hl=en&oi=ao">my Google Scholar profile</a>.</u>

A <sup>*</sup> next to the authors' names indicates a co-first-author publication.

{% assign preprint_pubs = site.publications | where: "category", "preprints" | sort: "date" | reverse %}
{% assign journal_pubs = site.publications | where: "category", "journals" | sort: "date" | reverse %}
{% assign conf_pubs = site.publications | where: "category", "conferences" | sort: "date" | reverse %}

Preprints and Publications Under Review
------
{% if preprint_pubs.size > 0 %}
{% for pub in preprint_pubs %}
* {{ pub.authors }}, "{{ pub.title }}", {{ pub.venue }}{% if pub.paperurl %}, [[URL]({{ pub.paperurl }})]{% endif %}

{% endfor %}
{% else %}
Nothing here yet!
{% endif %}

Journal Publications
------
{% if journal_pubs.size > 0 %}
{% for pub in journal_pubs %}
* {{ pub.authors }}, "{{ pub.title }}", {{ pub.venue }}{% if pub.paperurl %}, [[URL]({{ pub.paperurl }})]{% endif %}

{% endfor %}
{% else %}
Coming soon (on an academic timescale)!
{% endif %}

Conference Publications
------
{% if conf_pubs.size > 0 %}
{% for pub in conf_pubs %}
* {{ pub.authors }}, "{{ pub.title }}", {{ pub.status | append: " to the " }}{{ pub.venue }}{% if pub.paperurl %}, [[URL]({{ pub.paperurl }})]{% endif %}

{% endfor %}
{% endif %}
