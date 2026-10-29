---
layout: academic
permalink: /
title: "Jiayi Jane Chen"
description: "Jiayi Jane Chen is a Ph.D. candidate in Computer Science at UT Austin who builds system abstractions and frameworks that use AI to efficiently approximate optimal behavior in real-world networked systems and operating systems."
redirect_from:
  - /research/
  - /about/
  - /about.html
---

<section class="bio">
<p>I am a final-year Ph.D. candidate in Computer Science at The University of Texas at Austin, advised by <a href="https://www.cs.utexas.edu/~akella/">Aditya Akella</a> and <a href="https://sites.google.com/view/sanjay-shakkottai/">Sanjay Shakkottai</a>. I build <strong>system abstractions, frameworks, and generalizable AI components, grounded in theoretical analysis</strong>, that let real-world systems efficiently approximate optimal behavior as workloads, environments, and objectives change.</p>
<p>My work spans networking, operating systems, and machine learning. I was part of the founding proposal team for the <a href="https://ldos.utexas.edu">NSF Expedition on Learning-Directed Operating Systems (LDOS)</a>, where I now lead the undergraduate research program. Before UT, I received my B.S. in Electrical and Computer Engineering from Shanghai Jiao Tong University. I have also spent time at Microsoft Research, Google, and Intel.</p>
</section>

<div class="callout"><strong>I am on the 2026&ndash;27 academic job market</strong> for tenure-track faculty positions in computer systems and networking. My application materials: <a href="{{ '/files/Jiayi_Chen_CV.pdf' | relative_url }}">CV</a> &middot; <a href="{{ '/files/Jiayi_Chen_Research_Statement.pdf' | relative_url }}">Research Statement</a> &middot; <a href="{{ '/files/Jiayi_Chen_Teaching_Statement.pdf' | relative_url }}">Teaching Statement</a></div>

<h2>Research</h2>
<p class="thesis">Latent information should be a first-class object in system design.</p>
<p>Today's systems expose isolated measurements, delayed feedback, and the effects of only the deployed policy. The information that matters most for good decisions stays hidden. My research recovers this latent structure with lightweight AI, exposes it through reusable system interfaces, and uses theory to characterize what it can and cannot buy.</p>

<div class="grid-3">
<div class="card">
<div class="card-num">Thrust 1</div>
<h3>Representing latent workload and system dynamics</h3>
<p>Build compact learned representations that recover workload and system state that raw measurements hide.</p>
<div class="tags"><a class="tag" href="{{ '/publications/#unum' | relative_url }}">UNUM</a><span class="tag tag-more">More to come</span></div>
</div>
<div class="card">
<div class="card-num">Thrust 2</div>
<h3>Guiding policy search with system knowledge</h3>
<p>Exploit system knowledge to guide near-optimal policy search with smaller search space.</p>
<div class="tags"><a class="tag" href="{{ '/publications/#darwin' | relative_url }}">Darwin</a><span class="tag tag-more">More to come</span></div>
</div>
<div class="card">
<div class="card-num">Thrust 3</div>
<h3>Characterizing limits and safeguarding</h3>
<p>Theory for when extra information helps, and runtime guardrails that keep learned policies safe.</p>
<div class="tags"><a class="tag" href="{{ '/publications/#batching' | relative_url }}">Online Batching</a><a class="tag" href="{{ '/publications/#guardrails' | relative_url }}">Guardrails</a></div>
</div>
</div>
<p style="margin-top:14px"><a class="section-link" href="{{ '/files/Jiayi_Chen_Research_Statement.pdf' | relative_url }}">Read my research statement &rarr;</a></p>

<h2>Recent News</h2>
<ul class="news">
{% for n in site.data.news limit: 6 %}<li><span class="date">{{ n.date }}</span><span>{{ n.text }}</span></li>
{% endfor %}</ul>
{% if site.data.news.size > 6 %}
<details class="more"><summary>Show earlier news</summary>
<ul class="news">
{% for n in site.data.news offset: 6 %}<li><span class="date">{{ n.date }}</span><span>{{ n.text }}</span></li>
{% endfor %}</ul>
</details>
{% endif %}

<h2>Selected Publications</h2>
<ul class="pubs">
{% for p in site.data.publications %}{% if p.selected %}{% include pub.html pub=p %}{% endif %}{% endfor %}
</ul>
<p style="margin-top:14px"><a class="section-link" href="{{ '/publications/' | relative_url }}">All publications &rarr;</a></p>
