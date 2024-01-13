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
      ![Screenshot 2024-01-12 225143](https://github.com/Jayravalcode/Truck_Travel_prediction/assets/100700949/e0c10606-b663-4895-bee9-a5af5738e2c4)

## Questions to Address

1. **Total Tons Moved:**
   - Determine the total tons moved by each truck.
   - Calculate the combined total tons moved by all trucks.
   - The code groups the DataFrame (df3) by the "MACH_SER_NO" column, calculates the sum of "PAYLD_WT" for each truck, and computes the combined total tons moved by summing up all trucks' payload weights. The          results are rounded to two decimal places and displayed.

2. **Average Tones moved per truck:**
   - average_tons = df3.groupby('MACH_SER_NO')['PAYLD_WT'].mean().round(2)
   - The provided code calculates the average payload weight for each truck by grouping the DataFrame (df3) based on the "MACH_SER_NO" column and computing the mean of the "PAYLD_WT" column for each group.

3. **Tones per Gallon per distance travelled matrix for each truck and all trucks:**
   - Here we use the formula to calculate the tons per gallon like total weight
