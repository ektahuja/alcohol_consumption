# alcohol_consumption

Submitted by:
Ekta Ahuja, emahuja@umd.edu,
Kristen Bertch, kristennbertch@umd.edu,
Amar Kurane, akurane@umd.edu 

# Motivation:

Drinking is a common and even expected occurrence for college students in the United States. Unfortunately, drinking can lead to many negative consequences. As explained by the National Institute on Alcohol Abuse and Alcoholism, “1,825 college students between the ages of 18 and 24 die each year from alcohol-related unintentional injuries. Another student who has been drinking assaults more than 690,000 students between the ages of 18 and 24. More than 150,000 students develop an alcohol-related health problem and between 1.2 and 1.5 percent of students indicate that they tried to commit suicide within the past year due to drinking or drug use.”
Drinking is a serious problem that many students are faced with. The purpose of this research project is to identify the signs that a student is likely to consume high amounts of alcohol. If schools and counselors know which groups of students are a high risk of drinking heavily, they will be able to focus their efforts on the students who need the most help. The more we know about high risk students, the more we will be able to help them make the right decisions.

# Methodology:
## Data Preparation:

Our first step was to combine the weekday drinking (Dalc column) and the weekend drinking (Walc) in order to get the average the student drinks throughout the week.  We did this by multiplying the weekday-drinking column by five, multiplying the weekend drinking column by two, and then adding these numbers together. This gave us the average weekly consumption for each student.
Next we made two categories: students who were likely to be heavy drinkers and students who were not. The drinking amounts are on a one to five scale. If students are from zero to three then they are in the not considered heavy drinkers (or for purposes of the write-up a “drinker”). If they are four to five then they are considered likely to drink heavily. We created the avg_consumption_class column where we defined these parameters.

## Exploratory Data Analysis:

After we created the columns specified above we then moved on to examining the dataset as a whole. First, we just looked at a summary of the data. We then decided to compare some of the individual variables to alcohol consumption in order to better understand our dataset.  First we looked at alcohol consumption in relation to the type of jobs the students’ fathers had and then the type of job the students’ mothers had.
The information about the mother and fathers’ jobs was not very enlightening because in both cases the highest level of alcohol consumption was in the “other” category. Next we looked at drinking based on age.
We proceeded to make multiple more graphs comparing different variables to alcohol consumption. 
After finding the relationship between alcohol consumption and the variables above, we charted a few more variables so that we would have a good visualization of the data. These were:

* Absences vs. Average Consumption
* Student’s free time vs. Alcohol Consumption
* Student’s Grades vs. Alcohol Consumption

## Statistical Models:

Next we did a linear regression to see which variable were most important to determining whether a student was likely to be a drinker.
We deduced that the following variables has most effect on alcohol consumption:

* Sex
* Reason (for going to that college)
* Paid (is getting paid)
* Activities (extra-curricular) 
* Nursery (whether a nursery school was attended by the student)
* Famrel (quality of family relationship)
* Free time
* Goout
* Absences

We also used a decision tree to show the interaction of these variables. We then cross-referenced those results using the results of our random forest.
The random forest test highliged other variables, such as grades, that were not as prominent in our lm model. This indicated that we should consider these variables as well when doing our regression tests.
Finally, we split our data into test data and training data and then performed regresion tests. The goal was to find which set of variables most accuratly predicts whether a student will be a drinker.

We also implemented Naïve Bayes Classification algorithm to find out which set of variables were able to best predict whether a student is likely to be invloved in alcohol consumption. And we found out that ‘Age’ and ‘Sex’ of the student were the best predictors of alcohol consumption.
Then, to test the accuracy for our model, we plotted ROC graphs for Decision Tree and Random Forest Algorithms.

## Conclusion:
We could achieve the accuracy of about 95% using Logistic Regression Model for whether a student is likely to be a drinker. Our technique was effective in showing what schools should look for as early warning signs that students may be prone to drinking.

## Limitations:

* Limited number of records in the dataset
* Data is collected from the just two schools of same geograph




