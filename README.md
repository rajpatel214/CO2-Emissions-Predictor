# CO2-Emissions-Predictor

### **CO2 Emissions Predictor – Project Explanation**  

#### **Objective**  
The goal of this project is to develop a machine learning model that predicts CO2 emissions (in kilotons) based on various energy consumption and economic indicators. The dataset includes factors like access to electricity, renewable energy generation, GDP growth, and fossil fuel-based power consumption. By analyzing these variables, the model aims to estimate CO2 emissions for different years and regions.  

#### **Dataset Overview**  
The dataset consists of energy and sustainability-related features, such as:  
- **Energy production** (fossil fuel, nuclear, and renewable sources)  
- **Energy consumption metrics** (primary energy consumption, energy intensity)  
- **Economic indicators** (GDP growth)  
- **Geographical influence** (latitude)  
- **Electricity access and usage patterns**  

Missing values in critical variables like "Access to electricity" were handled by imputing the median value.  

#### **Feature Selection & Preprocessing**  
The selected features were used to build the predictive model:  
- **Independent Variables (X)**: All features except the target variable  
- **Target Variable (Y)**: CO2 emissions (Value_co2_emissions_kt_by_country)  

The dataset was split into training (80%) and testing (20%) subsets. To ensure stability and reduce the impact of outliers, the RobustScaler technique was applied for feature scaling.  

#### **Model Selection & Performance**  
Several regression models were tested to predict CO2 emissions:  

1. **Stacking Regressor** – A combination of Random Forest, K-Nearest Neighbors, and Decision Tree models, with Linear Regression as the final estimator.  
   - Achieved an accuracy score of **96%**  

2. **Bagging Regressor** – An ensemble technique using multiple Decision Tree Regressors to reduce variance and improve stability.  
   - Achieved an accuracy score of **96%**  

3. **AdaBoost Regressor** – An adaptive boosting technique using Decision Trees with a maximum depth of 20.  
   - Achieved an accuracy score of **97%** (best-performing model)  

4. **Gradient Boosting Regressor** – A boosting technique that optimizes error correction iteratively.  
   - Achieved an accuracy score of **96%**  

#### **Final Conclusion**  
The **AdaBoost Regressor** performed the best, achieving **97% accuracy** in predicting CO2 emissions. The model effectively captures the relationship between energy production, consumption, and CO2 emissions. These insights can help policymakers and researchers analyze the impact of energy usage on climate change and develop sustainable energy policies.
