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

# Insights from the Correlation Matrix
- **PM2.5 and Ozone**: There is a strong negative correlation (-0.74) between PM2.5 and Ozone levels. This suggests that when PM2.5 levels are high, Ozone levels tend to be low, and vice versa. This could be due to different environmental conditions that favor the formation of one pollutant over the other.
- **PM2.5 and Unhealthy Days**: There is a weak positive correlation (0.11) between PM2.5 levels and Unhealthy Days. This indicates that higher PM2.5 levels may slightly increase the number of unhealthy air quality days, but the relationship is not very strong.
- **Ozone and Unhealthy Days**: There is a weak negative correlation (-0.04) between Ozone levels and Unhealthy Days. This suggests that Ozone levels do not have a significant impact on the number of unhealthy days.
- **NO₂ and Health Metrics**: NO₂ shows very weak correlations with all health metrics, indicating that it may not be a major driver of unhealthy air quality days in this dataset.
- **Unhealthy Days and Very Unhealthy Days**: There is a moderate positive correlation (0.62) between Unhealthy Days and Very Unhealthy Days. This suggests that regions with more unhealthy days are also likely to experience more very unhealthy days.
- **Hazardous Days**: Hazardous Days show weak correlations with other metrics, indicating that they may be influenced by factors not captured in this dataset.


# Implications of the Correlation Analysis
- **PM2.5 and Ozone**: The strong negative correlation between PM2.5 and Ozone suggests that these pollutants may have different sources or formation mechanisms. This could have implications for air quality management strategies, as reducing one pollutant may not necessarily lead to a reduction in the other.
- **Unhealthy Days**: The moderate correlation between Unhealthy Days and Very Unhealthy Days highlights the importance of addressing air quality issues before they escalate to more severe levels.
- **NO₂**: The weak correlations involving NO₂ suggest that it may not be a primary concern in this dataset, but further analysis is needed to confirm this finding.


![image](https://github.com/user-attachments/assets/6024c3b5-c853-4293-bce5-7d6ab5a99324)

![image](https://github.com/user-attachments/assets/10abbf90-759f-49a5-899d-1ae19bee5076)

![image](https://github.com/user-attachments/assets/d99fdcb9-d9c9-406d-824f-38c28c3aae86)

![image](https://github.com/user-attachments/assets/ca0dc957-d93f-492b-a2ac-eb530d7fd9d8)

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
