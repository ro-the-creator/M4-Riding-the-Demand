# Module 4: BikeShare Analytics


<div align='center'>

<img width="6912" height="3456" alt="bikeshare-banner" src="https://github.com/user-attachments/assets/a4228bfb-d6c3-474e-90ff-ac298c71ef14" />


#### An analysis for a BikeShare Product team, aiming to extract stakeholder-ready insights from hourly usage data to inform pricing, promos, staffing, and availability.

</div>

<br>

## Project Overview

<div align='center'>

BikeShare Products Co. is a public bike provider that offers services to everyone in NYC and Jersey City. Bikes are available for people of all ages, with countless bike stations all across the area! This project aimed to do a deep statistical analysis of BikeShare Products Co.

</div>

<br>

<div align='center'>

### A Quick Look

</div>

- The newly implemented change did *not* have a statistically significant difference from before in terms of bike usage.

- The **Fall season**, specifically **August**, is the busiest time for bike usage. **Weekends** and **Evening** hours are typically the busiest bike usage times.
  - These times should be considered when preparing the bikes/stations for heavy usage. 

- On the contrary, the **Spring season**, specifically **April**, had the least bike usage. **Sundays** and **Early Morning** hours had the least used times. 
  - These times are best for maintenance, replacements, etc. Furthermore, there is an opportunity for more promotions during the Spring season, as the weather still generally permits during these times. This is statistically supported.

<br>

<div align='center'>

### Stakeholders

</div>

- **Product Manager (PM):** When/where demand is strong or fragile; user behavior patterns; which hypotheses to prioritize next quarter.

- **Operations Lead:** Inventory rebalancing windows; staffing for spikes; low-impact maintenance windows.

- **Marketing Lead:** Promo timing (day/hour/season), and segments likely to respond (e.g., casual rider vs registered).

- **Policy & Ethics Advisor:** Equity of access; avoiding decisions that disadvantage specific times/areas; responsible communication of uncertainty.

<br>

<div align='center'>

### About Me

<br>
    
