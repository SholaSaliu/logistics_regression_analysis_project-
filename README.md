# logistics_regression_analysis_project-
This project predicts airline customer satisfaction using Logistic Regression. It processes airline data, encodes features, splits data, and builds a model. Performance metrics are strong. Key drivers like inflight entertainment and disloyal customers are identified, with recommendations focusing on service and digital experience.
Airline Customer Satisfaction Prediction
Project Overview
This project aims to predict airline customer satisfaction using a Logistic Regression classification model. We analyze passenger survey data to identify key drivers of satisfaction, preprocess features, build a predictive model, and evaluate its performance. The ultimate goal is to provide actionable business recommendations to improve customer retention and satisfaction.

Dataset Summary
The dataset, Invistico_Airline.csv, contains survey responses from airline passengers, including various service ratings, demographic information, and a target variable indicating satisfaction (satisfied/dissatisfied). The dataset comprises approximately 130,000 entries with 22 features.

Modeling Approach
The following steps were undertaken to build and evaluate the Logistic Regression model:

Data Loading and Inspection: The Invistico_Airline.csv dataset was loaded into a pandas DataFrame. The distribution of the target variable (satisfaction) was inspected.
Data Preprocessing:
The target variable satisfaction was converted to a numerical format (0 for 'dissatisfied', 1 for 'satisfied').
Categorical features (Customer Type, Type of Travel, Class) were identified and one-hot encoded using pd.get_dummies.
Missing values in the Arrival Delay in Minutes column were imputed with the mean of the column.
Data Splitting: The preprocessed data was split into training (70%) and testing (30%) sets using train_test_split, ensuring stratification to maintain the original proportion of satisfaction categories in both sets.
Model Building: A Binomial Logistic Regression model from Scikit-learn (LogisticRegression) was initialized and trained on the X_train and y_train data.
Prediction: The trained model was used to make predictions (y_pred) and predict probabilities (y_pred_proba) on the X_test set.
Model Evaluation: The model's performance was evaluated using:
Confusion Matrix: To visualize the true positives, true negatives, false positives, and false negatives.
Accuracy: Overall correctness of the model.
Precision: The proportion of positive identifications that were actually correct.
Recall: The proportion of actual positives that were identified correctly.
Coefficient Interpretation: The coefficients of the Logistic Regression model were extracted and analyzed to understand the impact of each feature on customer satisfaction.
Business Recommendations: Actionable recommendations were formulated based on the interpretation of the model coefficients.
Performance Metrics
After training and evaluating the Logistic Regression model on the test set, the following performance metrics were obtained:

Accuracy: 0.8291 (82.91%)
Precision: 0.8438 (84.38%)
Recall: 0.8440 (84.40%)
Confusion Matrix:

Predicted Dissatisfied	Predicted Satisfied
Actual Dissatisfied	14307	3331
Actual Satisfied	3326	18000
Key Findings & Recommendations
Inflight Entertainment was identified as the strongest positive driver of satisfaction.
Customer Type (Disloyal Customer), Class (Eco/Eco Plus), and Type of Travel (Personal Travel) were significant negative drivers, indicating structural differences in satisfaction levels among these groups.
Recommendations include prioritizing improvements in inflight entertainment, enhancing core service quality (on-board service, check-in, seat comfort), optimizing the online experience, addressing pain points for disloyal customers, and considering segmented service improvements for different travel classes and types.
