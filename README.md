# ML Predictions

## Overview
This Python script focuses on making machine learning predictions based on health data, specifically medication and mood patterns. The predictions aim to provide insights into future medication adherence, mood changes, and potential doctor visits.

## Usage
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

1. Open the Jupyter Notebook:
   ```bash
   jupyter notebook predictions.ipynb
   ```
## Functionalities
The ML predictions script performs the following tasks:
- Predicts the probability of future medication misses.
- Analyzes mood patterns before and after medication intake.
- Differentiates between multi-medication and single-medication data.
- Predicts future medication events for individual users.
- Handles missing data and predicts medication intake based on historical patterns.
- Identifies weeks with low mood probability or high medication miss likelihood.
- Predicts mood changes for continuous medication misses or adherence.

## Dependencies
- Python (>=3.6)
- Libraries listed in `requirements.txt`

# Approach Overview

## Data Understanding
1. **Initial Inspection:** Started with a basic exploration and visualization of the dataset to understand the data distribution and relationships between the features and the target variables (Mood and Medication Adherence).
2. **Data Cleaning:** Handled missing values and converted date fields into a recognizable format.

## Feature Engineering
3. **Creating Additional Features:** Extracted day and month from the date to capture potential seasonality effects on mood and medication adherence.

## Data Preparation
4. **Data Splitting:** Split the dataset into training and testing sets to evaluate the performance of the models.

## Model Selection and Rationale: Random Forest Regressor
**Why Chosen:**
Random Forest was chosen for both mood and medication adherence prediction tasks. It is a versatile and robust algorithm that can capture complex relationships and interactions between features. It also provides good performance with default parameters, reducing the need for extensive hyperparameter tuning.

### Approach for Prediction
- Used historical data (date, medication adherence) to predict the mood.
- For medication adherence prediction, used date and mood as features.

## Model Training
Trained the Random Forest models on the training data for both tasks (mood and medication adherence prediction).

## Model Evaluation
Evaluated the models using relevant metrics (Mean Squared Error, Root Mean Squared Error, and Mean Absolute Error) to ensure the models were performing adequately.

## Prediction Approach
1. **Mood Prediction on Days with Missed Medication:**
   Identified days with missed medication and used the model to predict the mood on these days.
2. **Medication Adherence Prediction:**
   Used the model to predict medication adherence for future dates, helping to identify potential medication misses in advance.
3. **Analysis of Mood and Medication Adherence:**
   Analyzed patterns and trends in mood and medication adherence data.
   Identified potential side effects by observing unusually low moods after days with high medication adherence.

## Thinking and Approach for Predictions
- **Understanding the Problem Context:**
   Before diving into predictions, understanding the real-world implications and context of the problem is crucial. It ensures that the model and predictions are aligned with the objective of improving patient well-being.
- **Choosing the Right Model:**
   Selected a model that could handle both numerical and categorical data, manage missing values, and provide robust predictions with a balanced bias-variance trade-off (Random Forest).
- **Evaluating Model Performance:**
   Ensured to evaluate and validate the model’s performance rigorously to guarantee reliable predictions.
- **Interpreting the Results:**
   Interpreted the predictions and analysis results to extract actionable insights and recommendations, considering the healthcare context.

## Conclusion
The approach was holistic, starting from data understanding to model selection, prediction, and interpretation. The choice of the Random Forest algorithm ensured robustness and reliability in predictions, aligning with the goal of analyzing and predicting mood and medication adherence effectively. The interpretations and insights derived from the predictions aimed to contribute positively to healthcare outcomes, providing valuable information for patients and healthcare providers.


## Customization
You can customize the script by modifying parameters and classifiers based on your specific requirements. Further improvements and adjustments can be made to enhance prediction accuracy.

## Future Integrations
- Exploration of options to integrate the machine learning model with the main application.
- Continuous improvement and updates to enhance user experience.
- Predict user semtiment by doing analysis from the notes user written.

Feel free to explore, contribute, and adapt this script to better suit your needs. If you have any questions or suggestions, please reach out to ro93939@gmail.com, ruthvikroychekka@gmail.com, hemanth2198@gmail.com, uday.kadam201@gmail.com.

Happy predicting! 🤖
