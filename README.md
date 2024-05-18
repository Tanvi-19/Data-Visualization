# Call Center Trends Analysis Report
I joined a virtual internship at PwC, where my major role is to create interactive reports using Power BI.

Here is my First Task -


## Problem Statement :
Create a dashboard in Power BI for Claire that reflects all relevant Key Performance Indicators (KPIs) and metrics in the dataset. Get creative! 

- Possible KPIs include (to get you started, but not limited to):

  - Overall customer satisfaction
  - Overall calls answered/abandoned
  - Calls by time
  - Average speed of answer
  - Agent’s performance quadrant -> average handle time (talk duration) vs calls answered

## Dataset :

  ![image](https://github.com/Tanvi-19/Data-Visualization/assets/84302681/8c85de19-3d75-48bf-8057-fd7216b1b1dc)

## Data Cleaning/Preparation :
Dataset contains 5000 records and 10 columns.

- Understand the data
- Validated the data type of the column
    - Changed data type for column Time and AvgTalkDuration to Time as it contains the data related to time, initially it was declared as a Date data type.
 
## Performed Calculations :
Conditional Column :

- Created separate conditional column for Answered and Abandoned Calls (Used to count the overall answered and abandoned calls).

Measures Used :

- Total Calls = 'COUNT(Sheet1[Call Id])'
- Average customer satisfaction rating = `AVERAGE(Sheet1[Satisfaction rating])`
- Customer rating in between 4 to 5 = `CALCULATE(COUNTROWS('Sheet1'),AND('Sheet1'[Satisfaction rating] >= 4, 'Sheet1'[Satisfaction rating] <= 5))`
- Poor rating = `CALCULATE(COUNTROWS('Sheet1'),'Sheet1'[Satisfaction rating] = 1)`
- Average speed of answer in sec = `AVERAGE(Sheet1[Speed of answer in seconds])`

## Filters Used On :

- Months
- Resolved Issue
- Topics
- Agents
- Date

## Data Visualization :
![image](https://github.com/Tanvi-19/Data-Visualization/assets/84302681/2c64cdff-4224-4c15-8ce5-4d85758f706d)

- KPI's Used :
    - Total calls
    - Calls answered/abanded
    - Average satisfaction rating
    - Average speed of answer in sec
    - Calls by time
    - Agent’s performance quadrant - (total calls, answered calls, abanded calls, Avg talk duration, Avg speed of answer, Avg rating)
    - Total calls by topic

## Insights :
Based on the visualization following are the insights :

- Overall customer satisfaction rating is medium(3.4).
- 5000 total calls are registered over the span of three months (January, February, March).
- In the month of January average customer satisfaction rate was highest, and March was lowest.
- Agent Martha got a highest rating, and Joe got a lowest rating.
- Average speed of answering a call by agent Joe is highest and by agent Becky is lowest.
- Most of the issues resolved in January month with highest percentage, down in February and again slightly increased in March.
- Resolution rate of Jim is highest, though the average speed of answering a call is lower as compared to Joe. Also he attended maximum calls.
- Maximum calls are related to Streaming topic.

## Final Call :
- Based on above information I came to below conclusion :
    - Top 3 Agents based on call resolution rate : Jim, Dan, Becky
    - Top 3 Agents based on calls attended : Jim, Martha, and for third position we have 2 agents Dan and Diane but Dan's call resolution rate is higher as compared to Diane
    - Top 3 Agents based on customer ratings : Martha, Dan, Diane
