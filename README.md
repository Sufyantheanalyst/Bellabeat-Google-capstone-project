# Bellabeat-Google-capstone-project
The analysis follows the 6 steps of Data Analysis using python: Ask, Prepare, Process, Analyse, Share and Act.
# How Can a Wellness Technology Company Play It Smart?
In this context, we are part of the marketing analyst team employed by Bellabeat, a cutting-edge manufacturer specializing in health-oriented products designed for women. Urška Sršen, one of the co-founders and the Chief Creative Officer at Bellabeat, is of the opinion that delving into the analysis of fitness data from smart devices has the potential to reveal fresh avenues for growth and expansion for the company.
# Regarding the company:
Bellabeat was established by Urška Sršen and Sando Mur as a forward-thinking enterprise specializing in the creation of cutting-edge smart products with a strong emphasis on health and wellness. Leveraging Sršen's artistic background, the company has developed technology that not only boasts exceptional design but also serves as a source of information and inspiration for women across the globe. Through the collection of data pertaining to physical activity, sleep patterns, stress levels, and reproductive health, Bellabeat has empowered women by providing valuable insights into their own well-being and daily routines. Since its inception in 2013, Bellabeat has experienced rapid growth and has rapidly positioned itself as a technology-driven wellness enterprise tailored to the needs of women.

By 2016, Bellabeat had expanded its presence globally, establishing offices in various locations and introducing a range of new products. These Bellabeat products were made accessible through an increasing number of online retailers, complementing the company's own e-commerce platform on its website. While Bellabeat has made investments in traditional advertising avenues, including radio, out-of-home billboards, print media, and television, it places a strong emphasis on digital marketing. The company maintains an ongoing presence on Google Search, actively engages with audiences on Facebook and Instagram, and consistently interacts with consumers on Twitter. Additionally, Bellabeat runs video advertisements on YouTube and employs display ads on the Google Display Network to support marketing campaigns centered around key milestones.

Recognizing that a thorough analysis of the consumer data at their disposal could uncover additional growth opportunities, Sršen has tasked the marketing analytics team with a specific mission. The team is to focus on a Bellabeat product and examine the usage data of smart devices to gain deeper insights into how people are currently utilizing these devices. With this information in hand, she seeks high-level recommendations on how these emerging trends can shape and enhance Bellabeat's marketing strategy moving forward.

# The report will outline the insights gained through a structured data analysis process, which consists of the following stages:

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

To facilitate the process of file access, we can create a path variable to store the directory path that holds all the CSV files.
```python
 df14 = pd.read_csv('dailyActivity_merged.csv') 
```


