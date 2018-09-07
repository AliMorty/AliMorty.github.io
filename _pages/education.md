---
layout: talk
title: "Education"
permalink: /education/
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
|                                                        | 
|--------------------------------------------------------| 
| Course name,Score,GPA,Units,GPA*Units,Score*Units      | 
| Engineering Statistics,20,4,3,12,60                    | 
| Stochastic Processes (I),20,4,3,12,60                  | 
| Data Storage & Retrieval,20,4,3,12,60                  | 
| Foundations of Data Mining,19,4,3,12,57                | 
| Principles of Database Design,18.4,4,3,12,55.2         | 
| Artificial Intelligence,20,4,3,12,60                   | 
| Data Struct. & Algorithms,20,4,3,12,60                 | 
| Design of Algorithms,20,4,3,12,60                      | 
| Topics in Computer Science (Algorithm II),20,4,3,12,60 | 
| Theory of Machines & Languages,20,4,3,12,60            | 
| Design of Programming Language,19,4,3,12,57            | 
| Principles of Compiler Design,18.6,4,3,12,55.8         | 
| Principles of Computer & Prog. ,17,4,4,16,68           | 
| Advanced Computer Programming ,19.5,4,3,12,58.5        | 
| Computer Laboratory,20,4,1,4,20                        | 
| Discrete Structures  ,17.5,4,3,12,52.5                 | 
| Math. (I),19.5,4,3,12,58.5                             | 
| Math. (II),19,4,3,12,57                                | 
| Differential Equations,19.8,4,3,12,59.4                | 
| Engineering Mathematics,20,4,3,12,60                   | 
| BCs Project,20,4,3,12,60                               | 
| SUM,407.3,84,62,248,1198.9                             | 
| GPA,19.33709677,,,,                                    | 
| GPA in 20,4,,,,                                        | 


{% include My_Selected_Grades.html %}
<h2> More information About selected courses</h2>

{% for post in site.grades reversed %}
  {% include archive-single-grade.html %}
{% endfor %}
