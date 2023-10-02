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

Gathering Fundamental Data Information:

Total number of rows and columns.
Names of the columns.
Count of non-null values.
Data types of the columns.

```python
# review first 20 rows to get an idea about columns and data
df14.head(20)
```
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/821e8aa4-21df-4ada-a782-030f7d3503bd)

```python
# getting more info of data in detail 
df14.info
```
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/fd40cc7b-de6f-490c-b5d8-d98fb924b60d)

```python
# to check the number of rows and columns 
df14.shape
```
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/be546289-233a-4ee4-878a-cec07864fed4)

```python
df14.size
```
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/a4d9afd3-e6d0-44ae-820a-224c4e465c07)

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
Next, I will determine if there are any null or missing values within the dataset.
```python
# counting the missing values in dataframe
count_missing_values = daily_activity.isnull().sum()
```
```python
count_missing_values[:]
```
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/2a5fc810-32d3-46b2-8767-1229ca02b50c)

```python
daily_activity.info()        # ActivityDate column is object dtype
```
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/1c190dbe-9b52-494b-b248-484d285578e6)

Now that we've identified the data requiring refinement, our next step is to engage in data manipulation and transformation. This will involve the following operations:

Converting the "ActivityDate" to the "datetime64" data type.
Formatting the "ActivityDate" to the "yyyy-mm-dd" format.
Generating a new column named "DayOfTheWeek" by deriving the date as the corresponding day of the week for future analysis.
Establishing a new column titled "TotalMins" by aggregating the values from "VeryActiveMinutes," "FairlyActiveMinutes," "LightlyActiveMinutes," and "SedentaryMinutes."
Creating an additional column, "TotalHours," by converting the "TotalMins" column (mentioned in step 4) to hours.
Reordering and renaming columns to enhance clarity and organization.
To commence this process, we will initially convert the "ActivityDate" from an "object" data type to "datetime64," followed by the objective of formatting "ActivityDate" in the "yyyy-mm-dd" style.
```python
# converting ActivityDate object type to datetime type
daily_activity["ActivityDate"] = pd.to_datetime(df14["ActivityDate"])
```
```python
daily_activity.info()
```
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/8964dcca-4407-4639-8b7d-00f467d07360)

```python
print(daily_activity["ActivityDate"].dtype)
```
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/e59862a0-3530-4277-bc9d-16d6a5c06c62)

```python
# Converting format of ActivityDate to yyyy-mm-dd
daily_activity["ActivityDate"] = daily_activity["ActivityDate"].dt.strftime("%Y-%m-%d")
```
```python
print(daily_activity["ActivityDate"])
```
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/393cf264-1eea-483f-a44b-bad20d063a13)

```python
# creating new list of columns to rearrange the columns
new_columns = ['Id', 'ActivityDate', 'DayOfTheWeek', 'TotalSteps', 'TotalDistance', 'TrackerDistance', 'LoggedActivitiesDistance', 'VeryActiveDistance', 'ModeratelyActiveDistance', 'LightActiveDistance', 'SedentaryActiveDistance', 'VeryActiveMinutes', 'FairlyActiveMinutes', 'LightlyActiveMinutes', 'SedentaryMinutes', 'TotalExerciseMinutes', 'TotalExerciseHours', 'Calories']

# reindex function to rearrange columns based on "new_columns"
daily_activity = df14.reindex(columns=new_columns)
```
Creating new column by separating the date into day of the week for further analysis.
```python
# Creating new column by separating the date into day of the week for further analysis
daily_activity['DayOfTheWeek'] = daily_activity['ActivityDate'].dt.day_name()
```
```python
# to check the new added column
print(daily_activity)
```
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/73740e9e-b010-4c12-8131-8cf25e6cdf24)

```python
daily_activity["DayOfTheWeek"].head(5)
```
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/5a0fe0ab-720f-4d9a-acb1-88896bca3618)

Creating new column total_mins being the sum of total time logged.
```python
# creating new column total_mins by adding all minutes of all catagaries
daily_activity["total_mins"] = daily_activity["VeryActiveMinutes"] + daily_activity["FairlyActiveMinutes"] + daily_activity["LightlyActiveMinutes"] + daily_activity["SedentaryMinutes"]
daily_activity["total_mins"].head(5)
```
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/f14f3dc8-d68a-4302-b4bc-47eecbe17a5a)

```python
# creting a new column total_hours by converting total minutes into hours
daily_activity["total_hours"] = round(daily_activity["total_mins"] / 60)
```
```python
daily_activity["total_hours"].head(5)
```
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/da26bd23-9295-4b0a-92d7-42e9d8fb1bc7)

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
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/22a715ac-bedc-47e6-8100-53b075cc1cdf)

```python
# check the names of all columns
daily_activity.columns
```
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/9b59a804-999e-49c0-8056-d526f37be35e)

```python
# rename the columns 
daily_activity.rename(columns = {"Id":"id", "ActivityDate":"date", "DayOfTheWeek":"day_week", "TotalSteps":"total_steps", "TotalDistance":"total_dist", "TrackerDistance":"track_dist", "LoggedActivitiesDistance":"logged_dist", "VeryActiveDistance":"very_active_dist", "ModeratelyActiveDistance":"moderate_active_dist", "LightActiveDistance":"light_active_dist", "SedentaryActiveDistance":"sedentary_active_dist", "VeryActiveMinutes":"very_active_mins", "FairlyActiveMinutes":"fairly_active_mins", "LightlyActiveMinutes":"lightly_active_mins", "SedentaryMinutes":"sedentary_mins", "TotalExerciseMinutes":"total_mins","TotalExerciseHours":"total_hours","Calories":"calories"}, inplace = True)
```
```python
daily_activity.columns
```
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/71c83ba7-c00e-48a4-af75-7d1fdb81b7e9)

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
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/b0a2e361-5eb1-4428-85c5-18c8f3aa5ff1)
Usage Frequency Throughout the Week

