---
layout: post
title: "Assignment 2"
subtitle: "Drug related crimes in San Francisco"
date: 2023-03-21 12:30:00 +0100
author: Vivian Váradi, Thomas Adamopoulos & Søren Blatt Bendtsen
background: '/img/my_images/golden_gate_bridge.jpg'
---

---
layout: default
title: My Table
---

|              My Table                |
|-------------------------------------|
| Column 1 | Column 2 | Column 3 | Column 4 |
|----------|----------|----------|----------|
| Row 1, Column 1 | Row 1, Column 2 | Row 1, Column 3 | Row 1, Column 4 |
| Row 2, Column 1 | Row 2, Column 2 | Row 2, Column 3 | Row 2, Column 4 |
| Row 3, Column 1 | Row 3, Column 2 | Row 3, Column 3 | Row 3, Column 4 |
| Row 4, Column 1 | Row 4, Column 2 | Row 4, Column 3 | Row 4, Column 4 |
| Row 5, Column 1 | Row 5, Column 2 | Row 5, Column 3 | Row 5, Column 4 |
| Row 6, Column 1 | Row 6, Column 2 | Row 6, Column 3 | Row 6, Column 4 |
| Row 7, Column 1 | Row 7, Column 2 | Row 7, Column 3 | Row 7, Column 4 |
| Row 8, Column 1 | Row 8, Column 2 | Row 8, Column 3 | Row 8, Column 4 |
| Row 9, Column 1 | Row 9, Column 2 | Row 9, Column 3 | Row 9, Column 4 |

---
layout: default
title: My Table
---

# My Table

Table Title

| Column 1 | Column 2 | Column 3 | Column 4 |
|----------|----------|----------|----------|
| Row 1, Column 1 | Row 1, Column 2 | Row 1, Column 3 | Row 1, Column 4 |
| Row 2, Column 1 | Row 2, Column 2 | Row 2, Column 3 | Row 2, Column 4 |
| Row 3, Column 1 | Row 3, Column 2 | Row 3, Column 3 | Row 3, Column 4 |
| Row 4, Column 1 | Row 4, Column 2 | Row 4, Column 3 | Row 4, Column 4 |
| Row 5, Column 1 | Row 5, Column 2 | Row 5, Column 3 | Row 5, Column 4 |
| Row 6, Column 1 | Row 6, Column 2 | Row 6, Column 3 | Row 6, Column 4 |
| Row 7, Column 1 | Row 7, Column 2 | Row 7, Column 3 | Row 7, Column 4 |
| Row 8, Column 1 | Row 8, Column 2 | Row 8, Column 3 | Row 8, Column 4 |
| Row 9, Column 1 | Row 9, Column 2 | Row 9, Column 3 | Row 9, Column 4 |





<style>
table {
    border-collapse: collapse;
}
table td, table th {
    border: 1px solid black;
    padding: 5px;
}
table th {
    background-color: #f2f2f2;
}
</style>





Calendar Plot:

![Calendar plot](/viz/cal_plot_assignment2.png){: width="800" }

One observation about the calendar plot is that after 2010 drug crimes begin to decrease noticeably. So what's going on and has drug crime gone down in San Fransisco? 
The first part of the comprehensive health care reform law also known as Obamacare enacted on March 23, 2010, is the answer !! [1]

Obamacare does not specifically directly address substances. But, it does include provisions for mental health care, prescription medications, and substance use disorders.
The Obamacare forbids insurers from refusing coverage or raising premiums based on pre-existing diseases, including substance use disorders, and mandates coverage for mental health and substance use disorder therapies. [2]


According to Bronson et al. (2017)[3] many people in the US criminal justice system have major health care requirements, with 60% of state prisoners and sentenced jail inmates suffering from drug abuse and a considerable percentage suffering from psychological anguish or mental illness. While two-thirds of freed criminals are rearrested within three years, these factors frequently contribute to difficulty in breaking away from the cycle of crime. By treating these underlying problems before individuals enter the criminal justice system, providing accessible therapy in communities might offer a cost-effective and compassionate way to reduce crime rates.


Heat map with Folium:

<embed 
       type="text/html" 
       src="/viz/drugMap.html"
       width="800"
       height="500"
       >



Bokeh Visualization:

<embed 
       type="text/html" 
       src="/viz/bokeh_assignment2.html"
       width="1100"
       height="600"
       >
