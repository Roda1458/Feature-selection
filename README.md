# Feature Selection Project

This project focuses on applying various **feature selection techniques** to two datasets: the **Diabetes Dataset** and the **Melbourne Housing Dataset**. The aim is to enhance model performance by selecting the most relevant features while reducing the dataset's size.

## Datasets Used:
- **Diabetes Dataset:** Used to predict diabetes outcomes.
- **Melbourne Housing Dataset:** Used to predict housing prices.

---

## Feature Selection Techniques

Feature selection is the process of reducing the number of input variables when developing predictive models. This helps improve model performance by removing irrelevant or redundant features.

---

### 1. Missing Values Ratio

- **Definition:**  
  This method removes features that have a high percentage of missing values. Too many missing values can weaken the model's performance.
  
- **Diabetes Dataset:**  
  - Identify and remove features where more than 30% of the values are missing.
  - Analyze how the reduced feature set affects model accuracy in predicting diabetes outcomes.

- **Melbourne Housing Dataset:**  
  - Remove columns with more than 20% missing values.
  - Evaluate the impact of this filtering on the performance of the price prediction model.

---

### 2. High Correlation Filter

- **Definition:**  
  Highly correlated features provide similar information to the model, leading to redundancy. This method removes one of the features from highly correlated pairs.

- **Diabetes Dataset:**  
  - Identify pairs of features with a correlation greater than 0.8.
  - Remove one feature from each highly correlated pair and assess changes in diabetes classification accuracy.

- **Melbourne Housing Dataset:**  
  - Filter out features with a correlation greater than 0.85.
  - Evaluate how removing these features affects the accuracy of the price prediction model.

---

### 3. Low Variance Filter

- **Definition:**  
  Features with very little variation don't contribute much to model predictions. This method removes features with low variability.

- **Diabetes Dataset:**  
  - Remove features with low variance (i.e., features that don’t vary much across samples).
  - Observe the effect of this filtering on diabetes prediction accuracy.

- **Melbourne Housing Dataset:**  
  - Remove features with low variance (almost constant across samples).
  - Assess the impact on housing price predictions.

---

### 4. Forward Feature Selection

- **Definition:**  
  Forward feature selection is an iterative method that starts with no features and adds them one by one. The feature that improves the model the most at each step is added.

- **Diabetes Dataset:**  
  - Use forward feature selection with a logistic regression model.
  - Determine the optimal number of features for predicting diabetes outcomes.

- **Melbourne Housing Dataset:**  
  - Apply forward feature selection to find the best features for predicting housing prices using a linear regression model.

---

### 5. Backward Feature Elimination

- **Definition:**  
  Backward feature elimination starts with all features and removes the least important ones step by step, stopping when further removals reduce model performance.

- **Diabetes Dataset:**  
  - Perform backward feature elimination using a decision tree classifier.
  - Examine how removing the least important features one by one affects model performance.

- **Melbourne Housing Dataset:**  
  - Use backward feature elimination with a random forest model.
  - Analyze how removing the least important features impacts the price prediction accuracy.

---

### 6. Random Forest (Feature Importance)

- **Definition:**  
  Random Forests provide an importance score for each feature based on how much they contribute to reducing uncertainty in decision trees. The least important features can then be removed.

- **Diabetes Dataset:**  
  - Rank the features based on importance scores from a random forest model.
  - Keep only the top 5 most important features and evaluate the reduced model's accuracy.

- **Melbourne Housing Dataset:**  
  - Train a random forest model to determine the most important features for predicting housing prices.
  - Assess how removing the least important features affects model performance.

---

## Conclusion

This project demonstrates the use of several feature selection techniques, including:
- **Missing Values Ratio**: Removing features with many missing values.
- **High Correlation Filter**: Eliminating redundant features.
- **Low Variance Filter**: Removing features with little variation.
- **Forward Feature Selection**: Adding features that improve the model step by step.
- **Backward Feature Elimination**: Removing the least important features one by one.
- **Random Forest (Feature Importance)**: Ranking features by their contribution to model accuracy.
