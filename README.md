# # Titanic Survival Analysis: Exploratory Data Analysis with Pandas

## Project Overview

This project performs Exploratory Data Analysis (EDA) on the famous Titanic dataset using Python and Pandas.

The objective is to explore passenger information, understand the structure of the dataset, identify missing values, and uncover factors that influenced survival rates during the Titanic disaster.

This project was completed as part of the Data Science Nigeria (DSN) 2026 Free AI Classes Program.

---

## Problem Statement

The Titanic dataset contains passenger information such as:

- Passenger Class
- Gender
- Age
- Fare
- Cabin Information
- Embarkation Port
- Survival Status

The goal of this analysis is to investigate patterns in the data and determine which factors were most strongly associated with passenger survival.

---

## Technologies Used

- Python
- Pandas
- Google Colab

---

## Dataset Source

Titanic Dataset

Source:
https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv

---

## Project Tasks

### Task 1: Load the Dataset

The Titanic dataset was imported directly from GitHub using Pandas.

```python
import pandas as pd

url = "https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv"
df = pd.read_csv(url)

print(df.head())

Task 2: Perform Exploratory Data Analysis (EDA)
The dataset was explored to understand:
Dataset dimensions
Column names
Data types
Missing values
Statistical summaries
Key functions used:
Python
df.shape
df.info()
df.describe()
df.isnull().sum()

Survival Analysis
Overall Survival Rate
The overall survival rate was calculated using:
Python
df['Survived'].mean()
Result:
Plain text
38.38%
This means approximately 4 out of every 10 passengers survived.


Survival Rate by Gender
Python
df.groupby('Sex')['Survived'].mean()
Results:
Gender
Survival Rate
Female
74.20%
Male
18.89%
Key Insight
Female passengers were significantly more likely to survive than male passengers.
This suggests that gender played a major role in survival outcomes during the disaster.


Survival Rate by Passenger Class
Python
df.groupby('Pclass')['Survived'].mean()
Results:
Passenger Class
Survival Rate
1st Class
62.96%
2nd Class
47.28%
3rd Class
24.24%

Key Insight
Passengers traveling in First Class had the highest probability of survival.
Survival rates decreased steadily from First Class to Third Class, indicating that socioeconomic status influenced survival chances.
Missing Values Analysis
The analysis revealed missing values in several columns:
Column


Missing Values
Cabin
Highest
Age
Moderate
Embarked
Few


Key Insight
The Cabin column contains a significant number of missing values and would require further preprocessing before being used in predictive modeling.


Key Findings
Overall passenger survival rate was approximately 38%.
Female passengers had a substantially higher survival rate than males.
First Class passengers had the highest likelihood of survival.
Passenger class and gender were strong predictors of survival.
The dataset contains missing values that require preprocessing before machine learning applications.



Learning Outcomes
Through this project, I gained practical experience in:
Data Loading with Pandas
Exploratory Data Analysis (EDA)
Group-Based Aggregations
Missing Value Analysis
Data Interpretation
Statistical Summarization
Extracting Business Insights from Data


Author
George Abasiumoh
Chemical Engineering Graduate
Aspiring Data Scientist | Machine Learning Enthusiast | AI Learner
Achievements:
Top 50 Participant — DSN 2026 Free AI Classes
Ranked 9th in DSN Machine Learning Hackathon

