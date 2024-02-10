# Life-expectancy-
The World Health Organization (WHO)'s Global Health Observatory (GHO) data repository monitors each nation's health status as well as several other relevant variables. For the goal of analyzing health data, the datasets are made available to the public. The same WHO data repository website served as the source for the dataset relating to life expectancy, health factors for 193 nations, and its corresponding economic statistics. In this effort, we used data from 193 nations from 2000 to 2015 for analysis.
Source: https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who
•	Country: Country
•	Year: Year
•	Status: Classification of countries as 'developed' or 'developing' based on their gross domestic product (GDP).11
•	Life expectancy: Life expectancy (years of age).
•	Adult Mortality: Adult Mortality Rates of both sexes (Probability of dying between 15 and 60 years per 1000 population).
•	Infant deaths: Number of Infant (0-1 year of age) Deaths per 1000 population.
•	Alcohol: Alcohol, recorded per capita (15+) consumption (in liters of pure alcohol).
•	Percentage expenditure: Expenditure on health as a percentage of GPD per capita. (%)
•	Hepatitis B: Hepatitis B immunization coverage among 1-year-olds. (%)
•	Measles: Number of reported cases per 1000 population.
•	BMI: Average Body Mass index of entire population
•	Under-five deaths: Number of under-five deaths per 1000 population
•	Polio: Polio immunization coverage among 1-year-olds (%)
•	Total expenditure: General government expenditure on health as a percentage of total government expenditure (%)
•	Diphtheria: Diphtheria tetanus toxoid and pertussis (DTP3) immunization coverage among 1-year-olds (%)
•	HIV/AIDS: Deaths per 1000 live births HIV/AIDS (0-4 years)
•	GDP: Gross Domestic Product per capita (in USD)
•	Population: Population of the country
•	Thinness 1-19 years: Prevalence of thinness among children and adolescents for Age 10 to 19 (%)22
•	Thinness 5-9 years: Prevalence of thinness among children for Age 5 to 9 (%)
•	Income composition of resources: Human Development Index in terms of income composition of resources (index ranging from 0 to 1)
•	Schooling: Number of years of Schooling (years)

	1.3 Proposed Analytics Solution
The goal is to determine and predict the life expectancy of a country based on the other provided metrics, as well as to identify which ones have the greatest impact on life expectancy.
Data Collection and Cleaning:
•	Gather a comprehensive dataset that includes metrics such as healthcare expenditure, GDP, education levels, sanitation and other relevant socio-economic factors.
•	Clean the dataset to handle missing values, outliers, and inconsistencies.
Exploratory Data Analysis (EDA):
•	Conduct exploratory data analysis to understand the distribution and relationships among different variables.
•	Use visualizations like scatter plots, correlation matrices, and histograms to identify potential patterns and outliers.
Feature Engineering:
•	Identify key features that might have a significant impact on life expectancy.
•	Create new features if necessary, such as a combined socio-economic index, to capture the overall well-being of a country.
Correlation Analysis:
•	Quantify the correlation between each feature and life expectancy.
•	Rank features based on their correlation coefficients to identify the most influential factors.
Machine Learning Model Selection:
•	Choose appropriate machine learning models for prediction, such as linear regression, decision trees, or ensemble methods.
•	Split the dataset into training and testing sets to evaluate model performance.
Model Training and Validation:
•	Train the selected models on the training set and validate their performance on the testing set.
•	Use techniques like cross-validation to ensure robustness and avoid overfitting.
Interpretability and Visualization:
•	Develop visualizations to communicate the model's predictions and feature importance to stakeholders.
•	Provide insights into how changes in specific metrics can affect life expectancy.
Continuous Monitoring and Updating:
•	Implement a system for continuous monitoring of the model's performance.
•	Periodically update the model with new data to ensure its relevance and accuracy.
Deployment:
•	Deploy the analytics solution in a scalable and accessible manner.
 
	2 Data Exploration and Preprocessing
2.1 Data Quality Report
Table 1. Data Quality Report for Categorical Features
 
 
 
Table 2. Data Quality Report for Continuous Features
 

Life Expectancy:
•	The distribution of life expectancy is centered around the mean of approximately 69.22 years.
•	There is relatively low variability, with a standard deviation of 9.52.
•	The minimum life expectancy is 36.30 years, and the maximum is 89.00 years.
•	The dataset is slightly right-skewed, as the mean is less than the median (Q2).
Adult Mortality:
•	Adult mortality exhibits higher variability, as seen in the wide range from 1 to 723.
•	The mean adult mortality rate is 164.80, with a standard deviation of 124.29.
•	There are potential outliers or extreme values, as indicated by the large standard deviation.
Infant Deaths:
•	The distribution of infant deaths is positively skewed, with a mean of 30.30 and a maximum of 1800.
•	While the majority of entries have low infant death counts, there are instances with significantly higher values. 
Alcohol Consumption:
•	Alcohol consumption is positively skewed, with a mean of 4.60 and a maximum of 17.87.
•	The distribution is right-tailed, indicating that a few countries might have high alcohol consumption.
Percentage Expenditure:
•	The percentage expenditure varies widely, as evidenced by the high standard deviation.
•	Some entries may have exceptionally high percentage expenditure values, contributing to the variability.
Hepatitis B:
•	Hepatitis B vaccination coverage shows missing values, impacting the count and completeness of the dataset.
Measles:
•	Measles data is right-skewed, with a mean much lower than the maximum, indicating potential outliers.
BMI (Body Mass Index):
•	BMI distribution spans from 1 to 87.3, with a mean of 38.32 and moderate variability.
•	There are some missing values in the BMI variable.
Under-Five Deaths:
•	Similar to infant deaths, under-five deaths exhibit a positively skewed distribution with some higher values.
Polio:
•	Polio vaccination coverage has a moderate range and shows a small percentage of missing values.
Total Expenditure:
•	Total expenditure on health has some missing values and a right-skewed distribution.
Diphtheria:
•	Diphtheria vaccination coverage is similar to polio, with moderate coverage and a small percentage of missing values.
HIV/AIDS:
•	The distribution of HIV/AIDS prevalence is right-skewed, with a mean of 1.74 and a maximum of 50.6.
GDP (Gross Domestic Product):
•	GDP varies widely, with a large standard deviation, indicating economic disparities among countries.
Population:
•	Population data has a high standard deviation, suggesting substantial differences among countries.
Thinness (1-19 years and 5-9 years):
•	Both thinness variables exhibit positively skewed distributions, indicating variations in nutritional status.
Income Composition of Resources:
•	The income composition of resources is relatively concentrated, with a mean of 0.63.
Schooling:
•	Schooling years show moderate variability, with a mean of 11.99.

