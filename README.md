# Overview of Project

## Purpose and Background

  This project was a result of a request from Louise to analyize data from kickstarter campaigns in order to discern the outcomes
of campaigns based on campaign launch dates and campaign goals.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

Using a data set of Kickstarter campaigns, values for campaign date initiation, outcome, and "parent category" was aggregated into a pivot table.
This data was filtered by parent category for "Theater". The results of this filter were further analyzed by filtering the dates of campaign launch
by month of launch. The data was then filtered for outcomes only including the values of "successful", "failed", and "canceled".These results were 
sorted in a decending order for the outcomes value to arrive at the pivot table displaying aggregated counts of campaign outcomes.

A PivotChart was generated from the table and is displayed below:

![Theater Outcomes vs Launch](Resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals

The initial step of this analysis was to define the ranges over which the various theater campaigns would be analyzed. The ranges were provided in 
increments of $3999 with "less than 1000" acting as a lower bound and "greater than 50000" acting as the upper bound for the analysis set. Once the
bounds were set, the COUNTIFS() function was utilized to filter the Kickstarter data for the desired range, outcome, and campaign catagory. The
desired outcomes for the analysis were limited to "successful", "failed", and "canceled". The desired campaign catagory was set to "plays" for all
ranges. The results from each COUNTIFS() function was aggregated total of events meeting the desired citeria. After analyzing all the outcomes 
dover all of the desired ranges, the totals for each outcome in each range were summed together with the SUM() function. This provided the total 
events for each range.

The percentage of each outcome with in the range was calculated next. The total of each outcome in each of the monitery ranges was divided by the
total number of events in the range. The resulting value was multiplied by 100 to provide a percentage of each outcome within the monetary ranges.
The resulting percentages were then used to generated a plot of campaign outcome vs monertary goal ranges[1].

The resulting chart is provided below:

![Campaign Outcomes vs Campaign Goal (ranges)](Resources/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered

In the conducting this analysis, some challenges and difficulties surfaced. The first was the use of the use of the YEAR() function in Excel.
Since I am only generally familiar with the functionality of Excel, I had to make use of the provided link[2] in the module to learn how the
function could be used to achieve the desired results. Another challenge that was particularly of note occurred in when attempting to make
use of the COUNTIFS() function. In order to understand how to make use of this function properly, I had to make use of the provided "HINT"
link[3] found in the second third of the module. The third challenge encountered during this analysis was the sorting of the goal monetary 
ranges in the "Outcomes_vs_Goals" chart to properly set the values from least to greatest and arrive at an accurate depiction of the results.
This challlenge was solved using a Google search result[4]. 

## Results

What are two conclusions you can draw about the Outcomes based on Launch Date?

1. The first conclusion that can be drawn from the Outcomes based on Launch Date is May would be the best month to launch a theater campaign.

2. The second conclusion that can be drawn from the Outcomes based on Launch Date is December would be the worst month to launch a theater 
   campaign. 

What can you conclude about the Outcomes based on Goals?

From the graph, it can be concluded that the optimal goal ranges for a theater campaign are ranges targeting less than $5000 and between $35,000 and $40,000.

What are some limitations of this dataset?

One possible limitation of this data set is that it only analyzes campaign data from a singular crowdfunding platform. A more accurate data analysis could be
derived if data regarding theater campaigns from other sources were incorporated. Another limitation of this data set is the time frame for the data is not
current (does not include the most recent month). Including more recent data would yield a more accurate data analysis of trends in fundraising.

What are some other possible tables and/or graphs that we could create?

Possible tables and graphs that could be generated for a better understanding of theater campaign trends would include:

* Average pledged values for successful campaigns by month (graph)
* Average pledged values for failed campaigns by month (graph)
* Statistical calculations (Mean, Median, Mode, Standard Deviation, IQR) of successful campaigns (table)
* Statistical calculations of failed campaigns (table)
* Average number of campaigns launched per month vs campaign outcomes

## References
1. Module 1 Challenge. (n.d.). Retrieved September 13, 2020, 
from https://courses.bootcampspot.com/courses/453/assignments/5562?module_item_id=78674

2. YEAR function. (n.d.). Retrieved September 12, 2020, 
from https://support.microsoft.com/en-us/office/year-function-c64f017a-1354-490d-981f-578e8ec8d3b9?ui=en-us

3. COUNTIFS function. (n.d.). Retrieved September 12, 2020, 
from https://support.microsoft.com/en-us/office/countifs-function-dda3dc6e-f74e-4aee-88bc-aa8c2a866842?ui=en-us

4. Change the plotting order of categories, values, or data series. (n.d.). Retrieved September 13, 2020, 
from https://support.microsoft.com/en-us/office/change-the-plotting-order-of-categories-values-or-data-series-94108634-ddb1-409a-9a4d-13f57e6e6df5

5. Find Your&nbsp;. (n.d.). Retrieved September 14, 2020, 
from https://www.citationmachine.net/apa/cite-a-website