![casual-septum](https://github.com/user-attachments/assets/86b1b472-797d-4c8e-ae70-3cf6ae68bc88)

### Rolando Mancilla-Rojas

Hi! I'm Rolando, but I mainly like to go by Ro. I have a particular interest in business/finance, and I enjoy getting my hands dirty in the data.

[LinkedIn](https://www.linkedin.com/in/rolandoma33/) | [GitHub](https://github.com/ro-the-creator)

</div>

<br>

## README Navigation

- [Exploratory Data Analysis](#exploratory-data-analysis)  
  - [Trends and Insights](#trends-and-insights)  
  - [Visualizations](#visualizations)  
- [Hypotheses Testing](#hypotheses-testing)  
- [AB Testing](#ab-testing)  
- [Results](#results)  
  - [Recommendations](#recommendations)  
  - [Ethics](#ethics)  
- [Repo Navigation](#repo-navigation)



## Exploratory Data Analysis

<div align='center'>

For an initial analysis, there was only a slight amount of cleaning and data confirmation to do. This includes parsing the `dteday` column, checking nulls, and confirming that `casual` + `registered` users added up to the `cnt` column. After, I did simple computations to find the busiest/least busiest times for bike usage. 
</div>

### Trends and Insights

<div align='center'>

For the most part, I discovered that weekends in the evening held the busiest bike usage when checking instances by the hour. These also fell in the Fall season, specifically August. This is the strongest time for the business, and the only area of focus here should be to maintain strong numbers during these times.

On the contrary, I found that the beginning of the week, from Sunday - Wednesday, was the lower bike usage days. Specifically, the early mornings and spring times were very low. While there isn't much to be done about low bike usage during early morning hours, there is a large area in the Spring season that should be the focus of improvement for the next quarter.

More information on exploratory data analysis can be found [here](./cleaning_EDA).

</div>

### Visualizations


<div align='center'>
Visualization was an important part of my analysis. Charting the data not only helps visualize my findings, but it also helps me orient my points of focus during my statistical analysis.

<br>
  
<br>

<img width="622" height="453" alt="holidays-M4" src="https://github.com/user-attachments/assets/88d5c6db-0b14-44c9-9bde-b95e44fc1a54" />


<br>

<img width="1342" height="1856" alt="mod4-fig" src="https://github.com/user-attachments/assets/cb720ce6-7a79-4020-afec-8ce6e1f67ab7" />

<br>

<br>

More details on the visuals, including the process for creation, can be found [here](./visuals).

</div>


## Hypotheses Testing

<div align='center'>
The hypotheses section marked the start of my statistical analysis to find deeper, meaningful insights. Tests included:
</div>

<br>

- Average hourly rides between working vs. non-working days.

- Average hourly rides for varying levels of weather.
  - This included four conditions: Clear, Misty, Light Rain, & Heavy Rain.

<br>

<div align='center'>

These tests gave my insights more meaning by giving statistical context and support. The findings, as well as the process behind these tests, can be viewed in detail [here](./statistics).
</div>

## AB Testing

<div align='center'>
For the second and final part of my statistical analysis, I conducted an A/B test to find any statistical meaning for a new implementation, with a hypothetical launch set on September 1st, 2012.

To do this, separating the dataset using several filters was necessary. This included by date, hour, weather, humidity, and working/non-working days.
</div>

Other important information regarding this test includes:

- **Primary Metric:** Bike Usage per Hour

**Guardrail Metric:** Instances, Mean Bike Usage

<div align='center'>

More information for this test can also be found in the `/statistics` folder [here](./statistics).

</div>

## Results

<div align='center'>
The culmination of the statistical tests and EDA led to several insights and recommendations. Below are personal recommendations tailored for each stakeholder:
</div>

## Recommendations

### Product Manager (PM)

- **Strongest Bike Usage:** Fall (August), Fridays, During Evenings 
  - I recommend maintaining a commitment to keeping bike usage stable during these hours. They are already strong, so maintain this number.

- **Weakest Bike Usage:** Spring (April), Sundays, During Early Mornings 
  - I believe the Spring season should be the focus for the next quarter. There is a large, untapped potential for more usage during this time, especially in conjunction with the holidays. Furthermore, there is potential to improve early-week engagement.

- **Holiday Trends:** Highest during April and November (registered users) 
  - April holidays are a great way to boost sales during the weakest season. Furthermore, I recommend focusing on improve July sales by using the Fourth of July holiday as an incentive. The weather more than permits during these times. 

***

### Operations Lead

- **Peak demand:** Weekends, especially in the evenings
  - I recommend extra staffing during these times, as more bike usage will require more attention.

- **Maintenance windows:** Early weekdays, early in the morning 
  - There is minimal usage during these times and days, thus it is a good time to maintain/replace bikes.

***

### Marketing Lead

- **Promotional opportunities:** 
  - Potential to market to 9-5 workers with weekday specials.
  - Holidays, such as the Fourth of July or Labor Day, could be grounds for promotions to improve sales during these weaker times.

***

### Policy & Ethics Advisor

- **Equity of access:** 
  - Ensure that promotions/pushes during heavier weather seasons don't exclude people who aren't fully able-bodied.
  - Do not only provide maintenance during early morning hours; There is still bike usage during those times. Those people matter too.

---


### Ethics

<div align='center'>
During my statistica analysis, it was important that I maintained the standard transparency, ethical, and equitable commitment I made since I first entered the world of data analytics. I ensured my strength to that commitment by:
</div>

<br>

- **Cleaning:** transparent notebook, no rows dropped.

- **Feature Engineering:** Ensuring new columns don't exclude any data.

- **Ethical Mindset:** Researching the usage of bikes by all people, not just the able-bodied.


## Repo Navigation

- [/cleaning_EDA](./cleaning_EDA)
- [/statistics](./statistics)
- [/visuals](./visuals)
- [/slides](./slides)

