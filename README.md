# Crowdfunding Campaign Analysis

## Overview of Project
In this project, with the use of Excel, analysis will be made on Kickstarter data of over 4000 fundraising campaigns to help a playwright get an idea of how  crowdfunding campaigns fare based on certain factors. 

### Purpose
The main purpose of this analysis is to find out how the goals set for campaigns as well as the launch dates of the campaigns affect the outcome of different fundraising campaigns.


## Analysis and Challenges 


### Analysis of Outcomes Based on Launch Date

In performing analysis of outcomes based on launch date, a new column, "Years" was created from the "Date Created Conversion" column on the Kickstarter worksheet. A pivot table was then created from the Kickstarter worksheet onto a new sheet labeled "Theater Outcomes by Launch Date". The pivot table was filtered based on "Parent Category" and "Years". 'Outcomes' was placed in both the Columns and Values areas, and Date Created Conversion" was placed in the Rows. "Quarters" and "Years2" were auto-populated in the Rows field but they had to be removed so we can get the Row to show months of the year from January to December. The "Parent Category" was filtered to show only the data for "theater" and the "Column Labels" was sorted in descending order then filtered to show only "successful", "canceled" and "failed" outcomes. 

The final data obtained in the pivot table was then used to create the line chart below to show the relationship between outcomes and launch month:

![Image]( https://github.com/GerlechJen/kickstarter-analysis/blob/main/RESOURCES/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals

In performing analysis of outcomes based on goals, we wanted to be able to visualize the percentage of failed, successful and canceled plays based on the goal set for the campaign. A new sheet was created and labelled "Outcomes Based on Goals". Eight colums were created on this sheet with the following column headings Goal,
Number Successful, Number Failed, Number Canceled, Total Projects, Percentage Successful, Percentage Canceled and Percentage Failed.The Goal column had dollar ranges to enable the analysis to be made based on goal amount.
Using COUNTIFS() function, the "Number Successful", "Number Failed", and "Number Canceled" columns were filled by filtering on the Kickstarter "outcome" column, on the "Goal" amount column using the range of goals created , and on the "Subcategory" column using "plays" as the criteria. The total projects column was obtained using the sum function on the number of successful, failed, and canceled projects for each row.The percentage of successful, failed, and canceled projects were then calculated for each row. 

Based on the data in the table, the line chart below was created to visualize the relationship between the goal-amount ranges and the percentage of successful, failed, or canceled projects.

![image1]( https://github.com/GerlechJen/kickstarter-analysis/blob/main/RESOURCES/Outcomes_vs_Goals.png)
 
### Challenges and Difficulties Encountered

## Results

These are some conclusions that can be drawn from analyzing the theater outcomes based on launch date chart :
1. The month of May had the highest number of successful outcomes with 111 successful campaigns making it the best and recommended month to launch a campaign.
2. The month of December had the least number of successful campaigns with just 37 successful campaigns so as much as possible a campaign should not be launched in December. 

From the outcomes based on goals chart, it can be concluded that the goal set does not have a significant effect on the success or failure of the campaign. When the goal started at less than $1,000 the success rate kept on decreasing with increase in goal set up to $29,999. However, after that set goal when the goal kept increasing the success rate started going up for a while before decreasing to 0 at $45,000 to $49,999 and the finally increasing again to 13% at more than $50,000 goal.So it can be concluded that the goals set for a campaign does not have an effect on the success or failure of the campaign.


There were some limitations on the data set. First of all, 

Some other possible tables and/or graphs that we could create include::
1. We could create a graph to study if the duration of a fundraising campaign has an influence on the outcome.
2. We could also create a graph to check whether backers count has an influence on the success or failure of a fundraising campaign. 

