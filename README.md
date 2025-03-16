# air-pollution-asthma-analysis
Analysis of air pollution and asthma rates in the U.S.

### Project Overview
This project explores the relationship between air pollution and asthma, focusing on how environmental factors like PM2.5, O₃, and NO₂ impact respiratory health. The goal is to analyze air quality data, identify key pollutants, and assess their correlation with asthma-related health outcomes.


# Objective:
Analyze the relationship between air quality and asthma rates in various regions using public datasets:
1. This data will be useful for examining air pollution levels across different regions in U.S.: https://aqs.epa.gov/aqsweb/airdata/download_files.html
2. This dataset allows us to correlate asthma incidents with air pollution levels across different states in the U.S: https://www.cdc.gov/asthma/nhis/2021/data.htm 

# Steps:
1. Collect and preprocess data from sources like CDC, and EPA.
2. Conduct exploratory data analysis (EDA) to identify trends.
3. Perform correlation analysis to assess relationships between pollutants and asthma prevalence.
4. Build predictive models using machine learning techniques such as regression, random forest etc.
5. Visualize findings using QGIS for mapping and Tableau for trend analysis.

# Exploratory Data Analysis 

# 1. State-Level Asthma Rate Analysis 

![image](https://github.com/user-attachments/assets/a3fefdf2-61ae-4fef-a94b-fa0b6abc4f0f)

# 2. Average day with PM 2.0 per state. 

![image](https://github.com/user-attachments/assets/220a0241-d32d-4fa6-9436-8e5c6c11f99f)

# 3. Correlation Between Pollution and Health Metrics

To better understand the relationship between air pollution and health outcomes, we conducted a correlation analysis between various pollution metrics and health-related indicators. The following correlation matrix shows the relationships between different air quality metrics (e.g., PM2.5, PM10, Ozone, NO₂) and health-related metrics (e.g., Unhealthy Days, Very Unhealthy Days, Hazardous Days). 

Correlation Matrix: Pollution and Health Metrics

![image](https://github.com/user-attachments/assets/1ea84ac4-007c-4eed-9d8a-f499c4d85f28)

**Insights from the Correlation Matrix**
- **PM2.5 and Ozone**: There is a strong negative correlation (-0.74) between PM2.5 and Ozone levels. This suggests that when PM2.5 levels are high, Ozone levels tend to be low, and vice versa. This could be due to different environmental conditions that favor the formation of one pollutant over the other.
- **PM2.5 and Unhealthy Days**: There is a weak positive correlation (0.11) between PM2.5 levels and Unhealthy Days. This indicates that higher PM2.5 levels may slightly increase the number of unhealthy air quality days, but the relationship is not very strong.
- **Ozone and Unhealthy Days**: There is a weak negative correlation (-0.04) between Ozone levels and Unhealthy Days. This suggests that Ozone levels do not have a significant impact on the number of unhealthy days.
- **NO₂ and Health Metrics**: NO₂ shows very weak correlations with all health metrics, indicating that it may not be a major driver of unhealthy air quality days in this dataset.
- **Unhealthy Days and Very Unhealthy Days**: There is a moderate positive correlation (0.62) between Unhealthy Days and Very Unhealthy Days. This suggests that regions with more unhealthy days are also likely to experience more very unhealthy days.
- **Hazardous Days**: Hazardous Days show weak correlations with other metrics, indicating that they may be influenced by factors not captured in this dataset.


**Implications of the Correlation Analysis**
- **PM2.5 and Ozone**: The strong negative correlation between PM2.5 and Ozone suggests that these pollutants may have different sources or formation mechanisms. This could have implications for air quality management strategies, as reducing one pollutant may not necessarily lead to a reduction in the other.
- **Unhealthy Days**: The moderate correlation between Unhealthy Days and Very Unhealthy Days highlights the importance of addressing air quality issues before they escalate to more severe levels.
- **NO₂**: The weak correlations involving NO₂ suggest that it may not be a primary concern in this dataset, but further analysis is needed to confirm this finding.

### 4. Feature Importance for Predicting Unhealthy Days

After analyzing the correlations between pollution metrics and health outcomes, we built a predictive model to identify which air quality features are most important in predicting the number of **Unhealthy Days**. The following graph shows the **feature importance scores** for each pollutant (e.g., PM2.5, PM10, Ozone, NO₂) in predicting unhealthy days. This helps us understand which pollutants have the most significant impact on air quality health risks.

Graph: Feature Importance for Predicting Unhealthy Days

![image](https://github.com/user-attachments/assets/6024c3b5-c853-4293-bce5-7d6ab5a99324)

**Insights from the Feature Importance Graph**
- **PM2.5 is the Most Important Feature**: PM2.5 has the highest importance score (approximately 0.35), indicating that it is the most significant predictor of unhealthy days. This aligns with previous findings that PM2.5 is a major contributor to poor air quality and respiratory health issues.
- **Ozone is the Second Most Important Feature**: Ozone has the second-highest importance score (approximately 0.25), suggesting that it also plays a significant role in predicting unhealthy days. This is consistent with the known health risks associated with high ozone levels.
- **PM10 and NO₂ Have Lower Importance**: PM10 and NO₂ have relatively low importance scores (approximately 0.10 and 0.05, respectively). This suggests that while they may contribute to air pollution, they are less significant in predicting unhealthy days compared to PM2.5 and Ozone.

---

**Implications of the Feature Importance Analysis**
- **PM2.5 and Ozone are Key Pollutants**: The high importance scores for PM2.5 and Ozone highlight the need for targeted air quality interventions to reduce these pollutants, as they are the primary drivers of unhealthy air quality days.
- **PM10 and NO₂ May Require Further Investigation**: While PM10 and NO₂ have lower importance scores, they should not be ignored. Further analysis is needed to understand their role in specific regions or under certain conditions.
- **Policy Recommendations**: The findings suggest that public health policies should prioritize reducing PM2.5 and Ozone levels to minimize the number of unhealthy air quality days and protect respiratory health.

### Predictive Modeling

# Model Evaluation: Linear Regression and Random Forest

To predict asthma rates based on air quality data, we built and evaluated two machine learning models: **Linear Regression** and **Random Forest**. The following results show the performance of these models, including the **R² (coefficient of determination)** and **RMSE (Root Mean Squared Error)** metrics. These metrics help us assess how well the models predict asthma rates based on pollution data.

**Graph: Actual vs Predicted Asthma Rates (Linear Regression and Random Forest)**

![image](https://github.com/user-attachments/assets/10abbf90-759f-49a5-899d-1ae19bee5076)

**Insights from the Model Evaluation**
- **Linear Regression Performance**:
  - The Linear Regression model achieved an **R² of 0.80** and an **RMSE of 11.81**. This indicates that the model explains 80% of the variance in asthma rates and has a moderate prediction error.
  - While the model performs well, there is still room for improvement, as the RMSE suggests some deviation between the actual and predicted asthma rates.

- **Random Forest Performance**:
  - The Random Forest model outperformed Linear Regression, achieving an **R² of 0.92** and an **RMSE of 7.58**. This indicates that the model explains 92% of the variance in asthma rates and has a lower prediction error compared to Linear Regression.
  - The Random Forest model captures more complex, non-linear relationships between air quality metrics and asthma rates, leading to better predictive accuracy.

- **Comparison of Models**:
  - The Random Forest model is significantly more accurate than the Linear Regression model, as evidenced by the higher R² and lower RMSE.
  - This suggests that asthma rates are influenced by complex interactions between pollutants, which are better captured by ensemble methods like Random Forest.

---

**Implications of the Model Evaluation**
- **Random Forest is the Preferred Model**: Given its superior performance, the Random Forest model is better suited for predicting asthma rates based on air quality data.
- **Non-Linear Relationships**: The success of Random Forest highlights the importance of capturing non-linear relationships between pollutants and health outcomes, which may not be adequately modeled by simpler linear approaches.
- **Policy and Public Health Applications**: The high accuracy of the Random Forest model makes it a valuable tool for predicting asthma risks in different regions, which can inform targeted public health interventions and air quality regulations.


### Model Performance Comparison

To identify the best-performing model for predicting asthma rates based on air quality data, we evaluated several machine learning models, including **Gradient Boosting**, **Random Forest**, **Support Vector Regression (SVR)**, **K-Nearest Neighbors (KNN)**, **Neural Network**, and **XGBoost**. The following table summarizes the performance of these models using **RMSE (Root Mean Squared Error)** and **R² (coefficient of determination)** metrics.

**Table: Model Performance Comparison**
![image](https://github.com/user-attachments/assets/d99fdcb9-d9c9-406d-824f-38c28c3aae86)

#### Insights from the Model Performance Table
- **Gradient Boosting is the Best-Performing Model**: Gradient Boosting achieved the lowest RMSE (0.749) and the highest R² (0.999), making it the most accurate model for predicting asthma rates. This indicates that Gradient Boosting effectively captures the complex relationships between air quality metrics and asthma rates.
- **Random Forest and XGBoost Also Perform Well**: Random Forest and XGBoost also showed strong performance, with R² values close to 1 and relatively low RMSE scores (1.097 and 1.905, respectively). These models are robust alternatives to Gradient Boosting.
- **Neural Network Performs Moderately Well**: The Neural Network achieved an R² of 0.962 and an RMSE of 14.620, indicating decent performance but not as strong as Gradient Boosting or Random Forest.
- **K-Nearest Neighbors (KNN) Shows Limited Performance**: KNN achieved an R² of 0.772 and an RMSE of 35.590, suggesting that it is less effective at capturing the relationships in this dataset.
- **Support Vector Regression (SVR) Performs Poorly**: SVR had the worst performance, with an R² of -0.003 and a very high RMSE of 74.690. This indicates that SVR is not suitable for this type of regression task.

---

### Implications of the Model Performance Comparison
- **Gradient Boosting is the Preferred Model**: Given its superior performance, Gradient Boosting is the best choice for predicting asthma rates based on air quality data. Its high accuracy makes it a valuable tool for public health applications.
- **Ensemble Methods Outperform Other Models**: The strong performance of Gradient Boosting, Random Forest, and XGBoost highlights the effectiveness of ensemble methods in capturing complex, non-linear relationships in the data.
- **SVR and KNN Are Not Suitable**: The poor performance of SVR and KNN suggests that these models are not well-suited for this type of regression task, likely due to the complexity of the relationships between air quality metrics and asthma rates.

### Seasonal Trends in Pollution and Health Metrics

To understand how air quality and health metrics vary across different seasons, we analyzed the average levels of pollutants (e.g., PM2.5, PM10, Ozone, NO₂) and health-related metrics (e.g., Unhealthy Days, Very Unhealthy Days, Hazardous Days) over time. The following graph shows the seasonal trends in pollution and health metrics, highlighting how these factors change throughout the year.

**Graph: Seasonal Trends in Pollution and Health Metrics**

![image](https://github.com/user-attachments/assets/ca0dc957-d93f-492b-a2ac-eb530d7fd9d8)

#### Insights from the Seasonal Trends Graph
- **PM2.5 and PM10 Levels**:
  - PM2.5 and PM10 levels tend to peak during **Winter1** and **Winter2**, likely due to increased use of heating systems, reduced air circulation, and temperature inversions that trap pollutants close to the ground.
  - These levels drop during **Spring** and **Autumn**, possibly due to better air circulation and lower emissions from heating sources.

- **Ozone Levels**:
  - Ozone levels are highest during **Summer**, which is consistent with the formation of ground-level ozone in hot, sunny conditions. This is a common trend in urban areas with high traffic emissions.
  - Ozone levels are lowest during **Winter**, as cold temperatures and shorter daylight hours reduce the chemical reactions that produce ozone.

- **NO₂ Levels**:
  - NO₂ levels remain relatively stable across seasons, with slight increases during **Winter** due to higher emissions from heating and transportation.

- **Unhealthy, Very Unhealthy, and Hazardous Days**:
  - The number of **Unhealthy Days** and **Very Unhealthy Days** peaks during **Summer**, coinciding with high ozone levels.
  - **Hazardous Days** are more frequent during **Winter**, likely due to elevated PM2.5 and PM10 levels.

---

### Implications of the Seasonal Trends Analysis
- **Seasonal Variations in Pollution**: The graph highlights significant seasonal variations in pollution levels, with PM2.5 and PM10 peaking in winter and ozone peaking in summer. This suggests that air quality management strategies should be tailored to address seasonal pollution patterns.
- **Health Risks**: The increase in unhealthy and hazardous days during specific seasons underscores the need for targeted public health interventions during high-risk periods, such as winter and summer.
- **Policy Recommendations**: Policymakers should consider seasonal trends when designing air quality regulations and public health campaigns to mitigate the impact of pollution on respiratory health.


### Results and Discussion
1. **Key Findings**:
   - Elevated PM2.5 and Ozone levels were strongly associated with increased asthma rates.
   - Gradient Boosting achieved near-perfect predictive accuracy (R² = 0.9999).
   - Geographic disparities in air quality and asthma rates were observed.
2. **Public Health Implications**:
   - The findings emphasize the need for stricter air quality regulations in high-risk areas.
3. **Model Effectiveness**:
   - Gradient Boosting demonstrated the potential of machine learning models in public health risk assessments.
4. **Limitations**:
   - Data gaps for certain regions and the lack of longitudinal data may have limited the scope of our analysis.

### References
- World Health Organization. (2022). Air quality database: Update 2022. [Link](https://www.who.int/data/gho/data/themes/air-pollution)
- Centers for Disease Control and Prevention. (2021). Asthma data and surveillance: National Health Interview Survey (NHIS) 2021. [Link](https://www.cdc.gov/asthma/nhis/2021)
- Environmental Protection Agency. (2021). Air quality system (AQS): Outdoor air quality data. [Link](https://www.epa.gov/outdoor-air-quality-data)
