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

![image](https://github.com/user-attachments/assets/90a364fc-6e33-4d1d-b1c9-b66c69ad622e)

![image](https://github.com/user-attachments/assets/1ea84ac4-007c-4eed-9d8a-f499c4d85f28)

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
