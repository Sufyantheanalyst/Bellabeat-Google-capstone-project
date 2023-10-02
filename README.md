# Bellabeat-Google-capstone-project
The analysis follows the 6 steps of Data Analysis using python: Ask, Prepare, Process, Analyse, Share and Act.
# How Can a Wellness Technology Company Play It Smart?
In this context, we are part of the marketing analyst team employed by Bellabeat, a cutting-edge manufacturer specializing in health-oriented products designed for women. Urška Sršen, one of the co-founders and the Chief Creative Officer at Bellabeat, is of the opinion that delving into the analysis of fitness data from smart devices has the potential to reveal fresh avenues for growth and expansion for the company.
# Regarding the company:
Bellabeat was established by Urška Sršen and Sando Mur as a forward-thinking enterprise specializing in the creation of cutting-edge smart products with a strong emphasis on health and wellness. Leveraging Sršen's artistic background, the company has developed technology that not only boasts exceptional design but also serves as a source of information and inspiration for women across the globe. Through the collection of data pertaining to physical activity, sleep patterns, stress levels, and reproductive health, Bellabeat has empowered women by providing valuable insights into their own well-being and daily routines. Since its inception in 2013, Bellabeat has experienced rapid growth and has rapidly positioned itself as a technology-driven wellness enterprise tailored to the needs of women.

By 2016, Bellabeat had expanded its presence globally, establishing offices in various locations and introducing a range of new products. These Bellabeat products were made accessible through an increasing number of online retailers, complementing the company's own e-commerce platform on its website. While Bellabeat has made investments in traditional advertising avenues, including radio, out-of-home billboards, print media, and television, it places a strong emphasis on digital marketing. The company maintains an ongoing presence on Google Search, actively engages with audiences on Facebook and Instagram, and consistently interacts with consumers on Twitter. Additionally, Bellabeat runs video advertisements on YouTube and employs display ads on the Google Display Network to support marketing campaigns centered around key milestones.

Recognizing that a thorough analysis of the consumer data at their disposal could uncover additional growth opportunities, Sršen has tasked the marketing analytics team with a specific mission. The team is to focus on a Bellabeat product and examine the usage data of smart devices to gain deeper insights into how people are currently utilizing these devices. With this information in hand, she seeks high-level recommendations on how these emerging trends can shape and enhance Bellabeat's marketing strategy moving forward.

The report will outline the insights gained through a structured data analysis process, which consists of the following stages:

# Inquiry (Ask): 
We will begin by defining the problem to be addressed and explore how the insights derived from the analysis can inform strategic business decisions.

# Data Preparation (Prepare): 
This stage involves the collection of pertinent data, its organization, and secure storage. It is vital to assess the integrity and reliability of the data. The data will be cleaned and made analysis-ready, with a thorough documentation of the cleaning process, and the cleaned data will be archived.

# Data Processing (Process): 
In this phase, we will select appropriate tools to handle the data, highlighting their advantages. Data cleaning is a critical component of this step to ensure that the data is suitable for analysis.

# Data Analysis (Analyze): 
The data will be structured and formatted to address the specific questions at hand. We will perform calculations, discern trends, and uncover relationships within the dataset.

# Presentation (Share): 
To effectively communicate our findings, we will generate visualizations that showcase the most pertinent results. These findings will be connected back to the initial questions posed.

# Action (Act): 
The final stage involves presenting our ultimate conclusions and recommending a course of action in response to the insights gained. This will encompass the next steps to be taken based on our findings.

# Step 1: Defining Objectives

During this initial step, we outline the case study's problem, objectives, and desired outcomes.

# 1.0 Context
Bellabeat, a forward-thinking manufacturer of elegantly designed smart products focused on women's health, has been operating since 2013. With a mission to inspire and empower women by providing insights into their health and lifestyles, Bellabeat has experienced rapid growth, establishing itself as a technology-driven wellness company for women.

Urška Sršen, co-founder and Chief Creative Officer, believes that analyzing consumer data unrelated to Bellabeat, specifically FitBit fitness tracker usage data, could unveil new avenues for growth.

# 1.2 Business Challenge:
Our task is to conduct an in-depth analysis of FitBit fitness tracker data to gain valuable insights into how consumers utilize the FitBit app. These insights will inform Bellabeat's marketing strategy.

# 1.3 Business Goals:
We aim to answer the following questions:

What trends emerge from the analysis?
How can these trends be relevant to Bellabeat's customer base?
In what ways can these trends influence Bellabeat's marketing approach?

# 1.4 Expected Outputs:
Our deliverables will encompass:

A concise overview of the business challenge
A description of all utilized data sources
Comprehensive documentation detailing any data cleaning or manipulation
A summary of our analysis findings
Visual representations and key discoveries
High-level content recommendations derived from the analysis

# 1.5 Key Parties Involved:
Urška Sršen: Co-founder and Chief Creative Officer of Bellabeat
Sando Mur: Mathematician, Co-founder, and key member of the Bellabeat executive team
Bellabeat Marketing Analytics Team: A team of skilled data analysts responsible for guiding Bellabeat's marketing strategy.

