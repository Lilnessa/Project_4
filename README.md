# Project_4
Final Project

**Overview and Purpose**
The final project was constructed to present an individual retirement calculator. A general question most individuals in the workforce have is "When can I retire?" The goal of this project is to help someone accurately answer this question. The predictive model is based on three data sets that are part of the overall retirment blueprint. They are the respective cost of living in each of the United States, overall countrywide inflation, and average life expectancy based on age and gender. The result is a calculator that is highly accurate in its ability to predict whether an individual is qualified for retirement. If the individual is not eligible for retirement, the calculator provides an estimate as to how much more would be needed to reach the threshold of retirement. 

**Data Sets**
LIFE EXPECTANCY

The life expectancy data was taken from the Social Security Administration. The models were taken based on the average life expectancy for both females and males in 2024. As the model shows, life expectancy fluctuates between the two genders. This is important to reflect in the model because it needs to accurately predict whether someone can retire based on how much longer he or she is expected to live. As the data shows, women live longer than men by an average of 5 years. Women in general then would need to have more savings if they would like to retire.

COST OF LIVING

The data was gathered from Forbes Magazine to show the differences between the states in cost of living. They include housing costs, transportation, food costs and taxes in each of the 50 states. The model was based on CPI to showcase how expensive it can be to live in the various states. Each state has the average cost of living that was placed into the model. Hawaii and Massachusetts would be the two most expensive states while Mississippi and Alabama are the cheapest for average cost of living. With each state being different in terms of cost, it will directly reflect how much savings someone would need to retire. The model will show how much more savings someone would need if they move states or plan on retiring in another state. 

**Optimization**
There were previous models made before the Prophet model in attempts of optimization. Those previous models used a linear regression model, which on average gave an r squared value of 0.73.
 
The Jupyter Notebook shruti_model.ipynb contains one model which used a linear regression model and had an r squared value of 0.839. 

The Jupyter Notebooks linear_regression_annual.ipynb and linear_regression_month.ipynb both contained one model each using a linear regression model and had an r-squared value of 0.837. The difference between the two models is that the linear_regression_annual.ipynb used annual CPI values from 1913-2023, while the linear_regression_month.ipynb used monthly CPI values from January 1913 - December 2023.

The Jupyter Notebook demp.ipynb contained four different models. The first model used a linear regression model and had a r squared value of 0.837. The second model used a ridge regression model and had a r squared value of 0.837. The third model used a lasso regression model and had a r squared value of 0.837. The fourth model used a RandomForest regression model and had a r squared value of 0.999.

**Machine Learning Model**
INFLATION

The United States Bureau of Labor Statistics has inflation data since 1913. A predictive model was made using data from the last 110 years to estimate what inflation may look like in the coming 80 years. The programming model was coded with Facebook Prophet with a high degree of accuracy. It shows inflation gradually increasing every year which directly affects someone's ability to retire. This displays how much or how little the US Dollar will be worth in a given year. With this information, one can more accurately predict how much savings that person will need to retire if inflation is going to continue to rise. 

RETIREMENT CALCULATOR

With all the data collected, the model can finally predict if a person is a candidate for retirement. By using their income level for their state, life expectancy, and inflation, the calculator will showcase if a person is eligible for retirement with a high degree of accuracy. If they are not eligible for retirement, the calculator will describe how much more money is needed to retire.

**Resources**
https://www.ssa.gov/oact/STATS/table4c6.html,
https://www.bls.gov/cpi/,
https://www.forbes.com/advisor/mortgages/cost-of-living-by-state/

**Citations**
Code used for Facebook Prophet
https://facebook.github.io/prophet/docs/quick_start.html#python-api
