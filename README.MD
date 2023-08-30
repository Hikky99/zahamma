# Zahamma Heart Project Documentation

### Author: Hamza Mohammed


## Synopsis

Heart diseases are a leading cause of mortality in Ghana and around the world. This project focuses on developing machine learning models for early detection of heart diseases. By utilizing patient data, including medical history, lifestyle information, and laboratory test results, this model can identify individuals at high risk for heart disease, enabling early intervention.

## Aim

The primary objectives of this project are as follows:
- To create classification models for predicting the likelihood of heart disease based on various attributes.
- The problem involves binary classification, where the goal is to predict whether a patient is prone to heart disease or not.

## Dataset Attributes

The dataset includes the following attributes:

- **MaxHR**: The maximum heart rate achieved during exercise.
- **RestingECG**: Results of the resting electrocardiogram.
- **Age**: Age of the patient in years.
- **Sex**: Gender of the patient (M: Male, F: Female).
- **ChestPainType**: The type of chest pain experienced by the patient.
- **RestingBP**: Resting blood pressure measured in mm Hg.
- **Cholesterol**: Serum cholesterol level measured in mm/dl.
- **FastingBS**: Fasting blood sugar level (1: If FastingBS > 120 mg/dl, 0: Otherwise).
- **ExerciseAngina**: Presence of exercise-induced angina (Y: Yes, N: No).
- **Oldpeak**: ST depression induced by exercise.
- **ST_Slope**: The slope of the peak exercise ST segment.
- **HeartDisease**: Output class indicating the presence of heart disease (1: Heart disease, 0: Normal).




## Exploratory Data Analysis and Visualization

### Data Distribution Visualization

1. **Categorical Feature Distribution Visualization**
   - **Code Purpose**: Visualizes the distribution of categorical features based on whether a person has heart disease or not.
   - **Description**: This code creates a set of subplots to visualize the distribution of each categorical feature in the dataset. The distribution of each feature is plotted using Seaborn's `distplot` function, and each subplot represents a different categorical feature. The data is divided into two groups: one for people with heart disease and another for those without. The plots show how the distribution of each categorical feature varies between the two groups.

### Data Transformation and Encoding

2. **Label Encoding of Categorical Features**
   - **Code Purpose**: Converts categorical features into numerical values using label encoding.
   - **Description**: This code snippet uses the LabelEncoder from scikit-learn to transform categorical features like 'Sex', 'ChestPainType', 'RestingECG', 'ExerciseAngina', and 'ST_Slope' into numerical values. This is necessary for many machine learning algorithms that require numerical input. The transformed data is stored in the 'df1' DataFrame.

### Visualization Enhancement

3. **Enhanced Visualization Styling**
   - **Code Purpose**: Improves the visual styling of distribution plots.
   - **Description**: This code sets a modern color palette and applies it to a set of distribution plots. It uses a dark background style for the plots and customizes the text color, tick marks, and title text color to create a visually appealing and consistent appearance.

### Class Distribution Visualization

4. **Visualization of Heart Disease Distribution**
   - **Code Purpose**: Visualizes the distribution of heart disease cases in the dataset.
   - **Description**: This code creates pie charts and a count plot to display the distribution of heart disease cases. The first pie chart shows the percentage of people with and without heart disease. The second count plot displays the actual count of heart disease cases and no heart disease cases.

5. **Visualization of Categorical Features vs. Heart Disease**
   - **Code Purpose**: Compares the distribution of categorical features based on heart disease cases.
   - **Description**: This code generates count plots to visualize the distribution of each categorical feature based on the presence or absence of heart disease. Each subplot represents a different categorical feature, and the bars are color-coded to differentiate between cases with and without heart disease.

### Visualization of Numerical Features

6. **Visualization of Numerical Features vs. Heart Disease**
   - **Code Purpose**: Compares the distribution of numerical features based on heart disease cases.
   - **Description**: This code creates count plots to visualize the distribution of each numerical feature based on heart disease cases. Each subplot represents a different numerical feature, and the bars are color-coded to differentiate between cases with and without heart disease.

### Data Preprocessing and Scaling

7. **Data Grouping and Scaling**
   - **Code Purpose**: Creates new feature groups and applies scaling to numerical features.
   - **Description**: This code creates new feature groups by grouping certain numerical features based on their values. It then applies MinMax scaling to 'Oldpeak' and Standard scaling to 'Age', 'RestingBP', 'Cholesterol', and 'MaxHR' using MinMaxScaler and StandardScaler from scikit-learn. The transformed data is stored in the 'df1' DataFrame.

### Correlation Heatmap

8. **Correlation Heatmap**
   - **Code Purpose**: Visualizes the correlation between numerical features using a heatmap.
   - **Description**: This code generates a heatmap to visualize the correlation between numerical features in the 'df1' DataFrame. The colors indicate the strength and direction of the correlation between pairs of features.

### Correlation with Target

9. **Correlation of Features with Heart Disease**
   - **Code Purpose**: Measures the correlation of features with respect to heart disease.
   - **Description**: This code calculates the correlation of each feature with the 'HeartDisease' column and displays the results in a heatmap. It provides insights into the relationships between individual features and the target variable.

## Model Evaluation

### Model Function

10. **Model Evaluation Function**
    - **Function Purpose**: Trains a classifier, evaluates its performance, and plots the ROC curve.
    - **Description**: This function takes a classifier instance as input, trains it using the training data, makes predictions on the test data, and evaluates its performance. It calculates and displays the accuracy, cross-validation score, and ROC AUC score. Additionally, it plots the ROC curve to visualize the classifier's performance.

### Model Evaluation Function

11. **Model Evaluation Function**
    - **Function Purpose**: Evaluates the classifier's performance using a confusion matrix heatmap and classification report.
    - **Description**: This function takes a classifier instance as input and evaluates its performance. It calculates the confusion matrix, annotates it with labels for true negatives, false positives, false negatives, and true positives, and displays it using a heatmap. Furthermore, it prints out a detailed classification report containing metrics such as precision, recall, and F1-score.

