---
lang: it
layout: issuelist_react
title: "Tutte le segnalazioni"
subtitle: Scopri tutte le segnalazioni fatte sulla piattaforma
permalink: /issues_react/
categorieMapAll: true
justLatestIssues: true
---

{% if page.issuecategories %}
{% assign issuecategories = page.issuecategories[page.lang] %}
{% else %}
{% assign issuecategories = site.data.cfg.issuecategories[page.lang] %}
{% endif %}

<div class="row mx-auto">
{% for category in issuecategories %}
  <div class="col-xs-12 col-sm-6 mb-15">
	  <a href="/{{category[0] | slugify}}" class="btn btn-success btn-block">{{category[0]}}</a>
	</div>
{% endfor %}
</div>


