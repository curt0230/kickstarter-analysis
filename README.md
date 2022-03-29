# Kickstarting with Excel

## Overview of Project
Kickstarter is a platform on which project creators can crowdsource funding.  This project analyzes a sample Kickstarter data collected between 2009 and 2017 in order to identify trends for campaigns funding theater projects and plays.

### Purpose
The purpose of this project is to determine how successful various campaigns were relative to their launch dates and funding goals.

## Analysis and Challenges
Several metrics were derived from original Kickstarter campaign data.  Campaign start and end dates needed to be converted from Unix timestamps and the parent and subcategory needed to be parsed in order to perform a more detailed analysis.

[Kickstarter Challenge](https://github.com/curt0230/kickstarter-analysis/blob/main/kickstarter-analysis/Kickstarter_Challenge.zip)

### Analysis of Outcomes Based on Launch Date
During this analysis, the focus was on outcomes (successful, failed, and canceled) of completed campaigns based on launch dates.  To accomplish this, a Years column was added to enable an additional sorting and filtering method and provide additional clarity into campaign start dates.  Next, a pivot table was created with filters on Years and Parent Category.  The parent category filter was applied to include only "Theater" campaigns.  The rows, displaying the month of the converted version of the campaign created date, are aggreaged by the outcomes.  The pivot chart was further filtered by outcomes to exclude live campaigns from analysis since the final outcome is unknown in those cases.  A line chart was added to visualize these results.

![Theater_Outcomes_vs_Launch](/Resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals
During this analysis, the focus was on outcomes (successful, failed, and canceled) of completed campaigns based on launch dates.  First, a new workbook was added to the Kickstarter_Challenge workbook in order to review outcomes based on campaign funding goals.  Funding goals are broken down into 12 groupings of $5000 segments for goals ranging from less than $1000 to greater than $50,000.  Goal data for "Plays" campaigns was then summarized using the COUNTIFS function to determine the number of successful, failed, and canceled campaigns in each funding goal range.  Then, total campaigns for each outcome were summed and percents were derived.  Percent values were used to graph outcomes by goal on a line chart.

![Outcomes_vs_Goals](/Resources/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered
The biggest challenge I faced working on this project was correctly setting the ranges in the COUNTIFS function.  Carefully setting the boundaries to include both the lower and upper values for each range as well as ensuring each range was large enough to provide meaningful statistics resolved the issues and I was able to overcome the problem.

Also, the dataset represents a fairly small sample of Kickstarter campaigns and is somewhat outdated.  Trends since the start of the COVID-19 pandemic have been widely irregular, but more recent data covering 2018 to date would be helpful to understand those potential impacts as well.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
Campaigns launched in May seem to be most successful and have the lowest risk of failure, followed by those launched in June.  During that time frame 211 total campaigns (111 in May and 100 in June) were successful in reaching their funding goals, while 101 total campaigns failed (52 in May and 49 in June).  The fewest successful campaigns were launched in December when nearly 50% of campaigns failed (37 successful vs 35 failed).

- What can you conclude about the Outcomes based on Goals?
Small campaigns of less than $1000 seem to have the highest success rate at approximately 76%, closely followed by those ranging from $1000 to $5000 at 73%.  After that the success rate quickly tapers off.

- What are some limitations of this dataset?
The sample size of projects related to Theater and Plays is very limited in this data set.  Because of that, the results could be skewed somewhat.  A much larger sample could provide a more accurate result.  Additionaly, only one data source (Kickstarter) was analyzed, and arkets where Kickstarter is unused or less popular would be underrepresented.  Gathering data from various crowdfunding platforms could address both of these issues.

- What are some other possible tables and/or graphs that we could create?
One additional metric that deserves additional analysis is the impact of spotlighting campaigns on outcomes.  This marketing feature of the platform may very well be worth looking into to assure the sucess of the fundraising campaign and ultimately the project.