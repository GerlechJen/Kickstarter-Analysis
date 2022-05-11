# Crowdfunding Campaign Analysis

## Overview of Project
In this project, with the use of Excel, analysis will be made on Kickstarter data of over 4000 fundraising campaigns to help a playwright get an idea of how  crowdfunding campaigns fare based on certain factors. 

### Purpose
The main purpose of this analysis is to find out how the goals set for campaigns as well as the launch dates of the campaigns affect the outcome of different fundraising campaigns.


## Analysis and Challenges 


### Analysis of Outcomes Based on Launch Date

In performing analysis of outcomes based on launch date, a new column, "Years" was created from the "Date Created Conversion" column on the Kickstarter worksheet. A pivot table was then created from the Kickstarter worksheet onto a new sheet labeled "Theater Outcomes by Launch Date". The pivot table was filtered based on "Parent Category" and "Years". 'Outcomes' was placed in both the Columns and Values areas, and Date Created Conversion" was placed in the Rows. "Quarters" and "Years2" were auto-populated in the Rows field but they had to be removed so we can get the Row to show months of the year from January to December. The "Parent Category" was filtered to show only the data for "theater" and the "Column Labels" was sorted in descending order then filtered to show only "successful", "canceled" and "failed" outcomes. 

The final data obtained in the pivot table was then used to create the line chart below to show the relationship between outcomes and launch month.

![Image]( https://github.com/GerlechJen/kickstarter-analysis/blob/main/RESOURCES/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals

In performing analysis of outcomes based on goals, the objective was to be able to visualize the percentage of failed, successful and canceled plays based on the goal set for the campaign. A new sheet was created and labelled "Outcomes Based on Goals". Eight colums were created on this sheet with the following column headings: Goal,
Number Successful, Number Failed, Number Canceled, Total Projects, Percentage Successful, Percentage Canceled and Percentage Failed. The Goal column had dollar ranges to enable the analysis to be made based on goal amount.
Using COUNTIFS() function, the "Number Successful", "Number Failed", and "Number Canceled" columns were filled by filtering on the Kickstarter "outcome" column, on the goal-amount column using the range of goals created , and on the "Subcategory" column using "plays" as the criteria. The total projects column was obtained using the sum function on the number of successful, failed, and canceled projects for each row.The percentage of successful, failed, and canceled projects were then calculated for each row. 

Based on the data in the table, the line chart below was created to visualize the relationship between the goal-amount ranges and the percentage of successful, failed, or canceled projects.

![image1]( https://github.com/GerlechJen/kickstarter-analysis/blob/main/RESOURCES/Outcomes_vs_Goals.png)
 
### Challenges and Difficulties Encountered

While performing the analysis some challenges encountered were:
1. It was hard to detect when errors occured. Knowing the outcome expected in the table is what served as a guidance to know whether an error has been made in the calculations at all. To overcome this challenge I double-checked my work and compared my results with the expected results often.
2. While using the countifs function, moving from sheet to sheet resulted in errors. To overcome this I remained on the main kickstarter sheet while selecting the different columns for accurate results.

## Results

- These are some conclusions that can be drawn from analyzing the "Theater Outcomes Based on Launch Date" chart :
1. The month of May had the highest number of successful outcomes with 111 successful campaigns making it the best and recommended month to launch a campaign.
2. The month of December had the least number of successful campaigns with just 37 successful campaigns so as much as possible a campaign should not be launched in December. 

- From the "Outcomes Based on Goals" chart, it can be concluded that the goal set does not have any relationship with  the success or failure of the campaign. The number of canceled campaigns was 0 throughout so our conclusion will be based on the results for the failed and successful campaigns. When the goal started at less than $1,000 the success rate was 76% and it kept on decreasing with increase in goal till it got to a goal of $30000 to $34999 where it increased by 7%. It increased further by 60% for both $35000 to $39,999 and $40000 to $44999 goals. After that, it decreased once again to 0% for $45,000 to $49,999 goal and finally increased again to 13% for goal of $50000 or more. The opposite results can be seen when looking at the chart based on Percentage Failed. 

  Therefore, for the Outcomes Based on Goals, it does not follow any specific pattern and a relationship cannot be established between the goals set and the outcome. 

- There were some limitations on the data set. Over 400 of the campaigns had 0 backers count and such campaigns had their outcomes classified as either "failed" or "canceled". The factors that influenced the type of classification assigned is unclear. Campaigns with 0 backers count should have had the same classification. This can affect the accuracy of our data.  

- Some other possible graphs could have been created for analysis. Some of them include:
1. A graph to study if the duration of a fundraising campaign has an influence on the outcome.
2. A graph to check whether backers count has an influence on the success or failure of a fundraising campaign. 

