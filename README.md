# BAN6420_Module2_Ass_Salary_Function
This is my submission for Assignment Module 2 "Salary Function" - Sodiq Otunba Learner ID 154046

# Employee Data Processing

This project processes salary data for employees and provides functionalities to extract, display, and export employee information. The project is written in Python (for data processing and export) and includes an R script (for unzipping and displaying the data).

## Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
  - [Python Functions](#python-functions)
  - [R Script](#r-script)
- [Error Handling](#error-handling)
- [Contributors](#contributors)

---

## Features

- **Import Data**: Load and process salary data.
- **Employee Function**: Search for employee details by name.
- **Data Processing**: Handles salary data using a Python dictionary.
- **Error Handling**: Graceful handling of missing data and invalid inputs.
- **Export Employee Details**: Export an employee's information to a CSV file and zip it in an "Employee Profile" folder.
- **Unzip and Display in R**: The R script unzips the employee profile folder and displays the data.

## Requirements

### Python

- Python 3.x
- pandas
- os
- zipfile
- csv

### R

- R 4.x or later

## Installation

### Python

1. Clone this repository:
   ```bash
   git clone https://github.com/your-repo/employee-data-processing.git
2. Install required Python packages:
```bash
   pip install pandas
### R
Install R from CRAN.
No additional packages are required for the R script.

### Usage
##Python Functions
1. Import the Salary Data: Ensure you have a CSV file containing the salary data. You can load this data using pandas in Python.
```bash
  import pandas as pd
  salary_data = pd.read_csv("path_to_salary_data.csv")


