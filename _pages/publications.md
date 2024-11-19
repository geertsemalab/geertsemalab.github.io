---
title: "Geertsema Lab - Publications"
layout: gridlay
excerpt: "Geertsema Lab -- Publications."
sitemap: false
permalink: /publications/
---

<!-- markdownlint-disable MD025 -->
# Publications
<!-- markdownlint-enable MD025 -->

## Group highlights

**At the end of this page, you can find the [full list of publications](#full-list-of-publications). New papers will be avialable on [bioRxiv](https://www.biorxiv.org/search/author1%3AHylkje%2BGeertsema%20jcode%3Abiorxiv%20numresults%3A25%20sort%3Arelevance-rank%20format_result%3Astandard).**

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" alt="Cover image for {{ publi.title }}"/>
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>

## Full List of publications

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
