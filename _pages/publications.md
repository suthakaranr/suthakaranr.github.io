---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}

1. **Ratnasingam, S.**, Ning, W. (2020) Confidence Distributions for Skew Normal Change-Point Model Based on Modified Information Criterion. *Journal of Statistical Theory and Practice* 14 (3), 1-21 ([DOI](https://doi.org/10.1007/s42519-020-00108-5))

Conference Papers
======
1. **Ratnasingam, S.**, Perera, K., Wikramanayake, N. (2014), Rainfall Intensity-Duration-Frequency Relationship for Colombo Region in Sri Lanka, *Proceedings of the SAITM Research Symposium on Engineering Advancements*, 101-104pp, 26th April, ISBN
978-955-0638-03-1. ([pdf](http://suthakaranr.github.io/files/paper1.pdf))
1. **Ratnasingam, S.**, Perera, K., Wikramanayake, N. (2014), Identify the Best Probability Distribution for Daily Maximum Rainfall in Colombo, Sri Lanka, *Proceedings of the International Conference on Mathematical Modeling*, Sri Lanka, 89-93pp, 14th
March, ISBN 978-955-046-054-0. ([pdf](http://suthakaranr.github.io/files/paper1.pdf))
