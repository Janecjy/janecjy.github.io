---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a fifth-year Ph.D. student in Computer Science at The University of Texas at Austin, where I am co-advised by Prof. [Aditya Akella](https://www.cs.utexas.edu/~akella/) and Prof. [Sanjay Shakkottai](https://sites.google.com/view/sanjay-shakkottai/). Prior to that, I earned my bachelor degree in Electrical and Computer Engineering from Shanghai Jiao Tong University.

My research lies at the intersection of machine learning, networks, and systems, with a focus on applying learning-based techniques to improve the performance of networked systems. Rather than applying machine learning as a standalone optimization tool, my works are **structuring how AI can be used within systems** by designing abstractions, frameworks, and reusable components that enable learning-based techniques to be systematically integrated into system design and operation.
I am proud to be part of the [Learning-Directed Operating System (LDOS)](https://ldos.utexas.edu) expedition.

Thank you for visiting, and I hope you find my work as exciting as I do!

Selected Publications
======

**UNUM: A New Framework for Network Control** \[[paper](/files/unum_appendix_fixed.pdf)\]

<ins>Jiayi Chen</ins>, Nihal Sharma, Debajit Chakraborty, Saurabh Agarwal, Jeffrey Zhou, Aditya Akella, Sanjay Shakkottai\
*NSDI '26*

A system's ability to understand its current operating context is crucial for making good decisions. Yet most network controllers today rely on hand-crafted features that provide only a narrow view of the system and are often delayed by at least one RTT. Inspired by the separation principle in control theory, we argue that state estimation should be treated as a standalone, first-class entity. Unum provides a unified network-state embedder that learns a rich latent representation of system conditions. This shared representation can be used by many different controllers, decoupling the challenge of understanding the system from the task of making decisions. By offering a common and more expressive view of the network, UNUM enables controllers to make better and more coordinated decisions.

---

**Darwin: Flexible Learning-based CDN Caching** \[[paper](https://dl.acm.org/doi/10.1145/3603269.3604863)\] \[[talk](https://www.youtube.com/watch?v=kpjjopd9vQQ&list=PLU4C2_kotFP2JAkoL6pcgbb52f6GIJJd7&index=55)\]

<ins>Jiayi Chen</ins>, Nihal Sharma, Tarannum Khan, Shu Liu, Brian Chang, Aditya Akella, Sanjay Shakkottai, Ramesh K Sitaraman\
*ACM SIGCOMM '23*

Most production CDNs apply static, hand-tuned caching policy parameters at cache servers, such as admission frequency or size thresholds for the Hot Object Caches (HOC) of their system. However, these static policies fall short when a server is faced with unpredictable traffic pattern changes, even when policies employ multiple control parameters/knobs. Recent approaches have proposed learning-based solutions to dynamically adjust policy parameters, but they are limited in action space, caching objectives, or impose high overhead. We propose Darwin, a CDN cache management system that is robust to traffic pattern changes and can flexibly optimize different caching objectives with unrestricted action spaces. Darwin employs a three-stage pipeline involving traffic pattern feature collection, unsupervised clustering for classification, and neural bandit expert selection to choose the optimal caching policy. Through extensive simulations, experiments using an Apache Traffic Server (ATS)-based prototype, and theoretical analysis, we show that Darwin achieves significant performance gain w.r.t. different objectives such as maximizing object hit rates and minimizing disk writes, while simultaneously adapting to traffic pattern shifts. Darwin imposes negligible overhead and achieves high throughput compared to the state-of-the-art.

---

**How I learned to stop worrying and love learned OS policies** \[[paper](https://dl.acm.org/doi/abs/10.1145/3713082.3730384)\]

Divyanshu Saxena\*, <ins>Jiayi Chen\*</ins>, Sujay Yadalam, Yeonju Ro, Rohit Dwivedula, Eric H Campbell, Aditya Akella, Christopher J Rossbach, Michael Swift\
*HotOS '25*

While machine learning has been adopted across various fields, its ability to outperform traditional heuristics in operating systems is often met with justified skepticism. Concerns about unsafe decisions, opaque debugging processes, and the challenges of integrating ML into the kernel---given its stringent latency constraints and inherent complexity---make practitioners understandably cautious. This paper introduces Guardrails for the OS, a framework that allows kernel developers to declaratively specify system-level properties and define corrective actions to address property violations. The framework facilitates the compilation of these guardrails into monitors capable of running within the kernel. In this work, we establish the foundation for Guardrails, detailing its core abstractions, examining the problem space, and exploring potential solutions.