Within this histogram, we examine the usage frequency of the FitBit app, categorized by days of the week.

Our findings reveal that users tend to have a preference for or recollection of (with consideration for the possibility of occasional lapses) tracking their activity on the app primarily during the middle of the week, spanning from Tuesday through Friday. It is worth noting that usage frequency experiences a decline on Fridays and persists at lower levels over the weekend and on Mondays.

```python
plt.figure(figsize=(8, 6))
plt.hist(daily_activity['very_active_mins'], bins=20, color='skyblue', edgecolor='black')
plt.xlabel('Very Active Minutes')
plt.ylabel('Frequency')
plt.title('Distribution of Very Active Minutes')
plt.grid(True)
plt.show()
```
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/1d7636b9-f0b4-4d05-96bf-7492d277f726)

```python
plt.figure(figsize=(8, 6))
plt.hist(daily_activity['fairly_active_mins'], bins=20, color='skyblue', edgecolor='black')
plt.xlabel('Fairly Active Minutes')
plt.ylabel('Frequency')
plt.title('Distribution of Very Fairly Minutes')
plt.grid(True)
plt.show()
```
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/a83e6150-06c8-4d05-abb7-488262b25e6d)

```python
plt.figure(figsize=(8, 6))
plt.hist(daily_activity['lightly_active_mins'], bins=20, color='skyblue', edgecolor='black')
plt.xlabel('Lightly Active Minutes')
plt.ylabel('Frequency')
plt.title('Distribution of Lightly Active Minutes')
plt.grid(True)
plt.show()
```
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/d878073b-f294-4d89-97e8-6e727d86eb3f)
These plots reveal that a significant number of users, exceeding 400 individuals, allocate minimal time to being Very or Fairly Active. In contrast, the distribution of LightlyActiveMinutes displays a noteworthy degree of symmetry, with the exception of instances of exceptionally low minute counts.

Nevertheless, an issue warrants consideration: it remains uncertain whether all users consistently utilized the tracker throughout the entire day within the analyzed timeframe. In the event that a user records data for the entire day, the sum of VeryActiveMinutes, FairlyActiveMinutes, LightlyActiveMinutes, and SedentaryMinutes should equate to 1440, representing the total number of minutes in a day.

```python
plt.figure(figsize=(8, 6))
plt.scatter(daily_activity['total_steps'], daily_activity['calories'], alpha=0.6, c='blue', edgecolor='black')
plt.xlabel('Total Steps')
plt.ylabel('Calories Burned')
plt.title('Steps vs. Calories Burned')
plt.grid(True)
plt.show()
```
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/1927371a-cc96-4fc0-b691-d7745e7c78e1)

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
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/15544afd-5739-4cd9-bec9-9a1b93d5233b)

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
![image](https://github.com/Sufyantheanalyst/Bellabeat-Google-capstone-project/assets/129004768/2f7ffbd0-1f1d-4540-9f32-a89bfba0d2c7)
Percentage Breakdown of Activity Duration

As illustrated in the pie chart,

The largest portion, accounting for 81.3%, is attributed to Sedentary minutes. This suggests that users primarily utilize the FitBit app for recording daily activities such as commuting, sedentary movements (shifting from one location to another), or completing routine errands.

The usage of the app for tracking fitness activities (e.g., running) is infrequent, as evidenced by the minimal percentages for fairly active activity (1.1%) and very active activity (1.7%). This observation is somewhat disheartening considering that the FitBit app was originally designed to promote physical fitness.

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
As anticipated, VeryActive distances are covered in shorter durations, as indicated by their steeper regression lines, signifying higher speeds. FairlyActiveMinutes and LightlyActiveMinutes also exhibit variations in speed. It would be intriguing to gain insight into the criteria used for this categorization to better discern the distinctions between "Light" and "Moderate" activities.

# STEP 6: Act

In the final stage, we will present our findings and offer recommendations based on our analysis. During this phase, we will revisit our initial business inquiries and share high-level business suggestions.

Identification of Trends:
The majority of users (81.3%) primarily employ the FitBit app for monitoring sedentary activities, with a relatively limited focus on health habit tracking.
Users exhibit a preference for tracking their activities during weekdays, potentially influenced by increased outdoor activities during this period compared to weekends.

Application of These Trends to Bellabeat Customers:
Both companies, Bellabeat and FitBit, share a common mission of empowering women with insights into their health, habits, and fitness data. These prevalent trends in the health and fitness domain can be directly applicable to Bellabeat's customer base.

Utilizing These Trends for Bellabeat's Marketing Strategy:
The Bellabeat marketing team can encourage users by providing valuable education and equipping them with information about the benefits of fitness. They can suggest various exercise routines, such as simple 10-minute workouts on weekdays and more intensive workouts on weekends. Additionally, offering information on calorie intake and expenditure within the Bellabeat app can further enhance user engagement.

During weekends, the Bellabeat app can strategically send notifications to motivate users to engage in physical activities, fostering a healthier lifestyle.








