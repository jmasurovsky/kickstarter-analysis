# kickstarter-analysis
Performing analysis on Kickstarter data to uncover trends

# Kickstarting with Excel

## Overview of Project

### Purpose

An analysis of Kickstarter data was performed to assist Louise in determining the fundraising goal for her play in the U.S. and musical in G.B. Data suggested a fundraising goal of $5,049 for her play in the U.S. since the mean pledged is greater than the mean goal. For her musical, a fundraising goal of under the mean of £4,000, and closer to the median of £2,000. The purpose of this project was to create visualizations of Kickstarter campaign, focusing on theater and plays, outcomes based on their fundraising goals and launch dates. 


## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

To create the visualization of theater outcomes based on launch date, a years column was created using the YEAR() function on the Date created conversion column. The reason for this was to group the data by month in the pivot chart. I then created a pivot chart to  using the Parent Category column, so that it can filter theater outcomes, and the Year column, which filtered all the rows by month. The columns showed results of outcomes of those successful, failed and canceled, in that order, while "live" was removed. At this point, a line chart was created to show the relationship between campaign outcomes and their launch month.


### Analysis of Outcomes Based on Goals

In order to visualize the relationship between campaign outcome goals, of plays specifically, that were successful, failed, or canceled a new sheet was created with 8 the following columns: Goal, Number Successful, Number Failed, Number Canceled, Total Projects, Percentage Successful, Percentage Failed, and Percentage Canceled. The Goal column was split to show the following count values at a fundraising goal range: 
	![img_1](https://github.com/jmasurovsky/kickstarter-analysis/blob/master/Resources/Outcomes_Based_on_Goals_Table.png). 

The COUNTIFS() function was used to calculate the # of successful, failed, and canceled campaigns based on the goal range. The COUNTIFS() function had to have multiple criteria, filtered by the goal amount, the campaign outcome, and plays from the subcategory column. The percentages of each were calculated and used as the y-axis when visualizing as a line chart, while x-axis had values from the Goal column.


### Challenges and Difficulties Encountered

A challenge I encountered for Deliverable 1, was initially not understanding why the YEAR() function was showing a date (see example below), and that was because the Year column was set to "short date", therefore it had to be converted to "general". 
	
![img_2](https://github.com/jmasurovsky/kickstarter-analysis/blob/master/Resources/Years_challenge_example.png)


The challenge I had in Deliverable 2, was repetitive writing and editing the COUNTIFS() function for each different goal and outcome.  


## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

	1. Taking a look at the line chart below, successful theater campaigns peak in May remain at large number to July, while at the same time campaign outcomes that failed peak in May, as well. Although, in May, outcomes failed are at its highest count number of 52 failed, it is at a lower percentage at 31%, compared to failed outcomes in December, at 47%. Louise should plan to launch her play in May. The trend line for canceled theater shows remain consistent throughout, except for January which has the highest count and October, which contains no data.
	
	![img_3](https://github.com/jmasurovsky/kickstarter-analysis/blob/master/Resources/Theater_Outcomes_vs_Launch.png)



- What can you conclude about the Outcomes based on Goals?

	1. The line chart below shows trends for the most successful play Kickstarter campaign outcomes are based on fundraising goals of less than 1,000, from 1,000 to 4,999, 35,000 to 39,999, and 40,000 to 44,999. The least successful plays had a fundraising goal of 25,000 to 29,999, 30,000 to 34,999 45,000 to 49,999, and greater than 50,000.
	
	![img_4](https://github.com/jmasurovsky/kickstarter-analysis/blob/master/Resources/Outcomes_vs_Goals.png)


- What are some limitations of this dataset?
Outliers?

	1. For deliverable 2, there were possible outliers in the dataset for the outcomes based on goals causing the dataset to be skewed to the right. Looking at the table, there number of total projects decreases significantly, thus some of the larger Goal column ranges might not be as statistically significant as the smaller ones such as less than 1,000 all the way to 14,999.

	2. A possible limitation of the dataset is the lack of context for why a theater campaign outcome failed based on their launch date, especially during the month of May when the highest number of successful theater Kickstarters and the highest failed. Another limitation could be for deliverable 1, there is no data for canceled theater shows that launched in October, but that does not guarantee a show launching in October will never be canceled.

	3. Lastly, instructions for the assignment were to label a sheet "Theater Outcomes Based on Launch Date" and was limited by the Excel character limit and had to rename it "Theater Outcomes by Launch Date".

- What are some other possible tables and/or graphs that we could create?
	
	1. Creating a histogram of outcomes based on goals would show the data is skewed. Since there are a lot more campaigns based on a goal of 1,000 to 4,999, creating a table that includes more breaks within that range to spread the data out more and have a better sample. 

	2. Creating a table and line chart showing the relationship of successful outcome campaigns at each goal range to the 'Years' column would create additional insight on when to launch a Kickstarter campaign at a more specific fundraising goal.



