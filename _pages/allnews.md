---
title: "News"
layout: textlay
excerpt: "MarkoLab at Georgia Tech and Emory."
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news limit %}
{{ article.date }}
{{ article.headline | markdownify }}
{% endfor %}

