# kickstarter_analysis

## Overview of Project

### Purpose

This project analyzes kickstarter project data to better inform project strategies and assess how a new project has fared compared to its peers, including optimal release dates and funding goals by comparing data from successful, failed, and canceled preexisting projects. 

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

A line chart showing seasonal trends in Kickstarter theatre project outcomes was produces by creating a pivot table (https://github.com/nabouzaid/kickstarter_analysis/blob/444162307a611444de69d865af3036d6dfc05c99/outcomes_vs_launch_pivot.png
) counting the instances of successful, failed, and canceled project outcomes based on the month a project was started. Since the original data set contained a wide variety of projects, this table was filtered to show only theatre projects. Showing the number of outcomes by month allowed the resulting line chart to show broad seasonal trends in project outcomes. 

### Analysis of Outcomes Based on Goals

A chart (https://github.com/nabouzaid/kickstarter_analysis/blob/444162307a611444de69d865af3036d6dfc05c99/outcomes_vs_goals_chart.png) showing the outcomes of Kickstarter play projects based on goals was created using the COUNTIFS function to isolate the number of failed, successful, and canceled projects falling under the subcategory of plays and within successive goal intervals. The percentage of successful, failed, and canceled projects was calculated using the total number of play projects within each interval. 

### Challenges and Difficulties Encountered

There were many opportunities for mistakes in using the COUNTIFS function to calculate the number of successful, failed, and canceled within each goal interval since each function used unique manually entered data. To somewhat reduce the number of formulas to be manually entered, I entered the text outcomes (successful, failed, canceled) in cells corresponding to the outcome columns so that they could be included in the COUNTIFS formulas as relative references, reducing the number of formulas to be entered by 2/3s.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

The number of successful theatre project outcomes was highest in the summer months, with an increase of 98% from April to May (https://github.com/nabouzaid/kickstarter_analysis/blob/444162307a611444de69d865af3036d6dfc05c99/Theater_Outcomes_vs_Launch.png). The increase was disproportionate with the rise in total projects, although the number of projects overall increased, with an an 80% rise in the total number of projects from April to May. The number of successful projects nearly converged with the number of failed projects in December, with a distinct decrease in the fall. There was a consistently small number of cancelled projects with a slightly higher number in January. 

- What can you conclude about the Outcomes based on Goals?

The share of projects with a successful outcome was highest in the very low funding intervals, with the percentage of failed projects exceeding the percentage of successful projects at the $15 000 to $19 999 interval. https://github.com/nabouzaid/kickstarter_analysis/blob/444162307a611444de69d865af3036d6dfc05c99/Outcomes_vs_Goals.png

- What are some limitations of this dataset?

The analysis of the outcomes of plays based on their goals suffered due to few instances of play projects at higher goal amounts, with only 4% of projects having a goal of $2500 or more. Furthermore, no play projects in this data set were canceled.  

- What are some other possible tables and/or graphs that we could create?

Although the graph showing the theatre outcomes based on launch date demonstrates a distinct spike in successful play projects in May, it is unclear how much of seasonal outcome trends are accounted for by an increase in projects overall based on this graph. A stacked line or bar chart, such as a 100% stacked bar chart shows a more moderate increase in successful May projects since it only reflects the share of the total successful projects (https://github.com/nabouzaid/kickstarter_analysis/blob/444162307a611444de69d865af3036d6dfc05c99/alternative_launch_date_outcomes.png)
