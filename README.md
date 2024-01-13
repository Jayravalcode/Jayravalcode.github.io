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
4. **Library are used**
   - pandas:- for , numpy, matplotlib, seaborn, and statsmodels.tsa.arima.model

## Questions to Address

1. **Total Tons Moved:**
   - Determine the total tons moved by each truck.
   - Calculate the combined total tons moved by all trucks.
   - The code groups the DataFrame (df3) by the "MACH_SER_NO" column, calculates the sum of "PAYLD_WT" for each truck, and computes the combined total tons moved by summing up all trucks' payload weights. The          results are rounded to two decimal places and displayed.

2. **Average Tones moved per truck:**
   - average_tons = df3.groupby('MACH_SER_NO')['PAYLD_WT'].mean().round(2)
   - The provided code calculates the average payload weight for each truck by grouping the DataFrame (df3) based on the "MACH_SER_NO" column and computing the mean of the "PAYLD_WT" column for each group.

3. **Tones per Gallon per distance travelled matrix for each truck and all trucks:**
   - For example tons per gallon is (x). for finding Tones per gallon per distance we divided the tons per gallon by distance coverd by truck. we consider loaded travel distance for finding the tones per gallon        per distance.
   - use _replace(0, np.nan)_ to replace nan value with 0.
4. **Which truck is running most efficient and which truck is running most inefficient as per as the matrix in item number 3?**
   - calculates the average efficiency (Tons per Gallon per Distance) for each truck by grouping the DataFrame (df3) based on the "MACH_SER_NO" column.
   - To identify the most efficient and inefficient trucks, it then determines the truck with the highest average efficiency using idxmax() and the truck with the lowest average efficiency using idxmin().
5. **Show Visually which truck has travelled empty most distance.**
   - calculates the total empty travel distance for each truck by grouping the DataFrame (df3) based on the "MACH_SER_NO" column and summing up the "EMTY_TRAV_DSTNC" column for each group.
   - It then identifies the truck with the maximum total empty travel distance using idxmax() to get the corresponding index and max() to get the maximum value.
   - ![image](https://github.com/Jayravalcode/Truck_Travel_prediction/assets/100700949/49e8d619-4040-4173-968a-7551d345dfd4)
6. **Show visually which truck has Max and Min Gear Shifts per Mile**
   - calculates and prints the total gear shifts per mile for each truck in the DataFrame df3. Additionally, it identifies and prints the truck with the maximum and minimum gear shifts per mile along with their        respective values.
      ![image](https://github.com/Jayravalcode/Truck_Travel_prediction/assets/100700949/b1ea7ed5-9c3e-496d-9dc4-9a9434d9452e)
7. **Which truck has max stop time in empty**
   -  identifies the row with the maximum value in the "EMTY_STOP_TM" column in the DataFrame df3. It then extracts the truck and time information from that row and prints a statement with the truck and its             corresponding maximum stop time in the empty state.
   -  The truck with the maximum stop time in empty state is: Truck 16
         The corresponding time is: 12149.0
8. **Total distance travelled by each truck as well as all trucks combined.**
   - calculates the total loaded and empty travel distances for each truck by grouping the DataFrame (df3) based on the "MACH_SER_NO" column. It then prints the         overall sum of loaded and empty travel distances for all trucks, rounded to two decimal places.
9. **Predict the future production capacity for each truck (Prediction & forecasting needs to be made for next 15 days)**
     1. Import Libraries:
         Import necessary libraries for data manipulation, plotting, ARIMA modeling, and multiprocessing.
     2. Prepare DataFrame:
         Convert date and time columns to a datetime format and set them as the DataFrame index.
     3. ARIMA Model Parameters:
         Set parameters for the ARIMA model, including the order and the number of steps to forecast.
     4. Define Forecasting Function:
         Create a function that takes a truck's name, performs time series forecasting using ARIMA, and plots actual vs. forecasted values.
     5. Multiprocessing for Parallelization:
         Use multiprocessing to parallelize the forecasting process for each unique truck.
     6. Results:
         Store and display the results, including the truck's name and the forecasted values.

