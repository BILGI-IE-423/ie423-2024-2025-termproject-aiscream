# Beneath the Surface: Quiet Factors in Student Success

# Abstract

This research project investigates the extent to which student academic performance can be shaped by factors beyond their control—such as family background, home environment, and socioeconomic context. Using machine learning models trained on features including parental involvement, household income, and access to educational resources, the study explores how these elements relate to academic outcomes. The core aim is to help educators better understand which students may be at risk of falling behind—not because of effort or motivation, but due to structural disadvantages at home that are often invisible in the classroom. By identifying these patterns, the study seeks to inform practical, empathy-driven approaches that allow teachers to offer timely and appropriate support to students who may otherwise go unnoticed.

# Scope of the Project

The project focuses on analyzing uncontrollable variables that can influence a student's academic success. These include factors such as Parental Education Level, Family Income, Distance from Home, Family Size, Parental Jobs, and Support at Home. Rather than aiming for broad or general conclusions about what affects academic performance, this study concentrates on:
* Understanding how much these background factors contribute to students doing well or poorly in school.
* Exploring which specific home-related features are most strongly linked to academic difficulty.
* Providing teachers with insight that could help them recognize students in need of extra attention, even before academic struggles become visible.
This perspective is particularly valuable in contexts where teachers may not have detailed knowledge of students' home lives, yet are expected to meet their learning needs fairly and effectively.

# Research Questions 

This study is guided by the central question: How much of a student’s success is shaped by factors outside their control? To explore this, we ask:
- **RQ1: Are student outcomes significantly affected by uncontrollable background variables?**  
  _This question helps us understand whether external circumstances have a noticeable pattern in academic outcomes._


- **RQ2: Which uncontrollable factors are most consistently linked with above- or below-average performance?**  
  _We aim to highlight which home or background-related features may be warning signs of academic risk._

- **RQ3: Is it possible to flag potentially at-risk students early on, using only background data—before their grades begin to drop?**
  _This could help teachers and schools provide timely, targeted support to students who may be silently struggling._
  
By focusing on what students bring with them to the classroom—before they even open a textbook—this project hopes to support more informed, sensitive, and proactive educational practices.

# Preprocessing 

Preprocessing is applied to all four datasets used in the study, referred to as por, mat, main, and factors. These names are used solely for identification; all datasets serve the same analytical purpose and share a largely overlapping set of features, with some unique features.

Preprocessing was applied separately to all four datasets. Most features were retained at this stage to preserve the full context of each student’s profile. While a few columns were removed for specific reasons (detailed below), features related to controllable behaviors, such as study time are intentionally kept. These variables, although not the primary focus of the analysis, are useful for:

identifying potential outliers in the dataset,
providing additional context when interpreting background factors,
and supporting exploratory analysis or validation checks during the modeling phase.

Removed Columns:

school (from 'mat' and 'por'): Removed to avoid splitting the datasets by school name, which would significantly reduce the sample size. The schools are structurally similar, so their distinction was not essential.
traveltime (from 'mat' and 'por'): The feature grouped all durations over 1 hour into a single category and used narrow 15-minute intervals between others, offering little useful variation.
Dalc and Walc (from 'mat' and 'por': Removed due to ethical and contextual concerns. These features relate to alcohol consumption, which is a sensitive subject, especially in a research focused on high school students that are mostly underaged. So we decided to exclude those features from our research.

Steps Applied to Each Dataset:

Missing Values: Imputed using median for numerical columns and mode for categorical ones.
Encoding: All categorical variables were label encoded to ensure compatibility with ML models.
Scaling: Numerical columns were standardized using z-score normalization.
Train-Test Split: Each dataset was split into training and test sets using an 70-30 ratio. All remaining columns are retained in both sets.
Split Checks: Histograms were generated to compare the train/test distribution of the target variable in each dataset.
File Export: A total of 8 CSV files were created, train and test versions for each of the four datasets(mat,por,main,factors).


## Datasets Used

- **[UCI Student Performance Dataset](https://archive.ics.uci.edu/dataset/320/student+performance)**  
  Contains student achievement data in secondary education, including grades and various student background factors.

- **[Student Performance Factors Dataset (Kaggle)](https://www.kaggle.com/datasets/lainguyn123/student-performance-factors)**  
  Offers insights into multiple factors influencing student performance such as family background, parental education, and school-related variables.

- **[Students Performance Dataset (Kaggle)](https://www.kaggle.com/datasets/rabieelkharoua/students-performance-dataset)**  
  A clean and structured dataset focused on students’ academic results, gender, test preparation, and parental education.


## Team Name: **AiScReam**

**Team Members:**

* Revhat Umut Akdoğan 120203012

* Eren Gümüşay 121203082

* Mohammad Eid Shokri Siag 121203010

