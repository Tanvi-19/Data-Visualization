# Call Center Trends Analysis Report
I joined a virtual internship at PwC, were my major role is to create interactive reports using Power BI.

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

- Created separate conditional column for Answered and Abandoned Calls (Used to count the overall answered and abandoned calls)

Measures used :

- Total Calls - Count = COUNT(Sheet1[Call Id])
- Average customer satisfaction rating = AVERAGE(Sheet1[Satisfaction rating]) 
- Customer rating in between 4 to 5 = CALCULATE(COUNTROWS('Sheet1'),AND('Sheet1'[Satisfaction rating] >= 4, 'Sheet1'[Satisfaction rating] <= 5))
- Poor rating = CALCULATE(COUNTROWS('Sheet1'),'Sheet1'[Satisfaction rating] = 1)
- Average speed of answer in sec = AVERAGE(Sheet1[Speed of answer in seconds])

## Filters used on :

- Months
- Resolved Issue
- Topics
- Agents
- Date

## Data Visualization :
![image](https://github.com/Tanvi-19/Data-Visualization/assets/84302681/2c64cdff-4224-4c15-8ce5-4d85758f706d)

