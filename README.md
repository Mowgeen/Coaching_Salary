# Coaching_Salary
### Required tools
Jupyter Notebook
Excel
### Project Overview
A given data set containing College School names, Coaches names, Coaches pay, and other information was given.  This information was used along with other information gathered from outside sources to predicting the salary of the next head coach of Syracuse University football.  The goal was to use linear regression to create a model based on the information gathered and answer lab questions regarding the next contract for the head coach of the football team.  Some of these questions were hypothetical with changes to the conference the team was in and some straightforward.  The best preforming predictors were identified, and some ethical decisions were made based on the project.  
### Data Cleaning
There were several issues that required attention in the data such as removing punctuation from numbers and making sure the actual pay was a numeric variable and not a string.  While public colleges are required to disclose the information about coach’s salaries, in the research it was found that private colleges are not and when looking four of the private colleges did not disclose their coaching salaries.  These schools were removed from the data set.  There was information that was not used as predictors and removed from the data at this point.  
### Data Acquisition
##### Stadium Capacity
Stadium information comes from https://bleacherreport.com/articles/1145292-power-ranking-all-124-college-football-stadiums, along with https://stadiumcapacity.com/ and google. This was manually entered. For adding information into the data three approaches were used. This is the first it is the worst possible way as the order needs to not change and it is not possible to see which school the data corresponds to until it is added to the data set.
##### Graduation Rate
Information was obtained from https://web3.ncaa.org/ and the cohort year was 2014. This is the second way information was added it is easier to read but combersome in the markdown as it is long taking up a lot of space. It would be easier to add information and it is easier to understand what the gsr score is associated with (which school it belongs to).
##### Win Loss Record
Information gathered frrom https://betiq.teamrankings.com/college-football/betting-trends/win-loss-records/?season=2021. The third way of adding data used was to create a excel file which will be submitted along with this markdown and read it into python as a pandas data frame. Using a inner join on school the data is merged and then the columns were fixed to have the final data frame.
### EDA (Exploratory Data Analysis)
![image](https://user-images.githubusercontent.com/118774600/212563628-d8a61b67-d67f-479f-9f52-9cd899e655d6.png)
![image](https://user-images.githubusercontent.com/118774600/212563645-f84f74b9-601b-4d00-9827-cecaf48bb094.png)
![image](https://user-images.githubusercontent.com/118774600/212563664-b680f14e-f955-4e20-9e7c-824e57f38fbf.png)
##### Correlation Heat Map
![image](https://user-images.githubusercontent.com/118774600/212563678-bb251f0c-8a34-4e74-a2b5-2c419a2779f0.png)
### Model Creationg
Two models were created one with all the variables used as predictors and one where some predictors were removed.  Two variables removed were loss and win percent because there was no information gained from having these along with number of wins.  Lastly FGR was removed (freshman graduation rate).  This was removed because as the graduation rate of freshman to the college increased it decreased the coach’s salary.  This may make sense as students were spending more time on schoolwork and less time on football making the team performance suffer.  As a school, the primary goal for student athletes should graduation and the coach should not be penalized because he puts education above winning.  Although both were still left in as an argument could be made that a student athlete should do both and a great coach could find a way to accomplish this task.  Ultimately it is the decision of the College as to which model to use.
### Results
![image](https://user-images.githubusercontent.com/118774600/212563402-fc1eee18-1dd8-422f-992f-f035cd0a6916.png)
The recommended Salary for the Syracuse football coach is: 3119004.55
What would his salary be if we were still in the Big East? What if we went to the Big Ten?
If Syracuse was still in the Big East (now the AAC) the recommended Salary for the football coach would be: 1648233.14
If Syracuse was in the Big Ten the recommended Salary for the football coach would be: 3770846.68
How good is our model?
The Original Model preforms slightly better and could be used accounting for 77.26 percent of the variation in coaches pay.
While model 2 seems to align more with a University's goals, it accounts for 75.75 percent of the variation in coaches pay.
### Bonus Section
A Hierarchiacal Clustering Model was created as a bonus for the project, attempting to show coach's pay based on conference it fails to do it does show some inforamtion and more needs to be done to find out what the clusters are showing.

![image](https://user-images.githubusercontent.com/118774600/212563716-7ce7a65c-21b3-4e2a-9124-70c73bbdb714.png)
