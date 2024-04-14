# Introduction
***
#### Data Science Project by Aidan Norton <br>
In this project, we will look at the sport of powerlifting. We will aim to answer the following three questions: <br>
- How is an individuals bodyweight correlated to their max bench press?
- Are Males/Females Relatively Better at a Given Exercise Compared to one Another?
- Is using Equipment Shown to be Significantly Helpful for Lifts?
### Powerlifting

Powerlifting is a competitive sport where each competitor gives their all to lift as much weight as they can with 1 repetition. <br>
There are three main exercises in powerlifting that are staples in measuring one's strength:
- Squat
- Deadlift
- Bench Press <br>
Each individual who performs at a powerlifting meet primarily performs at least a couple of these exercises. Each exercise is performed usually 3 times, and each participant's score is their best lift out of those few. <br> Whoever can lift the most weight combined across the three exercises in their weight/age class is regarded as the winner. <br>
### Dataset
https://www.kaggle.com/datasets/open-powerlifting/powerlifting-database <br>
We have a dataset consisting of hundreds of thousands of records of individuals' performance at powerlifting meets. <br>
There are many columns that record information about each participant's performance, such as their age, sex, weight, bench press, deadlift, squat; this dataset is an aggregation of many powerlifting meets across many years, so there is also information about the powerlifting meet dates, location, and event names. <br>
We will finally filter the squat/deadlift/bench records to focus only on the best out of three for each participant who went to meets that scored based on 3 attempts for each.
![alt text](https://github.com/nortona1atwit/DATASCIENCE-PROJECT/blob/main/graph/df_hea2.png?raw=true)
# Feature Engineering
***
<tab>For this dataset, there is a lot of columns that we do not need, and are irrelevant in the context of the goal of this project. We can start by excluding a numerous selection of columns such as the meet location information and dates. We want to keep only the ones we need to answer the three questions. <br>
Further down the line, we can fine tune our dataset further to meet the specific needs of each question.
![alt_text](https://github.com/nortona1atwit/DATASCIENCE-PROJECT/blob/main/graph/df_head.png?raw=true)
# Methods
***
### Tools
Python is a great programming language for data science with a powerful selection of libraries that help with data visualization and manipulation. <br>
In this project, we will be using a few standout libraries to help:
- Pandas: Data manipulation and storage
- Seaborn: Data visualization <br>
We can use features like scatterplots to visualize our data, and correlation matrixes to see how different features are correlated to one another.
# Questions
***
### 1) How is an individuals bodyweight correlated to their max bench press?
Intuitively, it can be predicted that as an individual's bodyweight increases, their strength will also increase. The bench press is a great exercise to measure raw strength. <br>
For this question, we will reduce the dataset to specify males between the age of 18-35 for consistency.
![alt_text](https://github.com/nortona1atwit/DATASCIENCE-PROJECT/blob/main/graph/benchpress_Scatterplot.png?raw=true) <br>
![alt_text](https://github.com/nortona1atwit/DATASCIENCE-PROJECT/blob/main/graph/q1_corr.png?raw=true) <br>
From the correlation cofficients, we can see that the correlation between Bodyweight (KG) and the bench press is about 0.556. This indicates a good positive correlation between the two. 
### 2) Are Males/Females Relatively Better at a Given Exercise Compared to one Another?
To answer this question, we can once again look at the correlation coefficients. We can split the data into two sets for male and female, and compare how each exercise contributes to their overall score. <br>
Once again, we look only at competitors between the age 18-35. <br>
Male: <br>
![alt_text](https://github.com/nortona1atwit/DATASCIENCE-PROJECT/blob/main/graph/q2_male.png?raw=true) <br>
Female: <br>
![alt_text](https://github.com/nortona1atwit/DATASCIENCE-PROJECT/blob/main/graph/q2_female.png?raw=true) <br>
Looking at the correlation coefficients beteen TotalKg and each exercise, we can see a big jump in regards to the bench press between males and females. The correlation between total weight lifted and bench press is .41 for females, compared to .29 for males. The deadlift is also up a bit by .06 for females as well. From this, we can say that the bench press is a relatively more important exercise for determining a female contestant's performance compared to a male contestant.
### 3) Is using Equipment Shown to be Significantly Helpful for Lifts?
By splitting the data into two sets, those who use equipment, and those who don't, and comparing the Dots, we can see if using equipment is shown to have any significant benefit. <br>
Dots is a measurement technique in powerlifting to compare relative strength to bodyweight.
![alt_text](https://github.com/nortona1atwit/DATASCIENCE-PROJECT/blob/main/graph/dots.png?raw=true) <br>
It is conclusive that using equipment boosts powerlifting performance, with equipment giving a 34% increase.
# Conclusion
***
Powerlifting is an exciting sport, and it offers an extensive data source for researching raw human strength and performance of staple exercises like the bench press, deadlift, and squat. From powerlifting, we can draw meaningful conclusions that can be applied not to just powerlifting, but to lifting weights in general. Casual lifters can use this data to figure out how to improve their lifts, for example, how they can improve their bench press, and whether they should use equipment or not.
