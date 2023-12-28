# SCC Treatment Analysis with Matplotlib

![image](https://user-images.githubusercontent.com/112406455/210905367-d528947b-4897-49ae-a416-82545974dc63.png)

## Background
Pymaceuticals, Inc., a pioneering pharmaceutical company, has recently embarked on a crucial study focusing on squamous cell carcinoma (SCC), a common form of skin cancer. In their latest animal study, they explored the efficacy of various drug regimens, including their primary drug, Capomulin, on 249 mice with SCC tumors over a 45-day period. As a senior data analyst, my role involves analyzing this extensive data to compare the performance of Capomulin against other treatments and providing comprehensive insights through tables, figures, and a summary of the study results. This study is a significant step in Pymaceuticals' mission to advance cancer treatment and improve patient outcomes.
## Objective 
1. **Prepare the Data**
* Execute package dependencies and data imports.
* Merge the `mouse_metadata` and `study_results` DataFrames.
* Identify and handle any duplicate mouse IDs.
* Use the cleaned DataFrame for subsequent analyses.

2. **Generate Summary Statistics**
*Develop a DataFrame detailing summary statistics for each drug regimen, including mean, median, variance, standard deviation, and SEM of tumor volume.

3. **Create Bar and Pie Charts**
* Utilize Pandas and Matplotlib to generate two identical bar charts showing time points for each drug regimen.
* Create two identical pie charts displaying the gender distribution of mice using both Pandas and Matplotlib methods.

4. **Quartiles, Outliers, and Box Plot Analysis**
* Analyze the final tumor volume for key treatments: Capomulin, Ramicane, Infubinol, and Ceftamin.
* Calculate quartiles, IQR, and identify potential outliers.
* Generate a box plot for each treatment group, highlighting any outliers.

5. **Line Plot and Scatter Plot Creation**
* Select a Capomulin-treated mouse and plot tumor volume versus time point.
* Produce a scatter plot illustrating tumor volume versus mouse weight for the Capomulin regimen.

6. **Correlation and Regression Calculation**
* Determine the correlation coefficient between mouse weight and average tumor volume for Capomulin-treated mice.
* Fit a linear regression model and overlay this on the scatter plot.