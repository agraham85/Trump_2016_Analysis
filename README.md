<a name="br1"></a> 

**2016 Trump Voter Survey**

Predictive Model Selection

Andrew Graham – Fall 2022



<a name="br2"></a> 

**Overview**

Summary and Goals

**Purpose**

To determine the best model to predict, based on survey results from surveys,

whether someone voted for Trump or not in 2016. Survey contains demographics

and views on ideology, religion and racism.

**Significance**

To gain an understanding of how certain demographics and views align. Challenge

and/or confirm assumptions about the 2016 election. Prediction models can be

used in future elections to estimate the likelihood of a candidate getting votes in the

future. This can also be used to predict what types of candidates voters would

prefer in future elections.



<a name="br3"></a> 

**Overview**

Summary and Goals

How does the performance of a Naïve Bayes Classifier compare with KNN

Classifier, Random Forest Classifier , and Logistic Regression in predicting whether

an individual voted for Trump in 2016 given survey answers on demographics,

region, ideology, and views on racism?



<a name="br4"></a> 

**Overview**

Data Description

• Data from survey results collected

Output: Voted for Trump

• 1, 0 (Yes, No)

in 2016

• 40% Yes, 60% No

• Balanced

• 64,600 datapoints

• 44,898 with answer for Trump Vote

• 1 Continuous

Inputs

• 6 Demographic

• 17 Nominal

• 2 categorical

• 4 binary

• Age, Sex, Education, Race, Income,

State

• 2 Ideology Questions

• 4 Religion Questions

• 4 Racism Questions

• 11 ordinal



<a name="br5"></a> 

**Overview**

Data Cleaning

• No misspellings or formatting

number\_missin percent\_missin

issues

g

g

state 0

votetrump 0

age 0

0\.000000

0\.000000

0\.000000

0\.000000

0\.000000

0\.000000

10\.506036

3\.343133

1\.360862

0\.049000

0\.044545

0\.717181

2\.013453

0\.104682

0\.115818

0\.222727

0\.191545

• No duplicates

• Removed NAs for Target

• 7337 NA

• 16% rows with NAs

• No dependencies

female 0

collegeed 0

racef 0

famincr 4717

ideo 1501

• Randomly Distributed between

pid7na 611

bornagain 22

religimp 20

churchatd 322

prayerfreq 904

angryracism 47

whiteadv 52

fearraces 100

racerare 86

outputs

• NAs Removed

• 37,561 Data Points

Remaining



<a name="br6"></a> 

**EDA**

Dataset

• Ideology Features >60% correlation

with a vote for Trump

• Views on whether whites have an

advantage correlates 62%

• Views on racism correlates >40%

• Religion views correlate ~ 20-30%

• Demographics , no significant

correlation



<a name="br7"></a> 

**EDA**

Demographics

• Younger voters less like to vote for Trump

• Non-white very unlikely to vote for Trump

• Other demographics have minor

differences



<a name="br8"></a> 

**EDA**

Location

• South and Midwest

most likely to vote for

Trump

• Most states not very

predictive

• Exception Northeast

• California

• Oregon

• Hawaii



<a name="br9"></a> 

**EDA**

Ideology

• As expected, the left

ideology unlikely to

vote for Trump, right

likely

• Independents split

• Moderates split by lean

to not vote for Trump



<a name="br10"></a> 

**EDA**

Views on Religion

• The more religious, the

more likely to vote for

Trump

• Church Attendance the

affect is a bit less

significant

• Prayer frequency much

more significant



<a name="br11"></a> 

**EDA**

Views on Racism

• Most angry that racism exists,

slight correlation.

• May indicate different

definitions

• The rejection of white

privilege highly correlated

with a vote for Trump

• Fearing other races not

correlated (Likely people did

not admit to this)

• Rejecting the commonality of

racism correlates with a vote

for Trump



<a name="br12"></a> 

**Model Evaluation**

Preprocessing

• Clustering using KNN used to see if there is

an effect on performance

• K for KNN chosen to be 6

• Train Test split 80:20

• Clustering and non-clustered datasets



<a name="br13"></a> 

**Model Evaluation**

Multi-Model Comparison

Without Clustering

With Clustering

• 4 Models Trained

• Random Forest and Logistic Regression Best Performers

• Clustering did not improve results

• Optimize models without Clustering

• No Overfitting



<a name="br14"></a> 

**Model Evaluation**

Model Optimization/ Selection

• Both Models perform

equally

• Select simplest model

• Select Logistic Regression

• Parameter C: 0.1



<a name="br15"></a> 

**Conclusion**

Final thoughts Lessons Learned

• Ideology, views on white advantages, and the race of the respondent were

the most significant predictors

• Income not as significant as initially thought

• There seems to be an accuracy ceiling of about 90%

• The 10% may not be captured in the questions analyzed

• Fuller datasets with full survey answers would be useful

• Logistic Model was the simplest and performed the best

