---
layout: page
title: About
permalink: /about/
weight: 3
---

# **About Me**

Hi I am **{{ site.author.name }}** :wave:,<br>

I recently finished my end-of-study internship at <a href="https://namr.com/" target="_blank">namR</a> as a Data Scientist where I engineered a methodology to filter noisy labels from training sets, resulting in the improvement of data quality and model performance 📈. I've also developed a meta-model (LightGBM + KNN) to predict the use type of France's 34 million buildings 🏙️ from extremely unbalanced spatial data.

**I'm now working as a Machine Learning Engineeer at <a href="https://wiremind.io/" target="_blank">Wiremind</a> where I'm developing and deploying machine learning models to optimize airline revenues.**

I hold a Canadian :canada: M.Sc in Artificial Intelligence from the <a href="https://www.uqac.ca/" target="_blank">UQAC</a> as well as a French :fr: Computer Science Engineering Degree with a focus on Data Science and Artificial Intelligence from the <a href="https://www.utbm.fr/" target="_blank">UTBM</a>.

You can find my CV in French and in English in the <a href="https://clementdelteil.com/CV/" target="_blank">Resume</a> section of this website.

More personally, this site is both a portfolio and a personal site where I can share my <a href="https://clementdelteil.com/photography/" target="_blank">pictures</a>, my <a href="https://clementdelteil.com/reading/" target="_blank">readings</a> or <a href="https://clementdelteil.com/blog/" target="_blank">articles</a> on some AI and Data Science topics I like. Traveling is an integral part of my personal life and my school curriculum, I spent 1 year in Slovenia with an internship and an exchange semester and now 1 year in Canada. Outside of that I had the chance to travel to many countries: :fr: :slovenia: :canada: :it: :morocco: :hungary: :vietnam: :us: :reunion: :peru: :cambodia: :croatia: :gb: :es: :de: :czech_republic: :switzerland: :kr: :cuba: ...

To conclude on my person, I live by the latin adage : "<em>Mens sana in corpore sano</em> ". I run 🏃🏻, read 📔, lift weights 🏋🏻 and sometimes yes, I sit in front of my computer 👨🏻‍💻. These activities help me keep clear ideas for my projects and my life ! Feel free to browse through the site, I have shared photos and projects from my journey.


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

More certifications and Badges are available on my <a href="https://www.linkedin.com/in/clementdelteil/details/certifications/" target="_blank">LinkedIn</a> page.
