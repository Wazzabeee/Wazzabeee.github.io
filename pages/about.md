---
layout: page
title: About
permalink: /about/
weight: 3
---

# **About Me**

Hi I am **{{ site.author.name }}** :wave:,<br>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.

<div class="row">
{% include about/skills.html title="Programming" source=site.data.programming-skills %}
{% include about/skills.html title="Data Science" source=site.data.data-skills %}
{% include about/skills.html title="Soft Skills" source=site.data.soft-skills %}
</div>

# **Working experience**
<div class="row">
{% include about/timeline.html source=site.data.work-timeline %}
</div>

# **Education**
<div class="row">
{% include about/timeline.html source=site.data.education-timeline %}
</div>

<h2 class="mb-3">Certifications</h2>
{% capture list_items %}
NVIDIA Accelerating End-to-End Data Science Workflows
NVIDIA Getting Started with Deep Learning
NVIDIA Accelerated Computing with CUDA Python 2020
Stanford University Machine Learning (Coursera)
Business Language Testing Service (BULATS) C2
Cisco Certified Network Associate (CCNA)
{% endcapture %}
{% include elements/list.html %}

More certifications and Badges can be viewed on my <a href="https://www.linkedin.com/in/clementdelteil/details/certifications/" target="_blank">LinkedIn</a> page.
