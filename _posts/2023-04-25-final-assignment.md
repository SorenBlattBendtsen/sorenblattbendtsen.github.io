---
layout: post
title: "Health and wealth - a Copenhagen data story"
subtitle: "Final project"
date: 2023-04-14 12:30:00 +0100
author: Vivien Váradi, Thomas Adamopoulos & Søren Blatt Bendtsen
background: '/img/my_images/rigshospitalet.jpg'
---
# Motivation - from a cold Carlsberg to understanding inequality in Copenhagen

We are a group of three people with different backgrounds working on this data story together. The idea for the story came to us over a few cold Carlsbergs on a Friday after noon. Two of us are foreigners who moved to Copenhagen to study a few years ago and one of us is born and raised in the city. Over a heated (but friendly) discussion, we realized we had quite different perspectives on life in Copenhagen. As a foreigner in Copenhagen, you quickly realize what all the world-reknowned life- and travel magazines they talk about. Besides the long and gray winters, quality of life seems very high in the city with it's fun and green neighborhoods, biking culture, free high quality education and delicious Nordic cuisine. Especially when you compare it to growing up during years with financial crisis in Athens or Budapest.

But for someone who has lived in Copenhagen for almost 30 years, it also feels like the city has changed a lot, and maybe not always for the better. It has become more and more expensive to live in the city and it feels like demographics has changed. In general, the inequality has been on the rise creating larger and larger differences in income and health across the different municipalities of Greater Copenhagen.

Although the Social Democratic party, who historically has been very strong in Copenhagen, always has had it as a primary goal to fight for more equality, the former Mayor of Copenhagen, Frank Jensen, in 2016 recognized the negative development and expressed his concern: "We know the development from other big cities, where the richest start to hide themselves behind surveillance and barbed wire, and I do not wish this for Copenhagen" [1]. Since then there has been economic disturbances with a global pandemic followed by Russia's invasion of Ukraine, which only looks like it will create even further inequality [2].

This discussion gave us the motivation to look at and analyze the data to understand what has really been going on in Copenhagen in terms of wealth and health. How is the region of the Greater Copenhagen during compared to the rest of Denmark and what does these differences look like across the different municipalities of Greater Copenhagen? How has the development been over time and different demographic groups?

# Dataset exploration
To answer these questions, we have worked on a dataset gathered from Rockwool Fonden's tool, Wealth and Inequality [3]. A further exploration of the dataset and the required data preparation can be found here in our Explainer Jupyter Notebook, but in general the final data set included consisted of 16 columns and  39605 rows. The table below provides a quick reference to the essential features and qualities used for this analysis. 

| Column Name | Definition | Type | Scale |
|----------|----------|----------|----------|
| Municipality | Name of the 20 municipalities in Region of Greater Copenhagen as well as the average of the region and the average of Denmark as a whole  | string/text  | Categorical |
| Year | Years running between 2005 and 2018  | Integer | Discrete |
| Gender | Men, Women | string/text | Categorical|
| Age | Four different age groups: 30-39, 40-49, 50-59, 60-65 | string/text | Categorical|
| Ethnicity | Four different ethnicity groups: Danish, Immigrants & Descendants, Non-Western Immigrants & Descendants | DateTime | Continuous|
| Education | Two educational groups: Higher Education, No Higher Education | string/text | Categorical|
| Income | Average income for each group combination of the above categorical variables | Float | Continuous|
| Days In Hospital | Average days spent in hospital for each group combination of the above categorical variables | Float | Continuous|
| Number of Hospitalizations | Average number of hospitalizations for each group combination of the above categorical variables | Float  | Continuous |

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



# Greater Copenhagen vs Denmark
* graphs on income and health comparing Denmark with Copenhagen
  * Copenhagen performs better than the rest of the country in general
* graphs on specific on age, gender, education and ethnicity.
  * Does anything stand out?



<p align="center">
  <embed 
       type="text/html" 
       src="/viz/dk_cph_days_hospital_line.html"
       width="400"
       height="400">
&nbsp; &nbsp; &nbsp; &nbsp;
  <embed 
       type="text/html" 
       src="/viz/dk_cph_hospitalizations_line.html"
       width="400"
       height="400">
</p>


# Copenhagen municipalities
* on the parameter that stands out, deeper analysis comparing the municipalities of Copenhagen with each other.
* map with correlation between income and health? and then income and health also in tool tip?
* Possible to do a cluster analysis? Create different clusters with a certain income and health and then see if there are any obvious patterns in which municipalities these clusters live in?

<embed 
       type="text/html" 
       src="/viz/cph_income_time_map.html"
       width="1000"
       height="750"
       >

<embed 
       type="text/html" 
       src="/viz/cph_hosp_times_time_map.html"
       width="1000"
       height="750"
       >

<embed 
       type="text/html" 
       src="/viz/cph_hosp_days_time_map.html"
       width="1000"
       height="750"
       >




# Did you follow along? Take the quiz!

<iframe
  src="/viz/sample-quiz.html"
  style="width:100%; height:300px;"
></iframe>


# References

[1] : [Politiken, København bliver rigere men mere skæv](https://politiken.dk/indland/art5613464/K%C3%B8benhavn-bliver-rigere-men-mere-sk%C3%A6v){:target="_blank"}{:rel="noopener noreferrer"}

[2] : [Arbejderbevægelsens Erhvervsråd, Krig vil ramme danskernes forbrug og realløn](https://www.ae.dk/analyse/2022-03-krig-vil-ramme-danskernes-forbrug-og-realloen){:target="_blank"}{:rel="noopener noreferrer"}

[3] : [Rockwool Fonden, Velstand og Ulighed](https://www.velstandogulighed.dk/){:target="_blank"}{:rel="noopener noreferrer"}