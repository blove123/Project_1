# Week 1 Project: Measuring Success for IGTV
As a Product Data Scientist at Instagram measuring the success of Instagram TV (IGTV), I would analyze various key performance indicators (KPIs) to assess its impact and user engagement. kPIs include; retention and usage, content, monetization, user feedback and surveys, competitive analysis, user demographics, churn rate etc.

## Solution
For this project, I would focus on using the user engagement matrics such as viewership, likes, comments, watch time etc. over a period of 20 days to assess the success of IGTV.   

### 1.	Data Retrieval:
I would retrieve my data stored on my local PC as data.csv and import it using the pandas library in python.

```python
##getting data from local storage
import pandas as pd
pd.DataFrame()
df= pd.read_csv('data.csv')
print (df)
```


### 3.	Data Preprocessing:
Before starting my analysis, I would clean and preprocess the data by handling missing values and re-indexing the table.

```python
## Filling in the missing values

df['Viewership'].fillna(2200, inplace=True)
df['WatchTime'].fillna(31000, inplace=True)
df['Likes'].fillna(145, inplace=True)
df['Comments'].fillna(24, inplace=True)
df['Shares'].fillna(36, inplace=True)
```

### 4.	Data Analysis:
To measure the success of IGTV, I'll perform various analyses using Python's pandas library to calculate average viewership and likes.
```python
 # Calculate average metrics
avg_likes = df['Likes'].mean()
avg_comments = df['Comments'].mean()
print('Average Likes: ', avg_likes)
print('Average Comments: ', avg_comments)

#Calculate Average Viewership
avg_viewership = df['Viewership'].mean()
print('Average_Viewership: ', avg_viewership)
```

### 5.	Visualization:
I’ll communicate my findings by creating visualizations using Matplotlib in Python.
•	I’ll create line charts of viewership over time
•	Also, bar charts showing average viewership and average likes

```python
## A plot of WatchTime Over Time
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv('data.csv')
df.plot(x = 'Date', y = 'WatchTime', marker = 'o', linestyle = '-')
plt.title('WatchTime Over Time')
plt.xlabel('Date')
plt.ylabel('WatcTime')
plt.grid(True)
plt.show()


## A plot of Viewership Over Time
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv('data.csv')
df.plot(x = 'Date', y = 'Viewership', marker='o', linestyle='-')
plt.title('Viewership Over Time')
plt.xlabel('Date')
plt.ylabel('Viewership')
plt.grid(True)
plt.show()


# Create a bar chart to visualize average likes and viewership
plt.bar(['Average Viewership', 'Average Likes'], [avg_viewership, avg_likes])
plt.xlabel('Metric')
plt.ylabel('Count')
plt.title('IGTV Success Metrics')
plt.show()
```
### 6.	Identify Trends:
I’ll analyze the charts to identify trends, such as increasing or decreasing viewership.
#### Solution: 
The overall trends, from the graphs plotted above;
1. Viewership: Shows a gradual increase in viewership over time, with some fluctuations.
2. Watch Time: Shows a general upward trend in watch time, indicating users are spending more time watching IGTV videos.

### 7.	Recommendations
The following are my recommendations to improve user interaction metrics on IGTV:
1. User Feedback and Communication:
   - Gather user feedback through surveys and comments to understand their preferences and pain points.
   - Actively communicate with content creators to gather their insights and address their concerns.
2. Data-Driven Decisions:
   - Continue to employ data analytics to identify trends, monitor user behavior, and make informed decisions.
   - Implement A/B testing for new features and changes to evaluate their impact on user engagement.
3. Content Recommendations:
   - Refine and optimize content recommendation algorithms to provide users with personalized content that aligns with their interests.
4. Retention Strategies:
   - Focus on user retention by analyzing why some users stop using IGTV and implementing strategies to keep them engaged.