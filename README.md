# Exploratory Data Analysis (EDA): Student Performance Dataset

## Introduction

Exploratory Data Analysis (EDA) is an essential step in the data analysis process that helps uncover patterns, trends, relationships, and anomalies within a dataset. Through statistical summaries and visualizations, EDA provides valuable insights that support data-driven decision-making.

This project focuses on analyzing student academic performance data collected from secondary school students. The objective is to identify factors that influence student achievement and understand how demographic, social, and academic attributes relate to final grades.

The project demonstrates key data analysis concepts including:

* Data inspection and cleaning
* Statistical summary analysis
* Univariate analysis
* Bivariate analysis
* Correlation analysis
* Data visualization using charts and plots
* Identifying key influencing factors
* Extracting meaningful insights from data

By exploring relationships between study habits, attendance, internet access, and academic performance, this project aims to provide insights that can support educational improvement strategies.

---

# Dataset Information

**Source:** UCI Machine Learning Repository

The Student Performance Dataset contains demographic, social, and academic information collected from Portuguese secondary school students.

## Dataset Overview

| Metric          | Value            |
| --------------- | ---------------- |
| Records         | 395              |
| Features        | 33               |
| Target Variable | G3 (Final Grade) |

---

# Features Included

| Feature   | Description               |
| --------- | ------------------------- |
| age       | Student age               |
| sex       | Student gender            |
| studytime | Weekly study time         |
| absences  | Number of school absences |
| internet  | Internet access at home   |
| G1        | First period grade        |
| G2        | Second period grade       |
| G3        | Final grade               |

---

# Tools and Technologies Used

## Programming Language

Python

## Libraries

* Pandas
* NumPy
* Matplotlib
* Seaborn
* UCI ML Repository API (ucimlrepo)

## Development Environment

Jupyter Notebook

---

# Requirements

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn ucimlrepo
```

---

# Project Structure

```text
Student_Performance_EDA/
│
├── Student_Performance_Dataset.ipynb
├── README.md
├── images/
│   ├── grade_distribution.png
│   ├── age_distribution.png
│   ├── gender_distribution.png
│   ├── studytime_distribution.png
│   ├── absences_distribution.png
│   ├── studytime_vs_grade.png
│   ├── absences_vs_grade.png
│   ├── gender_vs_grade.png
│   ├── internet_vs_grade.png
│   ├── correlation_heatmap.png
│   └── pairplot.png
```

---

# Data Exploration

## Step 1: Loading the Dataset

The dataset was fetched directly from the UCI Machine Learning Repository using:

```python
from ucimlrepo import fetch_ucirepo

