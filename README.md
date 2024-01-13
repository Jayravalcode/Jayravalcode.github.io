# Truck Transportation Prediction

## Problem Statement

The objective is to analyze various elements related to truck transportation.

## Techniques Used

- Data Science
- Data Analysis
- Data Preprocessing
- Data Cleaning

## Basic Steps

1. **Data Collection:**
   - Utilize Google Colab to store and access CSV files via Google Drive.

2. **Comparison of CSV Files:**
   - Compare both CSV files based on their column names.

3. **Data Processing Steps:**
   a. Check the data types using `df1.dtypes`.
   b. Rename or fill important columns:
      - Fill in the name where the column name is unnamed.
      - Change the name of the required column.

## Questions to Address

1. **Total Tons Moved:**
   - Determine the total tons moved by each truck.
   - Calculate the combined total tons moved by all trucks.
   - The code groups the DataFrame (df3) by the "MACH_SER_NO" column, calculates the sum of "PAYLD_WT" for each truck, and computes the combined total tons moved by summing up all trucks' payload weights. The          results are rounded to two decimal places and displayed.