# 💻Data preparation:
Obtaining the Data

In order to address our primary question, which pertains to how current user behaviors can inform our marketing strategy, we will be utilizing data sourced from FitBit Fitness Tracker Data (https://www.kaggle.com/arashnic/fitbit). This dataset, available on Kaggle, comprises personal fitness tracker data contributed by thirty-three Fitbit users who met the criteria for eligibility and provided their consent for the submission of personal tracker data. The dataset encompasses minute-level details regarding physical activity, heart rate, and sleep monitoring. Within it, you can find information regarding daily activity, step counts, and heart rate measurements, all of which can be harnessed to gain insights into user behavior.

Contained within the 'fitbit' directory is a subfolder titled 'Fitabase Data 4.12.16-5.12.16,' housing a collection of 18 CSV files, each of which contains tracker data, including minute-by-minute records of physical activity, heart rate data, and sleep monitoring statistics.

# We are using Python for data cleaning, transformation and visualisation

To facilitate the process of file access, we can create a path variable to store the directory path that holds all the CSV files.
```python
 df14 = pd.read_csv('dailyActivity_merged.csv') 
```
# 🧰Process
In this phase, our focus will be on data processing, which involves tasks such as cleaning and ensuring its accuracy, relevance, completeness, and freedom from errors and outliers. This will be achieved through the following steps:

# Data Exploration and Observation: 
We will carefully examine the dataset to gain a deeper understanding of its characteristics and content.

# Identification and Handling of Missing or Null Values: 
We will identify any missing or null values within the data and take appropriate measures to address them.

# Data Transformation: 
To ensure consistency, we will consider data type formatting and make any necessary adjustments.

# Preliminary Statistical Analysis: 
We will conduct an initial round of statistical analysis to uncover key insights and trends within the data.

The objective of these processes is to prepare the data for further analysis and ensure its quality and integrity.
```python
# import packages and alias
import numpy as np # data arrays
import pandas as pd # data structure and data analysis
import matplotlib as plt # data visualization
import datetime as dt # date time
```
```python
# importing dataframe 
df14 = pd.read_csv('dailyActivity_merged.csv')
```
# Data cleaning & manipulation
```python
# review first 20 rows to get an idea about columns and data
df14.head(20)
```
```python
# getting more info of data in detail 
df14.info
```
```python
# to check the number of rows and columns 
df14.shape
```
```python
df14.size
```
```python
#  resetting the index of the DataFrame while dropping the previous index
df14.reset_index(drop=True, inplace=True)
```
```python
df14.head(5)
```
```python
# rename the dataframe
daily_activity = df14
```
```python
daily_activity.head(5)
```
```python
# counting the missing values in dataframe
count_missing_values = daily_activity.isnull().sum()
```
```python
count_missing_values[:]
```
```python
daily_activity.info()        # ActivityDate column is object dtype
```
```python
# converting ActivityDate object type to datetime type
daily_activity["ActivityDate"] = pd.to_datetime(df14["ActivityDate"])
```
```python
daily_activity.info()
```
```python
print(daily_activity["ActivityDate"].dtype)
```
```python
# Converting format of ActivityDate to yyyy-mm-dd
daily_activity["ActivityDate"] = daily_activity["ActivityDate"].dt.strftime("%Y-%m-%d")
```
```python
print(daily_activity["ActivityDate"])
```
```python
# creating new list of columns to rearrange the columns
new_columns = ['Id', 'ActivityDate', 'DayOfTheWeek', 'TotalSteps', 'TotalDistance', 'TrackerDistance', 'LoggedActivitiesDistance', 'VeryActiveDistance', 'ModeratelyActiveDistance', 'LightActiveDistance', 'SedentaryActiveDistance', 'VeryActiveMinutes', 'FairlyActiveMinutes', 'LightlyActiveMinutes', 'SedentaryMinutes', 'TotalExerciseMinutes', 'TotalExerciseHours', 'Calories']

# reindex function to rearrange columns based on "new_columns"
daily_activity = df14.reindex(columns=new_columns)
```
```python
# Creating new column by separating the date into day of the week for further analysis
daily_activity['DayOfTheWeek'] = daily_activity['ActivityDate'].dt.day_name()
```
```python
# to check the new added column
print(daily_activity)
```
```python
daily_activity["DayOfTheWeek"].head(5)
```
```python
# creating new column total_mins by adding all minutes of all catagaries
daily_activity["total_mins"] = daily_activity["VeryActiveMinutes"] + daily_activity["FairlyActiveMinutes"] + daily_activity["LightlyActiveMinutes"] + daily_activity["SedentaryMinutes"]
daily_activity["total_mins"].head(5)
```
```python
# creting a new column total_hours by converting total minutes into hours
daily_activity["total_hours"] = round(daily_activity["total_mins"] / 60)
```
```python
daily_activity["total_hours"].head(5)
```
# STEP 4: Data Analysis

Executing Computations
Retrieving Statistical Metrics for Analysis:

Count: The number of rows.
Mean (Average)
Standard Deviation (Std)
Minimum (Min) and Maximum (Max) values
Percentiles at 25%, 50%, and 75%
```python
daily_activity.describe()
```
```python
# check the names of all columns
daily_activity.columns
```
```python
# rename the columns 
daily_activity.rename(columns = {"Id":"id", "ActivityDate":"date", "DayOfTheWeek":"day_week", "TotalSteps":"total_steps", "TotalDistance":"total_dist", "TrackerDistance":"track_dist", "LoggedActivitiesDistance":"logged_dist", "VeryActiveDistance":"very_active_dist", "ModeratelyActiveDistance":"moderate_active_dist", "LightActiveDistance":"light_active_dist", "SedentaryActiveDistance":"sedentary_active_dist", "VeryActiveMinutes":"very_active_mins", "FairlyActiveMinutes":"fairly_active_mins", "LightlyActiveMinutes":"lightly_active_mins", "SedentaryMinutes":"sedentary_mins", "TotalExerciseMinutes":"total_mins","TotalExerciseHours":"total_hours","Calories":"calories"}, inplace = True)
```
```python
daily_activity.columns
```
# STEP 5: SHARE
In this step, we are creating visualizations and communicating our findings based on our analysis.

```python
import matplotlib.pyplot as plt

# Data
days_of_week = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday']
frequency = [10, 15, 8, 12, 20, 18, 14]

# Create a bar plot
plt.figure(figsize=(8, 6))
plt.bar(days_of_week, frequency, color="green", edgecolor="black")

# Adding annotations and visuals
plt.xlabel("Day of the week")
plt.ylabel("Frequency")
plt.title("No. of times users logged in app across the week")

# Display the plot
plt.xticks(rotation=45)  # Rotate x-axis labels for better readability
plt.grid(axis='y', linestyle='--', alpha=0.7)
plt.tight_layout()
plt.show()
```
```python
plt.figure(figsize=(8, 6))
plt.hist(daily_activity['very_active_mins'], bins=20, color='skyblue', edgecolor='black')
plt.xlabel('Very Active Minutes')
plt.ylabel('Frequency')
plt.title('Distribution of Very Active Minutes')
plt.grid(True)
plt.show()
```
```python
plt.figure(figsize=(8, 6))
plt.hist(daily_activity['fairly_active_mins'], bins=20, color='skyblue', edgecolor='black')
plt.xlabel('Fairly Active Minutes')
plt.ylabel('Frequency')
plt.title('Distribution of Very Fairly Minutes')
plt.grid(True)
plt.show()
```
```python
plt.figure(figsize=(8, 6))
plt.hist(daily_activity['lightly_active_mins'], bins=20, color='skyblue', edgecolor='black')
plt.xlabel('Lightly Active Minutes')
plt.ylabel('Frequency')
plt.title('Distribution of Lightly Active Minutes')
plt.grid(True)
plt.show()
```
```python
plt.figure(figsize=(8, 6))
plt.scatter(daily_activity['total_steps'], daily_activity['calories'], alpha=0.6, c='blue', edgecolor='black')
plt.xlabel('Total Steps')
plt.ylabel('Calories Burned')
plt.title('Steps vs. Calories Burned')
plt.grid(True)
plt.show()
```
```python
day_of_week_order = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday']
plt.figure(figsize=(10, 6))
sns.barplot(x='day_week', y='total_steps', data=daily_activity, order=day_of_week_order)
plt.xlabel('Day of the Week')
plt.ylabel('Average Steps')
plt.title('Average Steps by Day of the Week')
plt.grid(axis='y', linestyle='--', alpha=0.7)
plt.show()
```
```python
# pltting pie chart
activity_labels = ['Very Active', 'Moderately Active', 'Lightly Active', 'Sedentary']
activity_sums = [daily_activity['very_active_mins'].sum(), daily_activity['fairly_active_mins'].sum(),
                 daily_activity['lightly_active_mins'].sum(), daily_activity['sedentary_mins'].sum()]
plt.figure(figsize=(8, 8))
plt.pie(activity_sums, labels=activity_labels, autopct='%1.1f%%', startangle=140)
plt.title('Total Activity Summary')
plt.show()
```
```python
import matplotlib.pyplot as plt
import seaborn as sns  # Import Seaborn
import numpy as np


fig, axes = plt.subplots(1, 4, figsize=(15, 5), sharey=True)
fig.suptitle('Distance per Minutes of Activity')

sns.regplot(data = daily_activity, x = 'very_active_mins', y = 'very_active_dist', ax=axes[0])
axes[0].set_xlim([0,500])
sns.regplot(data = daily_activity, x = 'fairly_active_mins', y = 'moderate_active_dist', ax=axes[1])
axes[1].set_xlim([0,500])
sns.regplot(data = daily_activity, x = 'lightly_active_mins', y = 'light_active_dist', ax=axes[2])
axes[2].set_xlim([0,500])
sns.regplot(data = daily_activity, x = 'sedentary_mins', y = 'sedentary_active_dist', ax=axes[3])
axes[3].set_xlim([0,500]);
```
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/3dcde150-a869-471b-b443-687a79334a1c)








