---
layout: post
title: "Health and wealth - a Copenhagen data story"
subtitle: "Final project"
date: 2023-04-14 12:30:00 +0100
author: Vivien Váradi, Thomas Adamopoulos & Søren Blatt Bendtsen
background: '/img/my_images/rigshospitalet.jpg'
---
# Motivation - from a cold Carlsberg to understanding inequality in Copenhagen

We are a group of three people with different backgrounds working on this data story together. The idea for the story came to us over a few cold Carlsbergs on a Friday after noon. Two of us are foreigners who moved to Copenhagen to study a few years ago and one of us is born and raised in the city. Over a heated (but friendly) discussion, we realized we had quite different perspectives on life in Copenhagen. As a foreigner in Copenhagen, you quickly realize what all the life- and travel magazines they talk about. Besides the long and gray winters, quality of life seems very high in the city with it's fun and green neighborhoods, biking culture, free high quality education and delicious Nordic cuisine. Especially when you compare it to growing up during years with financial crisis in Athens or Budapest.

But for someone who has lived in Copenhagen for almost 30 years, it also feels like the city has changed a lot, and maybe not always for the better. It has become more and more expensive to live in the city and it feels like demographics has changed. In general, the inequality has been on the rise creating larger and larger differences in income and health across the different municipalities of Greater Copenhagen.

Although the Social Democratic party, who historically has been very strong in Copenhagen, always has had it as a primary goal to fight for more equality, the former Mayor of Copenhagen, Frank Jensen, in 2016 recognized the negative development and expressed his concern: "We know the development from other big cities, where the richest start to hide themselves behind surveillance and barbed wire, and I do not wish this for Copenhagen" [1]. Since then there has been economic disturbances with a global pandemic followed by Russia's invasion of Ukraine, which only looks like it will create even further inequality [2].

This discussion gave us the motivation to look at and analyze the data to understand what has really been going on in Copenhagen in terms of wealth and health. How is the region of the Greater Copenhagen during compared to the rest of Denmark and what does these differences look like across the different municipalities of Greater Copenhagen? How has the development been over time and different demographic groups?

# Dataset exploration
To answer these questions, we have worked on a dataset gathered from Rockwool Fonden's tool, Wealth and Inequality [3]. A further exploration of the dataset and the required data preparation can be found  [here in our Explainer Jupyter Notebook](https://github.com/vivivaradi/socialdata2023/blob/master/assignments/Explainer%20Notebook.ipynb){:target="_blank"}{:rel="noopener noreferrer"}, but in general the final data set consisted of 14 columns and app. 12,000 rows. The table below provides a quick reference to the essential features and qualities used for this analysis. 

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
    width: 98%; /* Set the width of the table to 80% of its container */
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
Before diving deep into what is happening in Copenhagen, we want to put the development of health and and income into perspective. To do so, let's have a comparison over time between the Greater Region of Copenhagen with it's 20 municipalities and Denmark as a whole. The story across the entire country is in general a positive one where income has been growing and time spent in the hospital is decreasing.

### Interactivity
The following sections will include interactive visualizations where you yourself can drill down into the graph for further investigation. You can do so by using the drop down menus as filter and by hovering over the graphs with the mouse for more information. However, it is important to mention that you can only apply one drop down filter at a time. So if you first make a filter for Gender and then afterwards make a filter for Age, then the Gender filter no longer is applied. We invite you to play around with the drop down menus as well as hovering over the bars for more information or highlighting specific time periods.

### Income

<embed 
       type="text/html" 
       src="/viz/dk_cph_income_bar.html"
       width="900"
       height="450"
       >

The visualization above shows the development over time of annual disposable income for Greater Copenhagen and Denmark. It is clear to see that, Copenhagen has had a relatively higher income than the rest of the country. The biggest gaps of income are found when diving down into the different age groups, especially from 40 years and above. This is a trend that has been growing over the years where the older you get when living in Copenhagen, the more disposable income you have compared to the rest of the country. While also looking at ethnic Danish people, the income gap between the capital and the rest of the country has followed the same trend.

On the other hand, Immigrants and Descendants has had a similar income, where only in reason years the income has become slightly higher for those living in Greater Copenhagen. If diving deeper down into ethnicity, we find that Non-Wester Immigrants and Descendants, as the only demographic group, have a lower income in the capital, and the difference is quite noticable.


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
When looking at the development on two important health parameters, Number of Days in Hospital and Number of Hospitalizations, both the Danish population as well as the citizens of the capital have had a significant decrease in how much time they spent in the hospital. On the other hand, there has been a slight increase in the amount of hospital visits. As one would expect, elder people spend more time and have more visits to the hospital, but significantly more within Copenhagen. 

When diving down in the visualizations, we can find some interesting demographic trends. The average man in Denmark spend more time in the hospital compared to men in Copenhagen, and also compared to women across the country. We can also see an important difference between educated and non-educated peopl, where e.g. high educated people in Copenhagen spend less time in the hospital than high educated people in the rest of Denmark, but low educated people in Copenhagen spend more time in the hospital compared to the rest of Denmark. At last we also see, that Immigrants and Descendants, especially Non-Western, spend much less time in the hospital compared to ethnic Danish people.

So what can we learn from this? Although the level of income is higher in Copenhagen than the country average, the difference within health parameters don't stand out in the same way. Within certain groups, especially for elder people, much more time is spent in the hospital for citizens in Copenhagen. As we could also see from the cluster analysis, age was the strongest descriptive parameter for both wealth and health. Having this in mind, let's deep dive into the 20 municipalities within the Greater Region of Copenhagen!

