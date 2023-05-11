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
Before diving deep into what is happening in Copenhagen, we want to put the development of health and and income into perspective. To do so, let's have a comparison over time between the Greater Region of Copenhagen with it's 20 municipalities and Denmark as a whole. 

### Interactivity
The following sections will include interactive visualizations where you yourself can drill down into the graph for further investigation. You can do so by using the drop down menus as filter and by hovering over the graphs with the mouse for more information. However, it is important to mention that you can only apply one drop down filter at a time. So if you first make a filter for Gender and then afterwards make a filter for Age, then the Gender filter no longer is applied.

### Income

<embed 
       type="text/html" 
       src="/viz/dk_cph_income_bar.html"
       width="900"
       height="450"
       >

The visualization above shows the development over time of annual disposable income for Greater Copenhagen and Denmark. It is clear to see that, since the financial crisis in 2008, there has been a positive growth in income and that through this entire period, Copenhagen has had a relatively higher income than the rest of the country. The biggest gaps of income are found when diving down into the different age groups, especially from 40 years and above. This is a trend that has been growing over the years where the older you get when living in Copenhagen, the more disposable income you have compared to the rest of the country. While also looking at ethnic Danish people, the income gap between the capital and the rest of the country has followed the same trend.

On the other hand, Immigrants and Descendants has had a similar income, where only in reason years the income has become slightly higher for those living in Greater Copenhagen. If diving deeper down into ethnicity, we find that Non-Wester Immigrants and Descendants, as the only demographic group, have a lower income in the capital, and the difference is quite big.


### Health

<embed 
       type="text/html" 
       src="/viz/dk_cph_days_hospital_bar.html"
       width="900"
       height="450"
       >

<embed 
       type="text/html" 
       src="/viz/dk_cph_hospitalizations_bar.html"
       width="900"
       height="450"
       >

<p align="center">
  <embed 
       type="text/html" 
       src="/viz/dk_cph_days_hospital_line.html"
       width="43%"
       height="350">
&nbsp; &nbsp; &nbsp; &nbsp;
  <embed 
       type="text/html" 
       src="/viz/dk_cph_hospitalizations_line.html"
       width="43%"
       height="350">
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
       caption="Note: only possible to apply one filter at the time"
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