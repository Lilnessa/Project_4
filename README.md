# Project_4
Final Project 
---
Project Documentation Google Doc Link: https://docs.google.com/document/d/1cK-BasG8VOG2Pyr7UydXSSvqZxWtqCOU6hbMN1aXNRE/edit?usp=sharing

**Overview and Purpose**
The final project was constructed to present an individual retirement calculator. A general question most individuals in the workforce have is "When can I retire?" The goal of this project is to help someone accurately answer this question. The predictive model is based on three data sets that are part of the overall retirment blueprint. They are the respective cost of living in each of the United States, overall countrywide inflation, and average life expectancy based on age and gender. The result is a calculator that is highly accurate in its ability to predict whether an individual is qualified for retirement. If the individual is not eligible for retirement, the calculator provides an estimate as to how much more would be needed to reach the threshold of retirement. 

**The Models**

INFLATION

The United States Bureau of Labor Statistics has inflation data since 1913. A predictive model was made using data from the last 110 years to estimate what inflation may look like in the coming 80 years. The programming model was coded with Facebook Prophet with a high degree of accuracy. It shows inflation gradually increasing every year which directly affects someone's ability to retire. This displays how much or how little the US Dollar will be worth in a given year. With this information, one can more accurately predict how much savings that person will need to retire.

LIFE EXPECTANCY

The life expectancy data was taken from the Social Security Administration. The models were taken based on the average life expectancy for both females and males. As the model shows, life expectancy fluctuates between the two genders. To more accurately predict whether someone can retire, the model can show how much longer that person is likely to live. This is necessary for the model as to predict whether someone can retire or not. 

COST OF LIVING

The data was gathered from Forbes Magazine to show the differences between the states in cost of living. They include housing costs, transportation, food costs and taxes in each of the 50 states. The model was based on CPI to showcase how expensive it can be to live in the various states. Each state has the average cost of living that was placed into the model. Hawaii and Massachusetts would be the two most expensive states while Mississippi and Alabama are the cheapest for average cost of living. With each state being different in terms of cost, it will directly reflect how much savings someone would need to retire. 

RETIREMENT CALCULATOR
With all the data collected, the model can finally predict if a person is a candidate for retirement. By using their income level for their state, life expectancy, and inflation, the calculator will showcase if a person is eligible for retirement with a high degree of accuracy. If they are not eligible for retirement, the calculator will describe how much more money is needed to retire. 

**Resources**
https://www.ssa.gov/oact/STATS/table4c6.html,
https://www.bls.gov/cpi/,
https://www.forbes.com/advisor/mortgages/cost-of-living-by-state/

**Citations**
Code used for Facebook Prophet
https://facebook.github.io/prophet/docs/quick_start.html
https://www.forbes.com/advisor/mortgages/cost-of-living-by-state/

**Citations**
