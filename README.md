# Arrest-Prediction-in-Nashville


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



# Racial-Profiling-and-Bias-Detection-in-Minneapolis


### Project Objective

The objective of this project is to analyze racial bias in police interactions and violence in Minneapolis. The study aims to identify patterns and trends that may indicate discriminatory practices based on race.

### Data Description

The dataset contains records of police interactions, including variables such as race, gender, age, outcome of the interaction, and instances of violence. The key variables include:

- **Race**: The race of the individual involved in the police interaction.
- **Gender**: The gender of the individual.
- **Age**: The age of the individual.
- **Interaction Outcome**: The result of the police interaction (e.g., arrest, warning, no action).
- **Violence**: Whether violence was used during the interaction (yes/no).

### Data Preprocessing

#### Handling Missing Values

- **Race**: Missing values were imputed using the most frequent category.
- **Gender**: Missing values were handled by creating a separate category for missing values.
- **Age**: Missing values were replaced with the median age.
- **Interaction Outcome**: Missing values were imputed with the most common outcome.
- **Violence**: Missing values were treated as a separate category.

#### Data Transformation

- **Categorical Variables**: Encoded using one-hot encoding.
- **Continuous Variables**: Standardized to have a mean of 0 and a standard deviation of 1.

### Exploratory Data Analysis

#### Distribution of Variables

- **Race Distribution**: Analysis of the racial composition in police interactions.
- **Gender Distribution**: Analysis of gender representation.
- **Age Distribution**: Age distribution across different racial groups.
- **Interaction Outcome Distribution**: Frequency of different outcomes.

#### Visualizations

1. **Race vs. Interaction Outcome**:
   - Visualization showing the outcome distribution for different racial groups.
   
2. **Gender vs. Interaction Outcome**:
   - Visualization showing the outcome distribution for different genders.

3. **Age vs. Violence**:
   - Visualization showing the age distribution where violence was used.

4. **Race vs. Violence**:
   - Visualization highlighting the instances of violence across different racial groups.

### Statistical Analysis

#### Chi-Square Test of Independence

Performed at a 5% level of significance to determine the dependency between variables:

- **Race and Interaction Outcome**: Dependent
- **Race and Violence**: Dependent
- **Gender and Interaction Outcome**: Independent
- **Age and Violence**: Dependent

### Model Building

#### Classification Models

Several classification models were trained to predict the likelihood of violence in police interactions based on the given features. The models include:

- **Logistic Regression**
- **Naïve Bayes**
- **Support Vector Machine (SVM)**
- **Decision Tree**
- **Random Forest**
- **K-Nearest Neighbors (KNN)**
- **Gradient Boosting**

#### Model Performance

The models were evaluated based on accuracy, precision, recall, and F1-score. The dataset was split into training (80%) and testing (20%) sets. The key findings are:

- **Logistic Regression**: Accuracy - 78%
- **Naïve Bayes**: Accuracy - 75%
- **SVM**: Accuracy - 76%
- **Decision Tree**: Accuracy - 70%
- **Random Forest**: Accuracy - 80%
- **KNN**: Accuracy - 74%
- **Gradient Boosting**: Accuracy - 82%

### Key Findings

- **Racial Disparities**: Significant racial disparities were observed in the outcomes of police interactions, with minority groups more likely to experience adverse outcomes.
- **Gender Influence**: Gender did not strongly depend on the outcome of interactions.
- **Age Factor**: Younger individuals were more likely to experience violence during interactions.
- **Model Insights**: Gradient Boosting provided the best predictive performance, suggesting non-linear relationships between features and the likelihood of violence.

### Conclusion

The analysis highlights the presence of racial bias in police interactions in Minneapolis. The findings suggest a need for policy reforms and further training for police officers to address these disparities. Future work could involve more detailed temporal analysis and the inclusion of additional contextual variables.

