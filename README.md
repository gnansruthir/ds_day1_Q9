# Hospital Weather Impact Analysis

## Project Title
Hospital — Does Weather Affect Patient Arrivals?

## Overview
This project investigates whether weather conditions have a meaningful impact on daily patient arrivals at a hospital. The objective is to determine whether changes in temperature, rainfall, humidity, and air quality are associated with fluctuations in outpatient and emergency patient counts.

The analysis combines healthcare and environmental data to explore seasonal patterns, department sensitivity, and statistical relationships. A Linear Regression model is also trained and evaluated to assess whether weather variables can be used to predict patient volumes.

## Business Problem
A hospital observes that patient arrivals appear to rise during certain weather conditions, especially during periods of heavy rainfall, high humidity, and poor air quality. Management wants to know whether this pattern is real or simply anecdotal.

This project tests the hypothesis that weather significantly affects hospital patient arrivals and uses data-driven evidence to support or refute that claim.

## Dataset
The dataset used in this project contains two years of daily hospital data and is stored in:

- `hospital_weather_data.csv`

### Columns
- `Date`
- `Department`
- `Outpatient_Count`
- `Emergency_Count`
- `Temperature`
- `Rainfall`
- `Humidity`
- `Air_Quality`

### Dataset Characteristics
- 180 rows
- 8 columns
- no missing values
- daily records covering multiple departments and weather conditions

## Objectives
1. Clean and validate the dataset
2. Perform exploratory data analysis
3. Identify important weather-health relationships
4. Examine seasonal trends in patient arrivals
5. Compare patient volumes across weather conditions
6. Determine department sensitivity to environmental stress
7. Train and evaluate a Linear Regression model
8. Provide practical recommendations for hospital management

## Methodology
The project followed a structured data science workflow:

1. Data Loading and Validation
   - Loaded the dataset
   - Converted the `Date` column to datetime format
   - Checked missing values and data types

2. Exploratory Data Analysis (EDA)
   - Reviewed descriptive statistics
   - Compared outpatient and emergency counts by department
   - Analyzed correlations between weather variables and patient demand

3. Seasonal Analysis
   - Grouped data by season
   - Identified differences in patient arrival patterns across the year

4. Feature Engineering
   - Created weather category variables
   - Built a `Total_Patient_Count` feature
   - Constructed a `Weather_Severity` metric to summarize environmental stress

5. Visualization
   - Created seasonal trend plots
   - Compared departments visually
   - Developed scatter plots and a heatmap to highlight weather impact

6. Statistical Testing
   - Pearson correlation analysis
   - ANOVA for temperature categories
   - t-test for high vs low rainfall conditions

7. Machine Learning
   - Built a Linear Regression model
   - Used standardized features and department dummy variables
   - Evaluated performance using R², RMSE, and MAE

## Key Findings
### 1. Rainfall strongly affects emergency demand
The analysis showed that days with higher rainfall had significantly more emergency visits than days with lower rainfall. This suggests that adverse weather conditions trigger more emergency healthcare demand.

### 2. Monsoon conditions create the highest pressure on hospital services
Seasonal analysis showed that Monsoon periods had the highest average emergency arrival counts. This indicates that heavy rainfall and humid weather strongly affect healthcare demand.

### 3. Respiratory cases are highly weather-sensitive
The department analysis showed that Respiratory patients were the most sensitive to weather-related fluctuations. This is consistent with the idea that changes in air quality and humidity can worsen respiratory symptoms.

### 4. Humidity and air quality are important drivers
The correlation analysis showed meaningful relationships between humidity, air quality, and patient volume. Poorer air quality and higher humidity were associated with greater healthcare demand.

### 5. Temperature differences also matter
Temperature categories showed statistically significant differences in emergency counts, suggesting that hospital demand varies across warm, hot, and extreme weather conditions.

### 6. Weather matters statistically, not just visually
The statistical tests produced significant p-values, confirming that the observed relationships are not random and are statistically meaningful.

### 7. The model provides a practical forecasting baseline
The trained Linear Regression model produced a usable prediction baseline, although the fit is moderate rather than extremely strong. This is expected in real healthcare datasets, where many non-weather factors also influence hospital visits.

## Statistical Evidence
### Correlation Results
- Rainfall vs total patient arrivals: moderate positive relationship
- Humidity vs total patient arrivals: moderate positive relationship
- Air quality vs total patient arrivals: moderate negative relationship
- Temperature vs total patient arrivals: positive but weaker relationship

### Hypothesis Tests
- ANOVA for temperature categories: statistically significant
- t-test for high vs low rainfall: highly significant

These findings support the claim that weather has a meaningful impact on hospital demand.

## Linear Regression Model
A Linear Regression model was used to predict total patient count using weather variables and department categories.

### Model Features
- Temperature
- Rainfall
- Humidity
- Air_Quality
- Department dummy variables

### Model Evaluation
The model produced the following performance metrics:

- Test R²: 0.3099
- Test RMSE: 10.4218
- Test MAE: 7.7854

### Interpretation
Although the model is not highly accurate, it still provides a useful operational baseline. In real healthcare scenarios, patient arrivals are affected by many factors beyond weather, including disease outbreaks, hospital policies, patient behavior, and resource availability. The model is therefore useful as a planning tool rather than a perfect prediction engine.

## Business Recommendations
1. Increase emergency and respiratory staffing during monsoon and high-rainfall periods.
2. Prepare additional emergency supplies before weather stress events.
3. Monitor air-quality conditions closely, especially for respiratory patients.
4. Use forecast-based scheduling for high-risk departments.
5. Communicate weather-related health guidance to vulnerable patients.

## Conclusion
The results show that weather conditions significantly influence hospital patient arrivals. Rainfall, humidity, and air quality appear to be meaningful predictors of healthcare demand, particularly in emergency and respiratory services. The project provides evidence that weather should be incorporated into operational forecasting and hospital staffing strategies.

## Repository Structure
- `hospital_weather_data.csv` — source dataset
- `hospital_weather_analysis.ipynb` — notebook implementation
- `README.md` — project documentation



## Final Note
This project demonstrates how data analysis, statistical testing, and machine learning can be applied to a real healthcare challenge. The results provide evidence-based insight into how environmental conditions influence patient demand and highlight the importance of weather-aware hospital planning.
