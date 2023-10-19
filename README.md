# Module 2: Pandas-challenge

## Table of Contents

* [About](#about)
* [Tools](#tools)
* [Key Steps](#key-steps)
* [Analysis](#analysis)

## About

This project involves the aggregation of school and student data to reveal trends in school performance among 15 schools.

## Tools

* Jupyter Notebook
* Pandas
* Pathlib

## Key Steps

#### **Import Dependencies & Merge Pandas DataFrames**

I imported the necessary dependencies and merged data from CSV files.

```python
# Dependencies and Setup
import pandas as pd
from pathlib import Path

# File to Load
school_data_df = Path("Resources/schools_complete.csv")
student_data_df = Path("Resources/students_complete.csv")

# Read School and Student Data File and store into Pandas DataFrames
school_data = pd.read_csv(school_data_df)
student_data = pd.read_csv(student_data_df)

# Combine the data into a single dataset.
school_df = pd.merge(student_data, school_data, how="left", on=["school_name", "school_name"])
school_df.head()

```
The merged data frame highlighted the District Summary, School Summary, Highest and Lowest-Performing Schools by Passing Percentage, Math and Reading Scores by Grade Level, Scores by School Spending, and Scores by School Size and Type. 

---------------------------------------------------

#### **District Summary**
Created a high-level snapshot of the district's key metrics in a DataFrame.  
The District Summary gave a broad look into the district’s 15 school totals, student population of 39,170 and outlining the School District’s Total Budget of $24,649,428. The data frame also gave a snapshot of the school district’s 78.9% average math score, 81.8% average reading score, and overall passing rate of 65.1%.

<img src="images/DistrictSnapshot.png" alt= "snapshot">

---------------------------------------------------

#### **Per School Summary**
Created a DataFrame called per_school_summary with columns for School Type, Total Students, Total School Budget, Per Student Budget, Average Math Score, Average Reading Score, % Passing Math, % Passing Reading,% Overall Passing.

<img src="images/PerSchool.png"alt="Perschool">

---------------------------------------------------

#### **Top 5 Highest Performing Schools**
Created a DataFrame with the Top 5 Performing Schools.

<img src="images/HighestPerforming5.png"alt="Top5">

---------------------------------------------------
#### **Bottom 5 Performing Schools**
Created a DataFrame with the Bottom 5 Performing Schools

<img src="images/Bottom5.png" alt="bottom5">

---------------------------------------------------

#### **Math Scores by Grade**
Created a DataFrame for Math Scores by Grade.

<img src="images/MathByGrade.png" alt="mathG">

---------------------------------------------------

#### **Reading Scores by Grade**

Created a DataFrame for Reading Scores by Grade.
<img src="images/ReadingByGrade.png" alt="readingG">

---------------------------------------------------

#### **Scores by School Spending**
Created a DataFrame for Scores by School Spending.

<img src="images/ScoreSchoolSpending.png" alt= "schoolSpening">

---------------------------------------------------

#### **Scores by School Size**
Created a DataFrame for Scores by School Size.

<img src="images/SML.png" alt="lms">

---------------------------------------------------

#### **Scores by School Type**
Created a DataFrame for Scores by School Type

<img src="images/SchoolType.png" alt="schooltype"

---------------------------------------------------

## Analysis
The District Summary gave a broad look into the district’s 15 school totals, student population of 39,170 and outlining the School District’s Total Budget of $24,649,428. The data frame also gave a snapshot of the school district’s 78.9% average math score, 81.8% average reading score, and overall passing rate of 65.1%. The School Summary also identified the school names and school type.

The Highest and Lowest-Performing Schools by Percentages gave a more narrowed interpretation of the data. The data frame indicated a strong correlation between Charter School Types with higher overall passing percentages and lower per-student budget. With the Charter School Type Overall Passing Percentage ranging from 90.5% to 91.3% and per student budget ranging from 582 dollars to 638 dollars. Meanwhile, the District School Types had higher per-student budget ranging from 655 dollars to 637 dollars and lower overall passing rates ranging from 52.9% to 53.3%.</n>

The Math and Reading by Grad Level data frame indicated that all Grade Levels had passing percentages throughout 9th, 10th, 11th, and 12th grade, with little variation on each school’s individual grade level scores.  

The Scores by School Spending highlighted a key Spending Range Per Student metric, essential in identifying a deficit in return on investment on the total budget. The evident correlation is that the District School Types have a higher Spending Range Per Student and lower scores and percentages across the fields highlighted in this data frame. The Charter School Types hold a solid return on investment of their Total Budget, with a lower Spending Range Per Student, yet higher scores and percentages, corroborating the opposite effect with the District Type of School correlation. Another conclusion from this data set is that the highest Overall Passing Percentage came from the Spending Range of less than 585 dollars.

The Scores by School Size data frame grouped student population sizes into three categories, Small, Medium, and Large. This metric helped identify that scores are impacted by student population, with the most successful scores within the School District coming from the Charter School Type and the Small to Medium School Sizes with populations ranging from less than a thousand and up to two thousand student population. In contrast, the District School Types had lower overall Scores and a larger student population of two thousand to five thousand. A limitation to this data set is that socioeconomic factors were not considered.

In conclusion, the data collected would reflect that the Charter School Types within the PyCity School District has an overall better success rate across all highlighted metrics within the data frames. The variable of lower student population in the Charter School Types was an evident contributor to a lower budget per-student and had a direct effect on return of investment on allocated resources on higher average math and reading scores and an overall higher passing percentage. To improve the analysis I would add class size per school type and per classroom budget in each individual academic subject. This can help identify any overinvestments with allocated resources. 


Sited Peer Collaboration with Ryan Himes, Adam Gostinger
