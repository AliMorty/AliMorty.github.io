---
layout: talk
title: "Education"
permalink: /grades/
author_profile: true
---

<blockquote>
  <p><strong>BSc in Computer Engineering</strong> <br>
  AmirKabir University of Technology (Tehran Polytechnic)</p>
  
  <ul>
  <li>CGPA:   Overall         18.47 / 20   </li>
  
  <li>Selected courses   19.33 / 20 <br></li>
  </ul>
</blockquote>

## A test here

<h2> All Grades</h2>
<a href="https://github.com/AliMorty/AliMorty.github.io/blob/master/files/Mortazavi_All_Grades.pdf">Download All_Grades.pdf</a>
<h2> Selected Grades</h2>
{% include My_Selected_Grades.html %}
<h2> More information About selected courses</h2>

{% for post in site.grades reversed %}
  {% include archive-single-grade.html %}
{% endfor %}