---
title: "Geertsema Lab - Team"
layout: gridlay
excerpt: "Geertsema Lab: Team members"
sitemap: false
permalink: /team/
---

<!-- markdownlint-disable MD025 -->
# Group Members
<!-- markdownlint-enable MD025 -->

**We are always looking for enthousiastic Master and Bachelor students to join the team** [(see student projects)](/join_the_lab)**!**

<!-- **We are  looking for new PhD students, Postdocs, and Master students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/vacancies) **!** -->

Would you like to send an e-mail to someone? Then please add ‘tudelft.nl’ to their email name.

Jump to [staff](#staff), [master and bachelor students](#master-and-bachelor-students), and [alumni](#alumni).

## Staff

{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}
<div class="col-sm-6 clearfix">
<img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="30%" style="float: left" alt="{{ member.name }}'s photo"/>
<h4>{{ member.name }}</h4>
<b>{{ member.role }}</b><br><i>Office: {{ member.office }}<br>{% if member.email %}Email: {{ member.email }}<br>{% endif %}</i>{% if member.research %}Research: {{ member.research }}{% endif %}
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## Master and Bachelor Students

{% assign number_printed = 0 %}
{% for member in site.data.students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}
<div class="col-sm-6 clearfix">
<img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="30%" style="float: left" alt="{{ member.name }}'s photo"/>
<h4>{{ member.name }}</h4>
<b>{{ member.role }}</b><br><i>Office: {{ member.office }}<br>{% if member.email %}Email: {{ member.email }}<br>{% endif %}</i>{% if member.research %}Research: {{ member.research }}{% endif %}
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## Alumni

<!-- TODO: Uncomment this once a graduate student or postdoc finishes

### Former graduate students and postdocs

{% for member in site.data.alumni_members %}

<div class="row-alumni">
<div class="col-sm-1 clearfix">
{% if member.year %}
{{ member.year }}
{% else %}
&nbsp;  <!-- Non-breaking space for consistency in layout - ->
{% endif %}
</div>

<div class="col-sm-3 clearfix">
{% if member.name %}
{{ member.name }}
{% else %}
&nbsp;  <!-- Non-breaking space for consistency in layout - ->
{% endif %}
</div>

<div class="col-sm-8 clearfix">
{% if member.role %}
{{ member.role }}
{% else %}
&nbsp;  <!-- Non-breaking space for consistency in layout - ->
{% endif %}
</div>
</div>

{% endfor %}

-->

### Former MSc students

{% for member in site.data.alumni_msc %}

<div class="row-alumni">
<div class="col-sm-1 clearfix">
{% if member.year %}
{{ member.year }}
{% else %}
&nbsp;  <!-- Non-breaking space for consistency in layout -->
{% endif %}
</div>

<div class="col-sm-3 clearfix">
{% if member.name %}
{{ member.name }}
{% else %}
&nbsp;  <!-- Non-breaking space for consistency in layout -->
{% endif %}
</div>

<div class="col-sm-8 clearfix">
{% if member.role %}
{{ member.role }}
{% else %}
&nbsp;  <!-- Non-breaking space for consistency in layout -->
{% endif %}
</div>
</div>

{% endfor %}

### Former BSc students

{% for member in site.data.alumni_bsc %}

<div class="row-alumni">
<div class="col-sm-1 clearfix">
{% if member.year %}
{{ member.year }}
{% else %}
&nbsp;  <!-- Non-breaking space for consistency in layout -->
{% endif %}
</div>

<div class="col-sm-3 clearfix">
{% if member.name %}
{{ member.name }}
{% else %}
&nbsp;  <!-- Non-breaking space for consistency in layout -->
{% endif %}
</div>

<div class="col-sm-8 clearfix">
{% if member.role %}
{{ member.role }}
{% else %}
&nbsp;  <!-- Non-breaking space for consistency in layout -->
{% endif %}
</div>
</div>

{% endfor %}

<!-- ## Administrative Support

<a href="h.vanlookerencampagne@tudelft.nl">Hannah Van Lookeren Campagne</a> is helping us (and other groups) with administration. -->
