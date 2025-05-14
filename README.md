# Diabetes_Prediction

# Objective<br>
This project aims to predict whether individuals are at risk of diabetes using survey data from the CDC BRFSS2015 dataset. The analysis includes data wrangling, exploratory data analysis (EDA), outlier handling, and exploration of feature relationships.<br><br>

# Dataset<br>
Source: Cleaned CDC BRFSS2015 survey responses<br>
Records: 70,692<br>
Features: 22 columns (including demographics, health status, lifestyle, etc.)<br><br>

# Feature Overview<br>
# Dataset Used<br>
The dataset used in this project is the clean dataset of 70692 survey responses to the CDC BRFSS2015. 
This dataset contains 22 feature columns.<br><br>

# Data Preparation<br>
Duplicates: 1,635 duplicate rows were removed.<br>
Missing Values: None remaining after cleaning.<br>
Outliers: Only BMI outliers were handled using the IQR method; other outliers were retained to preserve data integrity.<br><br>

# Data Visualization Techniques Used <br>
Correlation Matrix: To explore inter-feature relationships and their correlation with diabetes risk.<br>
Boxplots: Used for comparing BMI across diabetes status groups.<br>
Barplots: Visualized diabetes prevalence by age, gender, BMI, heart disease, smoking, and alcohol consumption.<br><br>

# Requirements<br>
Python 3.x<br>
pandas<br>
numpy<br>
matplotlib<br>
seaborn<br>
scikit-learn<br><br>

# Contribution<br>
If you'd like to contribute:<br>

1. Fork the repository.<br>
2. Create a new branch (git checkout -b feature-name).<br>
3. Make your changes and commit (git commit -m 'Add new feature').<br>
4. Push to your branch (git push origin feature-name).<br>
5. Open a Pull Request.<br><br>

# License<br>
This project is intended solely for educational and research purposes.