### K-means clustering analysis
We have furthemore performed a K-means clustering algorithm, which is an unsupervised machine learning model, applied to divide data into segments with similar behaviour. By doing so, we have found four clusters, which can be seen in the visualization below:

<embed 
       type="text/html" 
       src="/viz/kmeans.html"
       width="900"
       height="450"
       >

The clusters are shown on a scatter plot that compares Income and Days in Hospital for the people in Greater Copenhagen and for Denmark as a whole. It has been interesting to see, that the clusters are separated almost entirely based on different age groups. This confirms what we have already seen in the bar plots. Although there are some interesting differences between Denmark and Copenhagen, for both areas age is the best variable to explain income level and health status.


# Copenhagen municipalities
* on the parameter that stands out, deeper analysis comparing the municipalities of Copenhagen with each other.
* map with correlation between income and health? and then income and health also in tool tip?
* Possible to do a cluster analysis? Create different clusters with a certain income and health and then see if there are any obvious patterns in which municipalities these clusters live in?

During the following, we're going to take a closer look at Copenhagen and the differences between the individual municipalities within. The maps contain data about the development of income and hospitalizations across the years, from 2005 until 2018. 

### Interactivity: 
The maps work like a Gif. They will start playing automatically, but you can press the play button to restart and it will then run through all of the years showing the updated map. You can pause the gif at any given year and hover over a municipality with the mouse to see more information in the tool-tip.

<embed 
       type="text/html" 
       src="/viz/cph_income_time_map.html"
       width="900"
       height="750"
       >

<embed 
       type="text/html" 
       src="/viz/cph_hosp_times_time_map.html"
       width="900"
       height="750"
       >

<embed 
       type="text/html" 
       src="/viz/cph_hosp_days_time_map.html"
       width="900"
       height="750"
       >

After playing all of them, it is clear that there are staggering differences even between the municipalities. What's even more interesting is that here we can observe the exact opposite of what we saw in the previous section: the areas with the highest average salary generally have lower values for both number of days spent in hospital and times of hospitalization. 

Moreover we can observe one more interesting piece of information, which is that while during the years the average days spent in hospital is decreasing, the times of hospitalization shows an increasing tendency. This is an interesting contrast, but can possibly be explained by the technological advancement and machines and staff becoming more and more efficient at examining people. 

### Regression analysis
To finish off this analysis, we have applied a regression analysis to try to predict the development of Days Spent in Hospital based variables such as income, municipality, age, education and ethnicity. What we have predicted is:

* Older age is associated with much more days spent in the hospital compared to younger people.
* Higher education will lead to fewer days in hospital, whereas people without higher education will spend more time in the hospital in the future.
* A surprising insight is related to gender, where it looks like women will spent much less time in the hospital and men will spent more time.
* Danish ethnicity continues to be associated with more days in hospital compared to Immigrants and Descendants.
* Living in different municipalities shows varied relationships with days in hospital, but in general not that big. For instance, living in a low-income municipality like Glostrup is associated with more days in hospital, whereas living in Gentofte is associated with fewer days.

### So what did we learn from this? 
Generally speaking Denmark as a whole, as well as all of the Copenhagen municipalities, have become wealthier and healthier between 2005 and 2018. At least when just looking at disposable income and time spent in the hospital. However, this positive growth has been stronger in Copenhagen compared to the rest of the country. And when looking inside of Copenhagen, this growth has even been more uneven, creating a much larger gap between those living in the northern municipalities compared to especially those in the south-west.

We have also seen another major difference between Denmark and Copenhagen. While there in Denmark as a whole does not seem to be a strong correlation between income and time spent in hospital, this is exactly the opposite within Copenhagen, where people living in the richest neighborhoods usually spend less time in the hospital than those living in low-income neighborhoods. 

This supports the original idea we had of growing inequality in Copenhagen. When applying a k-means clustering model, we see that age is the strongest variable to describe the health and wealth status. However, when doing a regression analysis, we are confirmed of the inequality across neighborhoods and groups of people in Copenhagen. The model e.g. predicts men to spend much less time in the hospital in the future compared to woman. We predict a similar situation when looking at education level leading to an even bigger gap in health between those with a high level of education and those who does not.

This is a concerning development and we belive the differences have only been amplified with the previous years of pandemic and war on European territory. We invite politicians and other decision makers to dive down in the newest data to understand the current situation and take action towards a more equal Copenhagen.

# Do you want to know more?
We hope you found this article insightful! If you want to know more, have a look [here at our Explainer Jupyter Notebook](https://github.com/vivivaradi/socialdata2023/blob/master/assignments/Explainer%20Notebook.ipynb){:target="_blank"}{:rel="noopener noreferrer"} with code and explinations of all the data analysis and visualizations.


# References

[1] : [Politiken, København bliver rigere men mere skæv](https://politiken.dk/indland/art5613464/K%C3%B8benhavn-bliver-rigere-men-mere-sk%C3%A6v){:target="_blank"}{:rel="noopener noreferrer"}

[2] : [Arbejderbevægelsens Erhvervsråd, Krig vil ramme danskernes forbrug og realløn](https://www.ae.dk/analyse/2022-03-krig-vil-ramme-danskernes-forbrug-og-realloen){:target="_blank"}{:rel="noopener noreferrer"}

[3] : [Rockwool Fonden, Velstand og Ulighed](https://www.velstandogulighed.dk/){:target="_blank"}{:rel="noopener noreferrer"}