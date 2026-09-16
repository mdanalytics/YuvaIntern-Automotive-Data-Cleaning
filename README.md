# Automotive Data Quality Assessment & Cleaning Using Python

## Project Overview

This project focuses on identifying and cleaning common data-quality issues in an automotive dataset using Python. The dataset was created for practice with intentional errors such as missing values, duplicate records, inconsistent text values, invalid numerical values, and invalid year values.

The project demonstrates a basic data-cleaning workflow using **Pandas** and **NumPy**, from initial data inspection to cleaning and validation.

## Objective

The main objectives of this project are:

* Inspect the structure and size of the dataset
* Identify missing values
* Detect duplicate records
* Identify duplicate `Car_ID` values
* Detect inconsistent categorical values
* Identify invalid negative numerical values
* Detect invalid year values
* Clean missing and invalid values
* Validate the cleaned dataset

## Dataset

The dataset contains automotive information with **10 columns**:

| Column         | Description                    |
| -------------- | ------------------------------ |
| `Car_ID`       | Unique identifier for each car |
| `Brand`        | Car manufacturer               |
| `Model`        | Car model                      |
| `Year`         | Manufacturing year             |
| `Price`        | Vehicle price                  |
| `Mileage`      | Vehicle mileage                |
| `Fuel_Type`    | Petrol or Diesel               |
| `Transmission` | Manual or Automatic            |
| `Engine_cc`    | Engine capacity                |
| `Owner_Count`  | Number of previous owners      |

The initial dataset contains **50 records and 10 columns**. During the project, additional duplicate records are intentionally added to demonstrate duplicate detection and removal.

## Data Quality Issues Introduced

The project intentionally introduces several data-quality problems.

### 1. Missing Values

Missing values are added to:

* `Price`
* `Mileage`
* `Fuel_Type`

The initial quality check identifies **2 missing values in each of these columns**.

### 2. Duplicate Records

Three existing rows are duplicated to create duplicate records. The resulting dataset contains **53 rows**, and the initial duplicate check identifies **2 duplicate rows**.

### 3. Duplicate Car IDs

After removing complete duplicate rows, a duplicate `Car_ID` is checked and identified. The project then removes duplicate records based on `Car_ID`.

### 4. Inconsistent Categorical Values

Examples of inconsistent values intentionally introduced include:

* `toyota`
* `TOYOTA`
* `Toyta`

For fuel type:

* `petrol`
* `PETROL`
* `diesel`

For transmission:

* `automatic`
* `MANUAL`

These inconsistencies demonstrate why categorical values need standardization during data cleaning.

### 5. Invalid Numerical Values

The dataset contains invalid negative values such as:

* Negative `Price`
* Negative `Mileage`
* Negative `Engine_cc`

These values are identified and handled during the cleaning process.

### 6. Invalid Year Values

Two unrealistic year values are intentionally introduced:

* `1890`
* `2035`

These are identified as invalid year values during the data-quality inspection.

## Data Cleaning Process

The following cleaning techniques are demonstrated:

1. Inspect dataset shape and structure
2. Check missing values using `isnull()`
3. Detect duplicate records using `duplicated()`
4. Remove duplicate records using `drop_duplicates()`
5. Check duplicate `Car_ID` values
6. Handle missing numerical values using the median
7. Handle missing categorical values using the mode
8. Identify negative values using filtering
9. Convert invalid negative values to missing values
10. Replace missing numerical values using the median
11. Perform final validation

For example, missing `Price` and `Mileage` values are handled using median values, while missing `Fuel_Type` values are handled using the mode.

## Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Google Colab**
* **Jupyter Notebook (.ipynb)**

## Python Concepts Used

This project provides practical experience with:

* DataFrames
* Lists and dictionaries
* `df.shape`
* `df.loc[]`
* `df.iloc[]`
* `pd.concat()`
* `isnull()`
* `duplicated()`
* `drop_duplicates()`
* `fillna()`
* `median()`
* `mode()`
* Boolean filtering
* CSV file creation using `to_csv()`

## Project Workflow

```text
Create Dataset
      ↓
Introduce Data Quality Issues
      ↓
Initial Data Inspection
      ↓
Check Missing Values
      ↓
Check Duplicate Records
      ↓
Check Duplicate IDs
      ↓
Identify Inconsistent Values
      ↓
Identify Invalid Numerical Values
      ↓
Identify Invalid Years
      ↓
Clean the Dataset
      ↓
Validate the Cleaned Data
```

## Key Findings

The project demonstrates that even a small dataset can contain multiple types of data-quality problems.

The initial quality assessment identified:

* **53 rows**
* **10 columns**
* **2 duplicate rows**
* Missing values in `Price`, `Mileage`, and `Fuel_Type`
* Duplicate `Car_ID`
* Inconsistent categorical values
* Negative numerical values
* Invalid year values

After the cleaning steps, the project verifies that missing values and complete duplicate records have been addressed.

## Project File

**`YuvaIntern_Automotive_Data_Cleaning.ipynb`**

The notebook contains the complete Python code, data-quality checks, cleaning steps, and outputs.

## Author

**Mohammed Hassan**

Data Analyst / Data Science Learner

This project was completed as part of a practical data-quality and data-cleaning exercise.
