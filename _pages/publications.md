---
title: "MarkoLab - Publications"
layout: gridlay
excerpt: "MarkoLab -- Publications."
sitemap: false
permalink: /publications/
---


## Group highlights

(For a full list of publications and patents see [below](#full-list-of-publications) or go to [Google Scholar](https://scholar.google.com/citations?user=vx6__-sAAAAJ&hl=en)

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
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
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

{% for publi in site.data.publist_past %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}


## Patents

<em>TJ Gardner, W Liberti, J Markowitz, G Guitchounts</em><br /> Minimally invasive splaying microfiber electrode array and methods of fabricating and implanting the same <br /> <a href="https://patentimages.storage.googleapis.com/e4/ba/df/b6ec32fa8dc8a9/US20170007824A1.pdf">App Number 14902734 (2017)</a>
