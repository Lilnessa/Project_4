# Project 4 Appendix
An overview of what is in each file in the Project 4 Github Repository

## Cleaning the data
The original life expectancy data was cleaned in the [life_expectancy.ipynb](life_expectancy.ipynb) Jupyter Notebook file. The age and associated life expectancy for female and male were extracted for the year 2024. Then the data was combined into one data frame based on the age, and was exported as a csv file called [life_expectancy_df.csv](Resources/life_expectancy_df.csv). 

The original cost of living data was cleaned in the [cost_living.ipynb](cost_living.ipynb) Jupyter Notebook file. The state and the corresponding average cost of living was extracted from the original data source. The cost of living was then cleaned into an integer value, and the final data frame was exported as a csv file called [cost_living_df.csv](Resources/cost_living_df.csv).

The original inflation data was inputed into a SQL database in the Jupyter Notebook v_inflation_excel to sql.ipynb in the [Resources](Resources) folder. The SQL table was then called into a pandas database in the Jupyter Notebook file [project_4.ipynb](project_4.ipynb). Once into a database the table was cleaned, and then the data was reformatted to have the date for the end of each month, and the associated monthly average CPI value. This cleaned database was the format then used for the model.

## Model
The final optimized model can be found in the Jupiter Notebook file [project_4.ipynb](project_4.ipynb). The model used the prophet model, which a model by Meta which is an additive model for forecasting time series data based on an additive model where non-linear trends are fit with yearly, weekly, and daily seasonality, plus holiday effects [Meta Github](https://facebook.github.io/prophet/#:~:text=Prophet%20is%20a%20procedure%20for,several%20seasons%20of%20historical%20data.). The model was fit to the cleaned inflation data, where the feature for the model, X, was the date from the cleaned inflation data,, while the target for the model, y, was the monthly CPI value from the cleaned inflation data. The prophet model had a r squared value of 0.998.

The end of the month dates for January 2024 to December 2103 were then generated in a new data frame, and the model then predicted the CPI values for those months. From that prediction, the annual CPI values for 2024 to 2103 were then calculated and exported to the file [df_to_2103_annual.csv](Resources/df_to_2103_annual.csv) which can be found in the Resources folder.


## Calculator
The retirement calculator can be found in the Jupiter Notebook file [retirement_calculator.ipynb](retirement_calculator.ipynb). The calculator used the cleaned cost of living and life expectancy data as well as the predicted CPI values for the year 2024 to 2103. The calculator ask for the users, age, biological sex, retirement savings, and state of residence. Based on the age and sex, the number of predicted years of life yet is calculated. From the number of years left, the last year + 1 is calculated, and the cost of living based on the state from the current year to the last year is adjusted for inflation using the predicted CPI values. The all of the adjusted yearly cost of livings are added, and the savings are subtracted from that value. The calculator then tells you how much money you need to retire at that moment, or if you have enough to retire right now.  


## Optimized Models
There were previous models made before the Prophet model in attempts of optimization which can be found in the Optimizing Attempts folder. Those previous models used a linear regression model, which on average gave an r squared value of 0.73.

## Data sources:
The inflation data that was used for the model came from the [U.S. Bureau of Labor Statistics](https://data.bls.gov/timeseries/CUUR0000SA0?years_option=all_years) and the original data can be found in the Resources folder as [CPI_report_origin.xlsx](Resources/CPI_report_origin.xlsx). The original data consisted of the monthly CPI values from January 1913 to December 2023.

The life expectancy data that was used for the retirement calculator came from the [Social Security Program](https://www.ssa.gov/oact/HistEst/PerLifeTables/2017/PerLifeTables2017.html) and the original data can be found in the Resources folder [here](Resources/PerLifeTables_F_Alt2_TR2017.csv) and [here](/Resources/PerLifeTables_M_Alt2_TR2017.csv). The original data consisted of the predicted years left of the lifespan based on the current age and gender. 

The cost of living data that was used for the retirement calculator came from [Forbes Advisor Analysis](https://www.forbes.com/advisor/mortgages/cost-of-living-by-state/) and the original data can be found in the Resources folder as [data-FDgz9.csv](Resources/data-FDgz9.csv). The original data consisted of the average cost of living of each state in 2024.
