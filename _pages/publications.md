---
layout: academic
title: "Publications"
permalink: /publications/
heading: "Publications"
description: "Publications of Jiayi Jane Chen at SIGCOMM, NSDI, SIGMETRICS, HotOS, and NeurIPS and ICML workshops."
redirect_from:
  - /publication/
---

<p class="lede muted"> See also <a href="{{ site.author.googlescholar }}">Google Scholar</a> for the full list.</p>

{% assign sections = "conference|Conference Papers;workshop|Workshop Papers;review|Under Review;preprint|Preprints" | split: ";" %}
{% for s in sections %}
{% assign parts = s | split: "|" %}
{% assign items = site.data.publications | where: "type", parts[0] %}
{% if items.size > 0 %}
<h2>{{ parts[1] }}</h2>
<ul class="pubs">
{% for p in items %}{% include pub.html pub=p %}{% endfor %}
</ul>
{% endif %}
{% endfor %}
