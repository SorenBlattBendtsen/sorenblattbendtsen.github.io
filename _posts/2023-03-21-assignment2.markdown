---
layout: post
title: "Assignment 2"
subtitle: "Drug related crimes in San Francisco"
date: 2023-03-21 12:30:00 +0100
author: Vivien Váradi, Thomas Adamopoulos & Søren Blatt Bendtsen
background: '/img/my_images/golden_gate_bridge.jpg'
---

## Introduction

Welcome to our GitHub website devoted to investigating drug-related occurrences in San Francisco!
In this project, Søren, Vivien, and Thomas have used the Police Department Incident Reports Historical 2003 to May 2018 dataset to analyze drug crime incidents in San Francisco from 2003 to 2018.
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
    background-color: #b19cd9; /* Change the background color of the header */
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

To only focus on complete years for better comparison, we only included data up until 2017. From the exploration of the dataset it follows that the total number of crimes is 2,084,466 which are categorized in 37 cetegories. The total number of drug related crimes is 116,352 and as it can be seen, it was the sixth most occuring crime in San Francisco between 2003 and 2017. 

## Positice development in drug/narcotics crime

![Number of crimes per category](/viz/number_crimes_per_category.png){: width="800" }

We selected to analyze "drug/narcotics" incidents from the San Francisco crime dataset because of their considerable influence on public health, safety, and general community quality of life. But also because of an interesting development for this type of crime in San Francisco. 

![Calendar plot](/viz/cal_plot_assignment2.png){: width="800" }

One observation from the calendar plot above is that after 2010 drug-related crimes began to decrease noticeably. Up until 2010, there were almost always several days a week with up to 40-75 daily incidents. From 2010 that number went down, and in 2017 that number was between 0-20 daily incidents. So what's going on and has drug-related crime really gone down in San Fransisco? The answer lies in a change in strategy from both political and police-force perspective; from a "war-on-drugs" strategy to a "preventive and root problem" strategy.

The first part of the answer can be found in the comprehensive health care reform, also known as Obamacare, enacted on March 23, 2010 [1]. Obamacare does not specifically directly address substances. But, it does include provisions for mental health care, prescription medications, and substance use disorders. The Obamacare forbids insurers from refusing coverage or raising premiums based on pre-existing diseases, including substance use disorders, and mandates coverage for mental health and substance use disorder therapies [2].


According to Bronson et al. (2017)[3] many people in the US criminal justice system have major health care requirements, with 60% of state prisoners and sentenced jail inmates suffering from drug abuse and a considerable percentage suffering from psychological anguish or mental illness. While two-thirds of freed criminals are rearrested within three years, these factors frequently contribute to difficulty in breaking away from the cycle of crime. By treating these underlying problems before individuals enter the criminal justice system, providing accessible therapy in communities might offer a cost-effective and compassionate way to reduce drug-related crime rates.

Together with this, the city ran a more progressive public health policy with medical cannabis and needle exchange [4], while focusing police efforts to crack down on criminal groups and drug-dealers, instead of individual drug-users [5].

## Tenderloin - San Francisco's drug center

To understand the development further, we will look at the development over time across the different Police Districts in San Francisco. By clicking on the name of a district in the interactive visualization below, you can highlight the development across different districts.

<embed 
       type="text/html" 
       src="/viz/bokeh_assignment2.html"
       width="1100"
       height="600"
       >

Again, we clearly see that drug-related crime has decreased with the total number being three times lower in 2017 compared to 2009. The visualization shows us that the development has happened across all the police district, although drug-related crime continues to be centralized in a few specific districts, such as Tenderloin and Southern, accounting for app. half of all drug-related incidents. The same trend is visualized in the heat-map below (click on play to see the development).

<embed 
       type="text/html" 
       src="/viz/drugMap.html"
       width="800"
       height="500"
       >

So we can see that the city of San Francisco in general has had success on tackling drug-related crime, although it continues to have a challenge in certain neighborhoods, such as Tenderloin, which is one of the hippest neighborhoods in the city. The co-author of this article, Søren Blatt Bendtsen, remembers visiting San Francisco and Tenderloin as a teenager in 2009, during the peak of drug-related incidents. He remembers how while walking through beautiful parks, visiting museums, theaters and shopping in the hippest music and clothes stores, you would see needles lying on the streets and groups of homeless people sleeping in the parks.

From these visualizations, it is easy to assume that the trend could have continued decreasing, especially considering the legalization of marijuana in 2018 [6] and the implementation of safe injection sites in 2019 [4]. While this has been the case for most neighborhoods, the development in Tenderloin has gone completely backwards. In 2021, Tenderloin accounted for more than 60 % of the city's drug-related crime! It has become so bad, that the San Francisco Mayor, London N. Breed, in December 2021 called it an epidemic and declared a State of Emergency in the neighborhood to take more drastic measures into account to tackle these issues [5]. So it might look like the "preventive and root cause" strategy from previous years have come to an end, and a new tough-on-crime era has begun.


[1] : [Patient protection and affordable care act](https://www.healthcare.gov/glossary/patient-protection-and-affordable-care-act/){:target="_blank"}{:rel="noopener noreferrer"}

[2] : [Health care law protections](https://www.healthcare.gov/health-care-law-protections/){:target="_blank"}{:rel="noopener noreferrer"}

[3] : [ Bronson et al. (2017)](https://bjs.ojp.gov/content/pub/pdf/dudaspji0709.pdf){:target="_blank"}{:rel="noopener noreferrer"}

[4] : [California bill allowing San Francisco safe injection sites](https://www.sfchronicle.com/bayarea/article/California-bill-allowing-San-Francisco-safe-13589277.php){:target="_blank"}{:rel="noopener noreferrer"}

[5] : [San Francisco Chronicle, These charts show how drug incidents](https://www.sfchronicle.com/bayarea/article/These-charts-show-how-drug-incidents-in-the-16723745.php){:target="_blank"}{:rel="noopener noreferrer"}

[6] : [Weed legal San Francisco](https://lajolla.com/article/weed-legal-san-francisco/){:target="_blank"}{:rel="noopener noreferrer"}

