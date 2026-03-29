---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

{% assign preprints    = site.publications | where: "pub_type", "preprint"      | sort: "date" | reverse %}
{% assign working      = site.publications | where: "pub_type", "working paper" | sort: "date" | reverse %}
{% assign articles     = site.publications | where: "pub_type", "journal"       | sort: "date" | reverse %}
{% assign chapters     = site.publications | where: "pub_type", "book chapter"  | sort: "date" | reverse %}
{% assign conferences  = site.publications | where: "pub_type", "conference"    | sort: "date" | reverse %}
{% assign other        = site.publications | where: "pub_type", "other"         | sort: "date" | reverse %}

{% if preprints.size > 0 %}
## Working Papers & Preprints
{% for post in preprints %}
  {% include publication-single.html %}
{% endfor %}
{% endif %}

{% if articles.size > 0 %}
## Journal Articles
{% for post in articles %}
  {% include publication-single.html %}
{% endfor %}
{% endif %}

{% if chapters.size > 0 %}
## Book Chapters
{% for post in chapters %}
  {% include publication-single.html %}
{% endfor %}
{% endif %}

{% if conferences.size > 0 %}
## Conference Presentations
{% for post in conferences %}
  {% include publication-single.html %}
{% endfor %}
{% endif %}

{% if other.size > 0 %}
## Other
{% for post in other %}
  {% include publication-single.html %}
{% endfor %}
{% endif %}

{% if preprints.size > 0 %}
## Preprints
{% for post in preprints %}{% include publication-single.html %}{% endfor %}
{% endif %}

{% if working.size > 0 %}
## Working Papers
{% for post in working %}{% include publication-single.html %}{% endfor %}
{% endif %}
