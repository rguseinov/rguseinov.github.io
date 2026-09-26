---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

{% assign articles    = site.publications | where: "pub_type", "journal"       | sort: "date" | reverse %}
{% assign chapters    = site.publications | where: "pub_type", "book chapter"  | sort: "date" | reverse %}
{% assign review      = site.publications | where: "pub_type", "under review"  | sort: "date" | reverse %}
{% assign working     = site.publications | where: "pub_type", "working paper" | sort: "date" | reverse %}
{% assign progress    = site.publications | where: "pub_type", "in progress"   | sort: "date" | reverse %}

{% if articles.size > 0 %}
## Peer-reviewed Articles
{% for post in articles %}{% include publication-single.html %}{% endfor %}
{% endif %}

{% if chapters.size > 0 %}
## Book Chapters
{% for post in chapters %}{% include publication-single.html %}{% endfor %}
{% endif %}

{% if review.size > 0 %}
## Manuscripts Under Review
{% for post in review %}{% include publication-single.html %}{% endfor %}
{% endif %}

{% if working.size > 0 %}
## Working Papers
{% for post in working %}{% include publication-single.html %}{% endfor %}
{% endif %}

{% if progress.size > 0 %}
## Work in Progress
{% for post in progress %}{% include publication-single.html %}{% endfor %}
{% endif %}
