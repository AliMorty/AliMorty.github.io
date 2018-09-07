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
<br>
# a change YOU CAN SEE 
<br>
| Course Name                               | Score | GPA | Unit |
|-------------------------------------------|:-----:|:---:|:----:|
| Engineering Statistics                    |   20  |  4  |   3  |
| Stochastic Processes (I)                  |   20  |  4  |   3  |
| Data Storage & Retrieval                  |   20  |  4  |   3  |
| Foundations of Data Mining                |   19  |  4  |   3  |
| Principles of Database Design             |  18.4 |  4  |   3  |
| Artificial Intelligence                   |   20  |  4  |   3  |
| Data Struct. & Algorithms                 |   20  |  4  |   3  |
| Design of Algorithms                      |   20  |  4  |   3  |
| Topics in Computer Science (Algorithm II) |   20  |  4  |   3  |
| Theory of Machines & Languages            |   20  |  4  |   3  |
| Design of Programming Language            |   19  |  4  |   3  |
| Principles of Compiler Design             |  18.6 |  4  |   3  |
| Principles of Computer & Prog.            |   17  |  4  |   4  |
| Advanced Computer Programming             |  19.5 |  4  |   3  |
| Computer Laboratory                       |   20  |  4  |   1  |
| Discrete Structures                       |  17.5 |  4  |   3  |
| Math. (I)                                 |  19.5 |  4  |   3  |
| Math. (II)                                |   19  |  4  |   3  |
| Differential Equations                    |  19.8 |  4  |   3  |
| Engineering Mathematics                   |   20  |  4  |   3  |
| BCs Project                               |   20  |  4  |   3  |
| GPA in 20                                 | **19.33** |     |      |
| GPA                                       |   **4**   |     |      |


{% include My_Selected_Grades.html %}
<h2> More information About selected courses</h2>

{% for post in site.grades reversed %}
  {% include archive-single-grade.html %}
{% endfor %}
