---
layout: page
title: About
permalink: /about/
weight: 3
---

# **About Me**

Hi I am **{{ site.author.name }}** :wave:,<br>
A passionate robotics engineer currently pursuing my Master of Science in Robotics at the University of Manchester. I hold a Bachelor's degree in Mechatronics from the Manipal Institute of Technology, where I developed a strong foundation in both electronics and mechanical systems, preparing me for a career at the intersection of technology and engineering.

<a href="https://github.com/akshattnj" target="_blank" 
       style="display: inline-block; padding: 10px 20px; font-size: 16px; cursor: pointer; text-align: center; text-decoration: none; color: #dddddd; border: 2px solid #dddddd; border-radius: 5px; background-color: transparent; margin-right: 10px;">
       GitHub
    </a>
    <a href="https://www.linkedin.com/in/akshattnj" target="_blank" 
       style="display: inline-block; padding: 10px 20px; font-size: 16px; cursor: pointer; text-align: center; text-decoration: none; color: #0077b5; border: 2px solid #0077b5; border-radius: 5px; background-color: transparent;">
       LinkedIn
    </a>

<div class="row">
{% include about/skills.html title="Programming Skills" source=site.data.programming-skills %}
{% include about/skills.html title="Other Skills" source=site.data.other-skills %}
</div>

<div class="row">
{% include about/timeline.html %}
</div>