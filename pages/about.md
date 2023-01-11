---
layout: page
title: About
permalink: /about/
weight: 3
---

# **About Me**

Hi I am **{{ site.author.name }}** :wave:,<br>
I am currently studying in Canada :canada:, at <a href="https://www.uqac.ca/" target="_blank">UQAC</a>, as part of a double-diploma agreement with my engineering school in France :fr:, the <a href="https://www.utbm.fr/" target="_blank">UTBM</a>. I'm doing a master's degree in professional computer science where I specialize in Data Science and Artificial Intelligence. 

By the way, as part of these two degrees that I am following, I am looking for a 6 months internship starting in August or September 2023. I don't have any specialization yet, I already worked on NLP, OCR, real-time classification, big data but I'm open to any project that could be a challenge 🦾! You can find my CV in French and in English in the <a href="https://clementdelteil.com/CV/" target="_blank">Resume</a> section of this website.

More personally, this site is both a portfolio and a personal site where I can share my pictures, my travels or articles on some AI and Data Science topics I like (coming soon). Traveling is an integral part of my personal life and my school curriculum, I spent 1 year in Slovenia with an internship and an exchange and now 1 year in Canada. And outside of that I have traveled to many countries: :fr: :slovenia: :canada: :it: :morocco: :hungary: :vietnam: :us: :reunion: :peru: :cambodia: :croatia: :gb: :es: :de: :czech_republic: :switzerland: :kr:

To conclude on my person, I live by the latin adage : "<em>Mens sana in corpore sano</em> ". I run 🏃🏻, read 📔, lift weights 🏋🏻 and sometime yes, I sit in front of my computer 👨🏻‍💻. These activities help me keep clear ideas for my projects and my life ! Feel free to browse through the site, I have shared photos and projects from my journey.


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
