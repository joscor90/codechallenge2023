# README

## About the project

This is a small ETL Project part of the Code Challenge 2023 by Globant. It compresses the use of Python and SQL in order to clean and organize the data.

## Tools

+ Python 3.11.4
+ Pandas 1.5.3
+ SQL Server
+ SQL Server Management Studio

## Dataset

The dataset used for this project was IIT Admissions Dataset - 200,000 Students, available on Kraggle: https://www.kaggle.com/datasets/goyaladi/iit-admissions-dataset?rvi=1. This dataset was downloaded as a csv file and store in the data directory of the project

## Setup

Python 3.11.4 and Pandas 1.5.3 should be installed on your device in order to run the code properly. A text editor that support ipynb files is also required.

## Worflow

### Data Cleaning

Data cleaning was performed using the **pandas** library and the code stored in the *code_challenge.ipynb* file. Briefly, *student_data.csv* was imported into a pandas dataframe were first it was explored by size, column types and a statistics summary. Later, missing values and duplicate handling was performed in order to obtain an appropiate csv file to use. For the missing values handling it was assumed that a "" correspond to a missing value. Missing values were only present in the *Student Name* field and not the *Student ID*  so i opted for missing value imputation instead of a removal of the entry. Then, an "Unkwon" value was imputed onto those missing entries.For duplicates handling it was opted to delete duplicated entries in which all fields are duplicated.

Finally, the transformed pandas dataframe was exported as a new csv file "called clean_code_challenge.csv". 

### Grouping by SQL

In order to group the data by specialization and year of admission SQL was used. SQL Server and SQL Server Management Studio were used. The resulting CSV file from the previous step was imported into **SQL Server Management** Studio where a new query was performed onto it. This query is specified in the *code_challenge.sql* file. The results from this query were exported as a new csv file called "clean_code_challenge_sqlResults.csv".

## Work-in-progress

Sadly, i didn't manage to implement the BigQuery table and the Apache Airflow injection because of lack of time. However i'm planning to do that eventually as part of a learning experience.

## Bonus

In the *bonus* folder you can check a small JavaScript project a did a while ago. I do also know React, Node and other JavaScript libraries for web development. 
