# Diabetes_Prediction

Objective<br>
This project aims to predict whether individuals are at risk of diabetes using survey data from the CDC BRFSS2015 dataset. The analysis includes data wrangling, exploratory data analysis (EDA), outlier handling, and feature relationship exploration.

Dataset
Source: Cleaned CDC BRFSS2015 survey responses

Records: 70,692

Features: 22 columns (demographics, health status, lifestyle, etc.)

Feature Overview
Feature	Description
Diabetes_binary	0 = No diabetes, 1 = Prediabetes or diabetes
HighBP	0 = No high BP, 1 = High BP
HighChol	0 = No high cholesterol, 1 = High cholesterol
CholCheck	0 = No cholesterol check in 5 years, 1 = Yes
BMI	Body Mass Index
Smoker	0 = No, 1 = Yes (smoked ≥100 cigarettes in lifetime)
Stroke	0 = No, 1 = Yes
HeartDiseaseorAttack	0 = No, 1 = Yes (CHD or MI)
PhysActivity	0 = No, 1 = Yes (physical activity in past 30 days)
Fruits	0 = No, 1 = Yes (consume fruit ≥1 time/day)
Veggies	0 = No, 1 = Yes (consume vegetables ≥1 time/day)
HvyAlcoholConsump	0 = No, 1 = Yes (men ≥14 drinks/week, women ≥7 drinks/week)
AnyHealthcare	0 = No, 1 = Yes (any health coverage)
NoDocbcCost	0 = No, 1 = Yes (could not see doctor due to cost in past 12 months)
GenHlth	1 = Excellent, 5 = Poor (general health, scale 1-5)
MentHlth	Days of poor mental health (1-30)
PhysHlth	Days of physical illness/injury (1-30)
DiffWalk	0 = No, 1 = Yes (difficulty walking/climbing stairs)
Sex	0 = Female, 1 = Male
Age	1 = 18-24, 13 = 80+ (13-level age category)
Education	1 = Kindergarten or less, 6 = College grad (scale 1-6)
Income	1 = < $35,000, 8 = $75,000+ (scale 1-8)
Data Preparation
Duplicates: 1,635 duplicates removed.

Missing Values: No missing values after cleaning.

Outliers: Only BMI outliers handled (using IQR method); other outliers retained as they represent rare but real cases.

Exploratory Data Analysis (EDA)
1. Class Distribution
Diabetes_binary: Nearly balanced (1:1 ratio between diabetic and non-diabetic).

2. Diabetes Prevalence by Age Group
Age Groups: Infant, Child, Minor, Pre-teen (custom bins).

Findings: Diabetes prevalence increases with age, highest in Pre-teen group.

3. Diabetes Prevalence by Gender
Observation: Females have a higher non-diabetic rate; males have a higher diabetic rate.

4. Socioeconomic Factors
Income & Education: Lower income and education levels are associated with higher diabetes risk.

5. Feature Relationships
BMI & Diabetes: Higher BMI categories show increased diabetes prevalence.

Heart Disease: Strong co-occurrence with diabetes.

Smoking: Smokers have a higher diabetes rate.

Alcohol Consumption: Heavy drinkers show a slight increase in diabetes risk.

Data Visualization
Correlation Matrix: Used to identify relationships between features and diabetes risk.

Boxplots: For outlier detection and comparison of BMI across diabetes risk groups.

Barplots: For prevalence analysis by age, gender, BMI, heart disease, smoking, and alcohol consumption.

Usage
Requirements
Python 3.x

pandas

numpy

matplotlib

seaborn

scikit-learn

Quick Start
python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.preprocessing import StandardScaler

# Load the dataset
df = pd.read_csv('dataset.csv')

# Data wrangling, EDA, and visualization steps follow as shown in the notebook/script
Key Results
No class imbalance: Diabetic and non-diabetic cases are nearly equal.

Age, BMI, and heart disease are strong predictors of diabetes risk.

Lifestyle factors (smoking, alcohol) and socioeconomic status (income, education) are also significant.

Reasoning
Outliers were retained except for BMI, as they may represent real-world rare cases.

Feature engineering (age and BMI bins) was used for better interpretability.

Visualizations and group statistics were central to understanding feature relationships.

License
This project is for educational and research purposes.
