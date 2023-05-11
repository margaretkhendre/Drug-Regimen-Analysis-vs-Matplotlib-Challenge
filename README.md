# Matplotlib Challenge

## Background
You've just joined Pymaceuticals, Inc., a new pharmaceutical company that specializes in anti-cancer medications. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

As a senior data analyst at the company, you've been given access to the complete data from their most recent animal study. In this study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

The executive team has tasked you with generating all of the tables and figures needed for the technical report of the clinical study. They have also asked you for a top-level summary of the study results.

## Instructions
This assignment is broken down into the following tasks:

- Prepare the data.

- Generate summary statistics.

- Create bar charts and pie charts.

- Calculate quartiles, find outliers, and create a box plot.

- Create a line plot and a scatter plot.

- Calculate correlation and regression.

## Prepare the Data
1. Run the provided package dependency and data imports, and then merge the mouse_metadata and study_results DataFrames into a single DataFrame.

2. Display the number of unique mice IDs in the data, and then check for any mouse ID with duplicate time points. Display the data associated with that mouse ID, and then create a new DataFrame where this data is removed. Use this cleaned DataFrame for the remaining steps.

3. Display the updated number of unique mice IDs.

<img width="1077" alt="Screenshot 2023-05-03 at 3 48 51 PM" src="https://user-images.githubusercontent.com/121995835/236030864-673ff32c-7053-477d-9f7b-42f61044ab93.png">

## Generate Summary Statistics
Create a DataFrame of summary statistics. Remember, there is more than one method to produce the results you're after, so the method you use is less important than the result.

**Summary statistics should include:**

- A row for each drug regimen. These regimen names should be contained in the index column.

- A column for each of the following statistics: mean, median, variance, standard deviation, and SEM of the tumor volume.

<img width="1077" alt="Screenshot 2023-05-03 at 3 50 23 PM" src="https://user-images.githubusercontent.com/121995835/236031289-b688fcd4-ad63-4ffa-9431-d13ac34caabd.png">

## Create Bar Charts and Pie Charts
1. Generate two bar charts. Both charts should be identical and show the total total number of rows (Mouse ID/Timepoints) for each drug regimen throughout the study.

- Create the first bar chart with the Pandas DataFrame.plot() method.

<img width="911" alt="Screenshot 2023-05-03 at 3 51 29 PM" src="https://user-images.githubusercontent.com/121995835/236031633-fec99590-77c0-4629-9e61-4b62f800af32.png">

- Create the second bar chart with Matplotlib's pyplot methods.

<img width="1025" alt="Screenshot 2023-05-03 at 3 52 03 PM" src="https://user-images.githubusercontent.com/121995835/236031824-38d3b382-f28f-4759-9c24-60c749db454e.png">

2. Generate two pie charts. Both charts should be identical and show the distribution of female versus male mice in the study.

- Create the first pie chart with the Pandas DataFrame.plot() method.

<img width="735" alt="Screenshot 2023-05-03 at 3 52 42 PM" src="https://user-images.githubusercontent.com/121995835/236032005-1dd3f617-6439-4821-906a-aefbbb3eae77.png">

- Create the second pie chart with Matplotlib's pyplot methods.

<img width="735" alt="Screenshot 2023-05-03 at 3 53 03 PM" src="https://user-images.githubusercontent.com/121995835/236032129-4776fa62-fffc-448b-8f1d-3184d4dd590f.png">

## Calculate Quartiles, Find Outliers, and Create a Box Plot
1. Calculate the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, calculate the quartiles and IQR, and determine if there are any potential outliers across all four treatment regimens. Use the following substeps:

- Create a grouped DataFrame that shows the last (greatest) time point for each mouse. Merge this grouped DataFrame with the original cleaned DataFrame.

- Create a list that holds the treatment names as well as a second, empty list to hold the tumor volume data.

- Loop through each drug in the treatment list, locating the rows in the merged DataFrame that correspond to each treatment. Append the resulting final tumor volumes for each drug to the empty list.

- Determine outliers by using the upper and lower bounds, and then print the results.

<img width="735" alt="Screenshot 2023-05-03 at 3 54 24 PM" src="https://user-images.githubusercontent.com/121995835/236032794-8e7e2ae0-0193-433d-92af-f035433484a9.png">

2. Using Matplotlib, generate a box plot that shows the distribution of the final tumor volume for all the mice in each treatment group. Highlight any potential outliers in the plot by changing their color and style.

<img width="735" alt="Screenshot 2023-05-03 at 3 53 47 PM" src="https://user-images.githubusercontent.com/121995835/236032639-50190726-5b0d-4ff2-a5f0-2d6de221e76a.png">

## Create a Line Plot and a Scatter Plot
1. Select a single mouse that was treated with Capomulin, and generate a line plot of tumor volume versus time point for that mouse.

<img width="735" alt="Screenshot 2023-05-03 at 3 55 26 PM" src="https://user-images.githubusercontent.com/121995835/236033079-7d75208d-9bab-47c3-8c7d-7516c3a1e943.png">

2. Generate a scatter plot of mouse weight versus average observed tumor volume for the entire Capomulin treatment regimen.

<img width="735" alt="Screenshot 2023-05-03 at 3 55 00 PM" src="https://user-images.githubusercontent.com/121995835/236032954-84729c22-d57f-4550-9347-4b9e1cbed4aa.png">

## Calculate Correlation and Regression
1. Calculate the correlation coefficient and linear regression model between mouse weight and average observed tumor volume for the entire Capomulin treatment regimen.

2. Plot the linear regression model on top of the previous scatter plot.

<img width="732" alt="Screenshot 2023-05-03 at 3 55 55 PM" src="https://user-images.githubusercontent.com/121995835/236033212-adb5c280-5c1d-4e1a-8881-f41cecd27298.png">