student_performance = fetch_ucirepo(id=320)
```

### Initial Dataset Dimensions

| Metric  | Value |
| ------- | ----- |
| Rows    | 395   |
| Columns | 33    |

---

## Step 2: Dataset Inspection

Dataset inspection included:

```python
df.info()
df.describe()
df.isnull().sum()
df.duplicated().sum()
```

### Observation

No significant missing value issues were identified, and the dataset was suitable for analysis after basic validation.

### Insight

Understanding data structure and quality is essential before performing any analytical tasks.

---

## Step 3: Statistical Summary

Statistical summaries were generated using:

```python
df.describe()
```

### Observation

Most students were between 15 and 18 years old, with final grades concentrated within the middle performance range.

### Insight

The dataset provides a balanced representation of student performance levels suitable for exploratory analysis.

---

# Univariate Analysis

## Grade Distribution

### Observation

Most students achieved final grades between 8 and 15, indicating average academic performance for the majority of students.

### Visualization

<img width="705" height="479" alt="Final_Grade_Distribution" src="https://github.com/user-attachments/assets/8882c42b-049f-41e7-b320-cccce32cfff4" />


---

## Age Distribution

### Observation

Most students were between 15 and 18 years old.

### Visualization

<img width="705" height="479" alt="Age_Distribution" src="https://github.com/user-attachments/assets/52ee44df-1ea5-463e-bee9-fa156ccfe165" />


---

## Gender Distribution

### Observation

The dataset contains a relatively balanced distribution of male and female students.

### Visualization

<img width="550" height="402" alt="Gender_Distribution" src="https://github.com/user-attachments/assets/6639d7e4-f31c-4061-be1a-f8fb9425061a" />


---

## Study Time Distribution

### Observation

Most students reported studying between two and five hours per week.

### Visualization

<img width="705" height="479" alt="Study_Time_Distribution" src="https://github.com/user-attachments/assets/294c190a-3654-4e34-a0ed-c368bd415ad4" />


---

## Absences Distribution

### Observation

Most students recorded relatively low numbers of absences, while a small number exhibited significantly higher absenteeism.

### Visualization

<img width="705" height="479" alt="Absences_Distribution" src="https://github.com/user-attachments/assets/50b896a6-ddf1-404b-8326-d38382e0e463" />

---

# Bivariate Analysis

## Study Time vs Final Grade

### Observation

Students who dedicated more time to studying generally achieved higher final grades.

### Visualization

<img width="710" height="479" alt="Study_Time_vs_Final_Grade" src="https://github.com/user-attachments/assets/872dd55a-7e4f-4bdf-a321-ccfcb67a9d1b" />


### Insight

Study habits appear to have a positive influence on academic performance.

---

## Absences vs Final Grade

### Observation

Higher levels of absenteeism were associated with lower final grades.

### Visualization

<img width="710" height="479" alt="Absences_vs_Final_Grade" src="https://github.com/user-attachments/assets/6488b522-31fd-47be-8a22-d059d6c4e541" />


### Insight

Regular attendance plays an important role in student success.

---

## Gender vs Final Grade

### Observation

Academic performance differences between genders were relatively small.

### Visualization

<img width="710" height="479" alt="Gender_vs_Final_Grade" src="https://github.com/user-attachments/assets/822b61e5-2e64-4704-b010-b686fcb9a478" />

---

## Internet Access vs Final Grade

### Observation

Students with internet access generally achieved slightly better academic outcomes.

### Visualization

<img width="710" height="479" alt="Internet_Access_vs_Final_Grade" src="https://github.com/user-attachments/assets/a9f38593-31d2-48a6-8d75-3d9f0fd6b332" />


### Insight

Access to educational resources may contribute positively to academic performance.

---

# Correlation Analysis

## Correlation Heatmap

### Observation

Strong positive correlations were observed between G1, G2, and G3 grades.

### Visualization

<img width="983" height="750" alt="Correlation_Heatmap" src="https://github.com/user-attachments/assets/9ac278b3-95bc-46e9-b3c7-71e9154e8e55" />


### Insight

Past academic performance is a strong indicator of future academic achievement.

---

## Pairwise Relationship Analysis

Pairplot visualization was used to examine relationships between:

* G1
* G2
* G3
* studytime
* absences

### Visualization

<img width="1233" height="1228" alt="pairplot" src="https://github.com/user-attachments/assets/e6332c59-8eec-4d35-87a3-067f26393d81" />


### Insight

The strongest relationships were observed between previous grades and final grades.

---

# Key Findings

* The dataset contains 395 student records and 33 attributes.
* Most students achieved final grades within the average performance range.
* Study time showed a positive relationship with academic performance.
* Higher absenteeism was associated with lower final grades.
* Internet access demonstrated a slight positive influence on performance.
* Previous grades (G1 and G2) exhibited the strongest correlation with final grade (G3).
* Academic performance patterns were consistent across multiple visualizations and statistical analyses.

---

# Conclusion

This project successfully demonstrated the application of Exploratory Data Analysis techniques using a real-world educational dataset.

Through statistical summaries, visualizations, and correlation analysis, several factors influencing student academic performance were identified. Study habits, attendance, internet access, and previous academic results all contributed to variations in final grades.

The analysis revealed that previous academic performance is the strongest predictor of final achievement, while factors such as study time and attendance also play important roles. These insights can help educators identify students who may require additional support and assist in developing strategies to improve learning outcomes.

Overall, the project provided valuable experience in data exploration, visualization, and analytical thinking while demonstrating how EDA can uncover meaningful patterns within educational data.
