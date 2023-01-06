# MatPlotLib Challenge

![image](https://user-images.githubusercontent.com/112406455/210905367-d528947b-4897-49ae-a416-82545974dc63.png)

## Background
You've just joined Pymaceuticals, Inc., a new pharmaceutical company that specializes in anti-cancer medications. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

As a senior data analyst at the company, you've been given access to the complete data from their most recent animal study. In this study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

The executive team has tasked you with generating all of the tables and figures needed for the technical report of the clinical study. They have also asked you for a top-level summary of the study results.

### Prepare the Data
* Run the provided package dependency and data imports, and then merge the mouse_metadata and study_results DataFrames into a single DataFrame.

* Display the number of unique mice IDs in the data, and then check for any mouse ID with duplicate time points. Display the data associated with that mouse ID, and then create a new DataFrame where this data is removed. Use this cleaned DataFrame for the remaining steps.

* Display the updated number of unique mice IDs.
<img width="1440" alt="Screen Shot 2022-10-26 at 9 40 31 AM" src="https://user-images.githubusercontent.com/112406455/198064005-dd301b1b-aff5-4cce-abb4-354b8ab0f8ae.png">
<img width="1440" alt="Screen Shot 2022-10-26 at 10 07 33 AM" src="https://user-images.githubusercontent.com/112406455/198064226-2558248d-87e4-436c-8408-6e770fe46256.png">

### Generate Summary Statistics
Create a DataFrame of summary statistics. Remember, there is more than one method to produce the results you're after, so the method you use is less important than the result.

Your summary statistics should include:

* A row for each drug regimen. These regimen names should be contained in the index column.

* A column for each of the following statistics: mean, median, variance, standard deviation, and SEM of the tumor volume.

Using a groupby and the summary statistical methods:
<img width="1440" alt="Screen Shot 2022-10-26 at 9 41 06 AM" src="https://user-images.githubusercontent.com/112406455/198064950-7006bd36-515f-4c63-b6ae-2f62b1498040.png">
Using the aggregation method in a single line:
<img width="1440" alt="Screen Shot 2022-10-26 at 9 41 27 AM" src="https://user-images.githubusercontent.com/112406455/198065148-75a93ace-51c6-4055-bdc9-6e5779392aa9.png">

### Create Bar Charts and Pie Charts
1. Generate two bar charts. Both charts should be identical and show the total number of time points for all mice tested for each drug regimen throughout the study.

* Create the first bar chart with the Pandas DataFrame.plot() method.
<img width="1440" alt="Screen Shot 2022-10-26 at 9 41 36 AM" src="https://user-images.githubusercontent.com/112406455/198065845-6c42a273-9ed1-42bd-b53c-5b5960b91c9d.png">

* Create the second bar chart with Matplotlib's pyplot methods.
<img width="1440" alt="Screen Shot 2022-10-26 at 9 41 42 AM" src="https://user-images.githubusercontent.com/112406455/198065923-4cd596f1-e985-48b7-91a7-992e08fa2e15.png">
2. Generate two pie charts. Both charts should be identical and show the distribution of female versus male mice in the study.

* Create the first pie chart with the Pandas DataFrame.plot() method.
<img width="1440" alt="Screen Shot 2022-10-26 at 9 41 51 AM" src="https://user-images.githubusercontent.com/112406455/198066885-7bb87726-efe3-4730-a618-932d379854ed.png">

* Create the second pie chart with Matplotlib's pyplot methods.
<img width="1440" alt="Screen Shot 2022-10-26 at 9 41 59 AM" src="https://user-images.githubusercontent.com/112406455/198067067-2947e42b-5f5e-4cd2-8d1e-53798fec3af6.png">

### Calculate Quartiles, Find Outliers, and Create a Box Plot
1. Calculate the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, calculate the quartiles and IQR, and determine if there are any potential outliers across all four treatment regimens. Use the following substeps:

* Create a grouped DataFrame that shows the last (greatest) time point for each mouse. Merge this grouped DataFrame with the original cleaned DataFrame.

* Create a list that holds the treatment names as well as a second, empty list to hold the tumor volume data.

* Loop through each drug in the treatment list, locating the rows in the merged DataFrame that correspond to each treatment. Append the resulting final tumor volumes for each drug to the empty list.

* Determine outliers by using the upper and lower bounds, and then print the results.
<img width="1440" alt="Screen Shot 2022-10-26 at 9 42 10 AM" src="https://user-images.githubusercontent.com/112406455/198067874-63248029-99e2-436f-9152-9b3dcbef7c0d.png">

2. Using Matplotlib, generate a box plot that shows the distribution of the final tumor volume for all the mice in each treatment group. Highlight any potential outliers in the plot by changing their color and style.
<img width="1440" alt="Screen Shot 2022-10-26 at 10 34 50 AM" src="https://user-images.githubusercontent.com/112406455/198070782-af4720bd-ebcd-4a37-af3a-6e3cae9aef40.png">

### Create a Line Plot and a Scatter Plot
* Select a mouse that was treated with Capomulin, and generate a line plot of tumor volume versus time point for that mouse.
<img width="1440" alt="Screen Shot 2022-10-26 at 9 42 23 AM" src="https://user-images.githubusercontent.com/112406455/198068347-658ed42d-fc34-44d3-b3e0-459ee1fd5aa0.png">

* Generate a scatter plot of tumor volume versus mouse weight for the Capomulin treatment regimen.
<img width="1440" alt="Screen Shot 2022-10-26 at 9 42 28 AM" src="https://user-images.githubusercontent.com/112406455/198068559-f60a1388-375e-4c1a-8da3-09918d7ddc38.png">

### Calculate Correlation and Regression
* Calculate the correlation coefficient and linear regression model between mouse weight and average tumor volume for the Capomulin treatment.

* Plot the linear regression model on top of the previous scatter plot.
<img width="1440" alt="Screen Shot 2022-10-26 at 9 42 37 AM" src="https://user-images.githubusercontent.com/112406455/198068776-75e65963-9f24-4ead-8d42-6c68016b1a4e.png">

### Analysis
* In this study, the correlation between mouse weight and the average tumor volume was 0.84, indicating a strong positive correlation between the two variables. 
* The mean tumor volume for Capomulin and Ramicane were significantly lower than their counterparts, suggesting they may be the most promising drug regimens.
* Taking a look at the bar plot for the total number of timepoints for all mice tested per regimen, it appears that there is an almost even distribution, with Capomulin and Ramican having the most mice and Propriva having the least. 

### Instructions on how to run the code properly:
* Download the repository onto you computer
* Open the repository in Jupiter Notebook
* Select the mainscript.ipynb in the Pymaeceuticals folder
* Select the "Kernel" tab and click "Restart Kernel and Clear all Outputs"
* Then proceed to hit shift + enter to cycle through the script cell by cell
* The code is accompanied by an outline to walk you through the process step by step

### References
Data generated by MockarooLinks to an external site., LLC (2022). Realistic Data Generator.
