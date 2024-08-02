# Racial-Profiling-and-Bias-Detection-in-Minneapolis-Arrest-Prediction-in-Nashville


### Project Overview
This project involves the analysis of police stops to predict the likelihood of an arrest. Using a large dataset from the Stanford Openpolicing Project, we aim to apply machine learning techniques to identify patterns and predictors of arrests during police stops.

### Objective
The primary objective is to use supervised learning methods to predict whether or not an arrest is made based on input features from police stop instances. This falls into the category of binary classification problems, with the target variable being `arrest_made`.

## Dataset Overview

### Source
The data comes from the Stanford Openpolicing Project and is focused on police stops in Nashville, TN, from 2010 to 2019.

### Description
The dataset contains information on 3,092,351 police stops and includes 42 columns with various details about each stop. The data was initially collected for the research paper: *E. Pierson et al., “A large-scale analysis of racial disparities in police stops across the United States”, Nature Human Behaviour, Vol. 4, 2020*.

### Key Variables
- `arrest_made`: Indicator of whether an arrest was made during the stop.
- `subject_race`: Race of the individual stopped.
- `subject_sex`: Sex of the individual stopped.
- `stop_time`: Time of the stop.
- `stop_date`: Date of the stop.
- `violation`: Reason for the stop.

## Data Preprocessing

### Handling Missing Values
Missing values were handled by either imputing or dropping columns based on their relevance and the proportion of missing data.

### Feature Engineering
New features were created, and existing features were transformed to enhance model performance. For example, date and time were converted into more meaningful time segments.

### Column Details
Raw columns were dropped to avoid clutter and focus on processed columns. Object data types were investigated to determine if they were categorical or another form, and sparse data was filled where necessary.

## Exploratory Data Analysis (EDA)

### Summary Statistics
Summary statistics provided an overview of the dataset, including counts, means, and standard deviations for numeric columns, and counts for categorical columns.

### Data Visualizations
Data visualizations helped in understanding the distributions and relationships between variables. For example, histograms, bar charts, and box plots were used to visualize the distribution of stop times, subject races, and arrest rates.

## Chi-Square Test of Independence

### Hypothesis Testing
The Chi-square test was used to determine if there was a significant association between categorical variables. For example, it tested the independence between `subject_race` and `arrest_made`.

### Results and Interpretation
Results indicated whether there were significant dependencies between variables. P-values less than 0.05 were considered significant, indicating a relationship between the tested variables.

## Modeling

### Data Split
The dataset was split into training (80%) and test (20%) sets to evaluate model performance.

### Models Used
Several models were applied, including Logistic Regression, Decision Trees, and Random Forests.

### Model Performance
Accuracy and other performance metrics were used to evaluate the models. For instance, confusion matrices, precision, recall, and F1 scores provided insights into model effectiveness.

## Model Interpretation

### Coefficients and Feature Importance
For models like Logistic Regression, coefficients were analyzed to understand the impact of each feature. For tree-based models, feature importance scores highlighted the most influential variables.

### Interpretation of Results
The results were interpreted to understand which factors were most predictive of arrests. For example, the race of the subject and the time of day were significant predictors.

## Conclusion

### Summary of Findings
The analysis revealed key insights into the factors influencing arrests during police stops. The models showed reasonable accuracy in predicting arrests based on the provided features.

