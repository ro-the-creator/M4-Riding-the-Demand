## Statistical Analysis

<div align='center'>

For the statistical analysis portion of this project, there were 3 main questions to answer that required different T-tests. This README will go over the functional analysis done to produce statistically-backed results. This document will also serve to provide in-depth answers to the questions posed per each test.

</div>

<br>

## Hypotheses Testing:

### **Question 1:**

<div align='center'>

*Do average hourly rides (remember each row in the data is a ride) differ between working days and non-working days?*
</div>

<br>

<div align='center'>

To prepare a statistical test for this question, we simply must filter our dataset to create two groups that we can compare: **working days** and **non-working days**. Since each instant already represents an hour, we simply feed our raw, filtered data in our function, where we test using an independent T-test.
</div>

<br>

*● What stakeholder would care about this test?*

- I believe both the Product Manager (PM) and the Operations Lead (OL) would care about this test for opposite reasons. 

    - The PM would care because they want to know when demand is strong or fragile. This test will give them a statistically-backed answer and help them focus on a hypothesis for the next quarter.
    - The OL would care about this because they want to know if, perchance, either group has significantly less demand. This would help them make important decision regarding staffing and maintenance, particularly scheduling time to maintain/replace bikes during low demand hours.

*● How should you sample the data?*

- In sampling, we simply filtered the dataset to produce two groups: working days and non-working days.


*● What are the hypotheses, what alpha would you choose and why, how
would you explain the result?*

- **Null Hypothesis**: There is no significant difference between hourly rides for working days vs. non-working days.

- **Alt. Hypothesis**: There is a statistically significant difference between hourly rides for working days vs. non-working days.

- I simply went with an alpha of 0.05, which represents that there is a 5% chance for a type I error. 0.05 is a generally accepted probability, so it felt appropriate here.

<br>

<div align='center'>

### **P-Value:** 4.250x10^-5
</div>

<div align='center'>
Given our P-value, we see that p < a, which tells us to reject our null hypothesis and go with the alternative. The results of this test deem that there is a statistically significant difference between working days vs. non-working days.

After confirming with their means, we can see that non-working days have less average hourly bike usage than its counterpart.

</div>

***

### **Question 2:**

<div align='center'>

*Do mean hourly rides differ across categories of multi-level categorical variables such as season or weather condition? 
If you find a difference, describe the appropriate post-hoc approach and what it would tell stakeholders.*
</div>

<div align='center'>
For this test, I chose to look at weather conditions and their in-group differences using an ANOVA test. This was done by creating groups for each weather condition, which can then be used for testing with functions. I also conducted a Post-Hoc test using Tukey's method, which allowed me to find which group was statistically significantly different than the others.
</div>

<br>

*● What stakeholder would care about this test? Does this change what multi-level categorical variable you choose?*

- I believe the Operations Lead and the Policy & Ethics Advisor (PEA) would care about this test.
    - The OL could use this information for allocating reserved time during harsher weather conditions for maintenance, restocking, etc.
    - The PEA might care about this to know when certain people may be affected and unable to ride bicycles during harsher weather conditions. This is important for maintaining fairness. Not every bike rider is fully able-bodied, and company decisions during harsher weather conditions could possibly negatively impact these people.

*● How should you sample the data?*

- The data is simply grouped together into four groups to be used for the ANOVA test.
    - Clear weather
    - Misty Weather
    - Light Rain Weather
    - Heavy Rain Weather

>[!NOTE]
> Weather groups are generalized and embody many other weather conditions similar to the titled definition.

*● What are the hypotheses, what alpha would you choose and why, how would you explain the result.*

- **Null Hypothesis**: There is no significant difference between the weather groups.

- **Alt. Hypothesis**: There is a statistically significant difference between one or more weather group.

- Again, I went with an alpha of 0.05 here. It remains an appropriate level for the probability of committing a type I error. 

### **P-Value:** 1.735x1010^-81

<div align='center'>
With such a small margin of error, there could possibly be an error during the process of the ANOVA test. Regardless, this result tells us that we should reject the null hypothesis and go with the alternative: that one or more groups are significantly different than the others.
</div>


### **Post-Hoc**

<div align='center'>
Because of our result, we should conduct a post-hoc test, using Tukey's method, to determine which group(s) are statistically different. After using the function and checking the groups' means, we can conclude that the 4th group— Heavy Rain —is statistically significantly different than the other groups. Specifically, it has a lower bike usage than its counterparts.
</div>

<br>


<br>

## Simulated A/B Test:

### **Question 3:**

<div align='center'>

*PM’s objective: Does ridership increase on working days
during early evening after launching a small app feature
change.*
</div>

<br>

<div align='center'>
This section created a simulated A/B testing by creating a before vs. after group comparison, with a hypothetical launch date of 2012-09-01.
This means:
</div>

<br>

- **Pre (Baseline):** 2012-08-04 → 2012-08-31 (inclusive)

- **Post (Feature On):** 2012-09-01 → 2012-09-28 (inclusive)

<br>

<div align='center'>
Furthermore, our group was pre-filtered with the following conditions:
</div>

<br>

- The entry was a working day.

- Between the hours of 5pm - 7pm.

- Only clear or misty weather conditions.

- Humidity was below 70%.

<br>

<div align='center'>
With these filters in mind, we went on to create our hypotheses, primary, and guardrail metrics.
</div>

### **Hypotheses:**
**Null:** There is no significant difference between the pre group and the post group.

**Alternative:** There is a significant difference between the pre group and the post group.

<br>

### **Metrics:**

**Primary:** Our primary metric is bike usage, since this is what is most important for the company when implementing new changes.

**Guardrail:** Without knowing about what change was implemented, our guardrail metrics remained relatively general. I only tracked the count bike usage per instance, the mean of bike rides per hour, and the overall average of bike ride per new instances.

<br>

### **P-Value:** 0.342

<div align='center'>
Given our p > a, we fail to reject the null hypothesis and continue to believe that there is no significant change that the new implementation brought. Even if we were to raise our alpha, there remains a large ~30% probability of committing a type I error, which is too large to consider this a real change.
</div>