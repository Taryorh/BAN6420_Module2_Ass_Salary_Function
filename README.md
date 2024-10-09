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
- [Error Handling&Logging](#error-handling&Logging)


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
  ```
### R
Install R from CRAN.
No additional packages are required for the R script.

### Usage
Pre: Launch your jupyter notebook with this command
```bash
  jupyter notebook --NotebookApp.iopub_data_rate_limit=10000000
```
## Python Functions
1. Import the Salary Data: Ensure you have a CSV file containing the salary data. You can load this data using pandas in Python.
```python
  import pandas as pd
  data = pd.read_csv("path_to_salary_data.csv")
```
2. Process the Data: A Python function process_data_as_dict processes the salary data into a dictionary for easy access:
```python
  employee_dict = process_data_as_dict(data)
  ```
3. Find Employee Details: Use the employee_details_check function to find employee details by name:
```python
  employee = employee_details_check("Employee Name",data)
  print(employee)
  ```
4. Export Employee Details: Export the found employee details to a CSV file and zip the file:
  ```python
       export_employee_details("Employee Name", employee_dict)
  ```
### R Script
After exporting the employee details, you can use the R script to unzip the folder and display the data.

1. Set working directory:
```R
setwd("path/to/Employee_Profiles")
```
2. Unzip the folder:
```R
  unzip("Employee_Profile.zip", exdir = "Employee_Profile")
```
3. Read and display data:
```R
for (file in list.files("Employee_Profile", full.names = TRUE)) {
  if (grepl("\\.csv$", file)) {
    employee_data <- read.csv(file)
    print(employee_data)
  }
}
```

# Error Handling & Logging
Missing Data: The code checks for missing columns and missing employee details, providing error messages when necessary and log it.
Invalid Input: The employee_details_check function raises an error if the employee's name is not found in the data.








