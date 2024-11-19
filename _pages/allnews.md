---
title: "News"
layout: textlay
excerpt: "Geertsema Lab at Delft University of Technology."
sitemap: false
permalink: /allnews.html
---

<!-- markdownlint-disable MD025 -->
# News
<!-- markdownlint-enable MD025 -->

{% for article in site.data.news %}
<p><b>{{ article.date }}</b> <br> {{ article.headline }}</p>
{% endfor %}
