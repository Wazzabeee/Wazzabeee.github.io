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


