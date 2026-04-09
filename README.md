# Titanic Data Analysis with Pandas

## Project Overview

This project demonstrates **data analysis using the Pandas library** in Python.  
The goal is to explore and analyze the **Titanic dataset** to uncover patterns that influenced passenger survival.

The project also includes a **custom dataset created from scratch** to demonstrate foundational Pandas skills such as creating DataFrames, assigning custom indexes, and organizing structured data.

All analysis was performed in **Google Colab**, and the notebook is included in this repository.

---

# Project Objectives

The project is divided into two main parts:

## Part 1 — Custom Dataset Creation
Create a dataset using a Python dictionary with the following requirements:

- 5 columns (features)
- 15 rows
- Custom index labels

This section demonstrates the ability to construct structured datasets using Pandas.

---

## Part 2 — Titanic Dataset Analysis

A real-world dataset is analyzed using Pandas to explore patterns related to passenger survival.

Dataset used:

train.csv


---

# Dataset Features

The Titanic dataset contains passenger information such as:

- PassengerId
- Pclass (Passenger Class)
- Name
- Sex
- Age
- SibSp (Number of siblings/spouses aboard)
- Parch (Number of parents/children aboard)
- Ticket
- Fare
- Cabin
- Embarked
- Survived (Target Variable)

Where:


Survived = 1 → Passenger survived
Survived = 0 → Passenger did not survive


---

# Project Workflow

## 1. Data Exploration

Initial exploration was performed using:

- `.head()` → View first rows of the dataset
- `.info()` → Understand dataset structure
- `.describe()` → Generate statistical summaries

These steps help identify:

- Data types
- Missing values
- Feature distributions

---

# 2. Data Cleaning

Real-world datasets often contain incomplete or inconsistent data.  
Several cleaning steps were applied:

### Handling Missing Values

| Column | Method Used |
|------|------|
| Age | Replaced with **median age** |
| Embarked | Replaced with **mode value** |
| Cabin | Dropped due to excessive missing values |

### Removing Duplicate Records

Duplicate rows were removed using:


drop_duplicates()


This ensures the dataset remains consistent and reliable for analysis.

---

# 3. Data Analysis using GroupBy

The `groupby()` function was used to analyze survival patterns across different passenger groups.

The following analyses were performed:

### Survival Rate by Gender
To determine whether male or female passengers had higher survival probabilities.

### Survival Rate by Passenger Class
To analyze the effect of socio-economic status on survival.

### Average Age per Passenger Class
To understand demographic differences between passenger classes.

### Survival Rate by Age Group
Passengers were categorized into age groups:


Child
Teen
Young Adult
Adult
Senior


Survival probabilities were then calculated for each group.

---

# 4. Data Filtering

Filtering techniques were used to extract specific subsets of the data.

Examples include:

### Female Passengers Who Survived

Sex = Female AND Survived = 1


### Children Who Survived

Age < 12 AND Survived = 1


### First Class Passengers Who Survived

Pclass = 1 AND Survived = 1


Filtering allows targeted analysis of particular passenger groups.

---

# 5. Key Insights

Based on the analysis, several important conclusions were identified.

### 1. Who was more likely to survive?

Female passengers had a significantly higher survival rate compared to male passengers.

This reflects the historical evacuation protocol:


"Women and children first"


---

### 2. Did passenger class affect survival?

Yes.

Passengers in **First Class** had the highest survival probability, while **Third Class passengers had the lowest**.

Possible reasons include:

- Better cabin locations
- Faster access to lifeboats
- Higher social priority during evacuation

---

### 3. Were children prioritized?

Yes.

Children had noticeably higher survival rates compared to many adult passengers.

This further supports the **women and children first** evacuation policy.

---

### 4. What combination had the highest survival rate?

The group with the highest survival probability was:


Female + First Class + Young Age


These passengers had the best chances of reaching lifeboats safely.

---

# Advanced Pandas Techniques Used

To extend the analysis, several advanced Pandas techniques were applied.

### Pivot Tables

Used to analyze survival probability across multiple variables simultaneously.

Example:


Sex vs Passenger Class


---

### Multi-Level GroupBy

Grouped passengers using multiple features:


Gender + Passenger Class


This reveals deeper survival patterns.

---

### Styled DataFrames

Pandas styling was used to create visual heatmaps that highlight survival probabilities.

---

# Technologies Used

- Python
- Pandas
- Google Colab
- GitHub

---

# Repository Structure


Titanic-Data-Analysis/
│
├── titanic_analysis.ipynb
├── train.csv
├── README.md


---

# How to Run the Project

1. Clone the repository


git clone [https://github.com/yourusername/titanic-analysis](https://github.com/VICO-27/Data-Analysis-with-Pandas).git


2. Open the notebook in **Google Colab**

3. Upload the dataset `train.csv`

4. Run the cells sequentially to reproduce the analysis.

---

# Learning Outcomes

Through this project the following skills were developed:

- Data manipulation with Pandas
- Data cleaning techniques
- Exploratory data analysis
- Group-based statistical analysis
- Data filtering and segmentation
- Extracting insights from real-world datasets

---

# Author

Ashenafi Deresa  
Computer Science & Engineering Student

---

# License

This project is intended for educational purposes.
