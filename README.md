# 🎮 Player Performance Prediction Model  

## Overview  
This project builds a **Random Forest Regression** model in Python to predict how long players take to complete a video game level.  
The model uses gameplay features **ammo usage** and **level difficulty** to estimate **completion time**.  

## Business Application  
- **Player Engagement:** Turn predictions into real-time challenges (e.g., “Our model predicts you’ll finish in 98s — can you beat it?”).  
- **Personalized Guidance:** Help players choose levels based on estimated completion time.  
- **Game Design Insights:** Provide developers with feedback on whether levels are too easy, too hard, or unbalanced.  

## Tech Stack  
- **Language:** Python  
- **Libraries:** pandas, scikit-learn (RandomForestRegressor, train_test_split, r2_score)  
- **Environment:** Jupyter Notebook  

## Implementation Steps  
1. **Data Preparation:**  
   - Removed the target column (`completion_time`) from the feature set.  
   - Split dataset into training (80%) and test (20%) sets.  

2. **Model Training:**  
   - Used `RandomForestRegressor` with a fixed random state for reproducibility.  
   - Trained on the training dataset and generated predictions on the test set.  

3. **Evaluation:**  
   - Compared predictions with actual values using **R² score**.  
   - Created a DataFrame to visualize actual vs predicted times.  

## Recommendations for Improvement  
- **Data Quality & Preparation:** Ensure the dataset is fully cleaned and validated to avoid biased inputs.
- **Feature Engineering:** consider additional features (e.g., player skill history, weapon type, or map layout) to strengthen predictive power.
- **Model Selection & Tuning:** Test alternative regression algorithms and optimise hyperparameters.
- **Deployment Considerations:** Package the model into a production-ready environment capable of receiving live player data and returning predictions in real time.
