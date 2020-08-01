# Kickstarting with Excel

## Overview of Project

### Purpose
The purpose of this analysis is to assist Louise in uncovering how different campaigns do in relation to their launch dates and their funding goals. This will be unraveled by creating analytical visualizations and analysis from campaigns outcomes based on their launch dates and funding goals from the kickstarter dataset. The main focus will be theater “category” and play “subcategory”. Conclusions will be reported based on the analyses that will be created by tables and charts. 

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
 

![Outcomes Based on Launch Date](resources/Theater_Outcomes_vs_Launch.png)

This line chart was derived from a pivot table created from the kickstarter dataset. To create the appropriate pivot table the following fields were placed in the designated areas. In the filter area: parent category and years. In the columns area: outcomes. In the rows area: date created conversion. Lastly in the values areas: outcomes which changes to count of outcomes. After filling in the areas with the pivot table fields, a pivot table appears. From here the parent category is filtered to be theater. The outcomes column is filtered to show successful, failed, and canceled as well as in descending order. As for the row labels are changed to display the months of the year by grouping. The pivot table presents the outcomes relationship with the launch dates (month) per the parent category of theater. The next step is to use this pivot table and create a line chart to have a visualization of the data's relationship. Proceed to the pivotable analyze tab and use pivotchart. Then select the design tab and use the change chart type, the pivot line chart above is the line with markers style.  

### Analysis of Outcomes Based on Goals

 

![Outcomes Based On Goal](resources/Outcomes_vs_Goals.png)

This line chart was derived from a chart with goal parameters and outcome percentages. The table's first column is populated with dollar-amount ranges which will group projects based on their goal amount. The next three columns represent the number of outcomes: successful, failed, and canceled. These columns were filled by using the countifs() function. The parameters were specific per column: for the successful column it was filtered on successful (outcome), goal which was using the ranges created on the first column, and plays (subcategory). For the next to failed and canceled were filtered similar to the successful column, but with a slight change on the outcome filter. The number failed will be filtered for failed outcome and as for number canceled was filtered on canceled. The next column was the total projects, took the sum of the row that was next to. From there the percentage successful was calculated by taking the number successful dividing by the sum of total projects then changing to percent value. This was done the same way for percentage failed and percentage canceled. With this data, take the goal, percentage successful, percentage failed, and percentage canceled columns and insert a line chart. This line chart presents the outcome of the fundraising campaign based on their fundraising goal. 

### Challenges and Difficulties Encountered
One of the challenges I faced during this analysis was during the analysis of outcomes based on launch date. I had created a pivot table from the kickstarter dataset and had placed the appropriate pivot table fields in the filters, columns, rows, and values. I had trouble creating the appropriate pivot line chart from the pivot table. My first choice of pivot line chart was the stacked line with markers style, the result did not match with the chart presented on the module challenge. In order to fix this, I went back to the modules to see what the correct pivot line chart that was used. Located on module 1.3.3 the correct pivot line chart used was line with markers style. After selecting this pivot line chart style, it was an exact match with the example presented. 



## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
  - According to the theater outcomes based on launch date, two conclusions that can be drawn are that the most successful theater kickstarter campaigns start in     	May and the least successful theater kickstarter campaigns start in December.

- What can you conclude about the Outcomes based on Goals?
  - Successful kickstarter campaigns for plays have lower fundraising goal than the failed kickstarter campaigns for plays. There’s a higher success rate for         	kickstarter play campaigns that have a fundraising goal less than $1,000. As for fundraising goals between $40,000 to $49,999 this shows a higher failure           rate for kickstarter play campaigns.


- What are some limitations of this dataset?
  - A possible limitation of this dataset is the data freshness meaning the most recent year of this data is limited from 2009 to 2017. If Louise were to             	determine budgets for the kickstarter play campaign for 2020 there wouldn’t be sufficient data to assist on this. Another potential limitation would be the         lack of granular data on city and state, as US is the target country. The city and state may impact the outcome of the trends that is being shown with the           data given.


- What are some other possible tables and/or graphs that we could create?
  - For further analysis a possible table that can be created is having the same data from the “Outcomes Based on Goals” but adding another column “Percentage of     	Total Projects from Grand Total”. To do so, take the sum of the “Total Projects” column have this value in cell E14 with =sum(E2:E13) as the formula. This           value represents the grand total of the total projects for subcategory of plays. In I1 label this as “Percentage of Total Projects from Grand Total”. In I2         have =(E2/$E$14) as the formula and then drag this formula down to I13. Then change I column to percentage values. The values in this column will present the       percentage of play projects in the certain goal parameters; ultimately shows where the majority of the play fundraising campaign’s goal falls into. 
  - To represent this data in a graph, highlight column A and column I and insert a clustered column graph. This graph will give a visualization of where the         	majority of kickstarter fundraising campaigns goals reside. From this graph, it shows that majority of the play campaign’s goal fall into tier of less than         $1000 and $1000 to $4999.
