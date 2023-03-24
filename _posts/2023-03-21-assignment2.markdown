---
layout: post
title: "Assignment 2"
subtitle: "Drug related crimes in San Francisco"
date: 2023-03-21 12:30:00 +0100
author: Vivian Váradi, Thomas Adamopoulos & Søren Blatt Bendtsen
background: '/img/my_images/golden_gate_bridge.jpg'
---

Welcome to our GitHub website devoted to investigating drug-related occurrences in San Francisco!
In this project, Soren, Vivi, and Thomas have used the Police Department Incident Reports Historical 2003 to May 2018 dataset to analyze drug crime incidents in San Francisco from 2003 to 2018.
Utilizing this dataset, we investigated trends and patterns in San Francisco drug crime occurrences, as well as the influence of other parameters such as time and location. Our objective is to learn more about the nature and scope of drug-related crime.

We hope you find this project useful and interesting. Thank you for stopping by!

## Dataset exploration 

The initial dataset consisted of 36 columns and  2215024 rows. The table below provides a quick reference to the essential features and qualities we used.
| Column Name | Definition | Type | Scale |
|----------|----------|----------|----------|
| IncidNTnUM | Incident Number: The number issued on the report, sometimes interchangeably referred to as the case number  | Integer  | Continuous |
| Category | Incident Category: A category mapped on the Incident Number used in statistics and reporting. Mappings provided by the crime. Analysis Unit of ther Police Department  | string/text | Categorical|
| DayOfWeek | The day of the week the incident occured | string/text | Categorical|
| Date | The date the incident occured | DateTime | Continuous|
| Time | The time the incident occured | DateTime | Continuous|
| PdDistict | The Police Disrtict that the incident reported. These are entered by the officers and not based on the point of the incident | string/text | Categorical|
| X | The longitude coordinate in WGS84 | longitude | Continuous|
| Y | The latitude coordinate in WGS84 | latitude | Continuous|
| PdId | Precinct ID at which precinct ws the incident reported | Integer  | Categorical |

<style>
table {
    border-collapse: collapse;
    width: 80%; /* Set the width of the table to 80% of its container */
    margin-left: auto; /* Center the table horizontally */
    margin-right: auto; /* Center the table horizontally */
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2); /* Add a shadow effect */
}
table td, table th {
    border: 1px solid #ccc; /* Change the border color */
    padding: 10px; /* Increase the padding */
    font-size: 14px; /* Set the font size of the table cells */
}
table th {
    background-color: #5D3BB9; /* Change the background color of the header */
    color: white; /* Change the header text color */
    font-weight: bold; /* Make the header text bold */
}
table tr:nth-child(even) {
    background-color: #f2f2f2; /* Set a background color for even rows */
}
table tr:hover {
    background-color: #ddd; /* Set a background color for row hover */
}
</style>







From the exploration of the dataset it follows that the total number of crimes is 2084466 which are categorized in 37 cetegories. The total number of drug related crimes is 116352 and as it can be seen it is the most occuring crime in San Francisco. 

![Number of crimes per category](/img/number_crimes_per_category.png){: width="800" }


![Calendar plot](/img/updated%20calendar%20plot%20.png){: width="800" }

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
