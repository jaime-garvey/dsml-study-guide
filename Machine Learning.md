
# Machine Learning

# Table of Contents
* [Overview](#overview)
* [Regression](#regression)
* [Classification](#classification)

# Overview

## What is Machine Learning?


## Types of Machine Learning**
|  Types         |  Description      |
|----------------|------------------|
|Supervised      |-labed data      |
|Unsupervised    | -unlabed data   |
|Semi-Supervised |                 |
  
## Theory

## Regression versus Classification


# Regression

## Algorithms

### Decision Trees
* For numerical data, each leaf node is a predicted value (basically choose average of last leaf node)

# Classification

## Classification Algorithms

### Decision Trees
(Also called Classification & Regression Trees (CART); Use If-Then-Else logic to classify)
* Look at every feature and decide which to split up



## Class Imbalances
(When one class that you are trying to classify is greater than the other - e.g. an unfair coin)

If we build a model on an imbalanced dataset, the model may predict the majority call all the time (which could lead to high acuracy - misleading). 

### Method 1: Oversampling 
<details><summary>Approaches</summary>
<p>
1. **Random** - Repeat data for minority class until it is balaned with the majority class. 
	
2. **Synthetic Minority Oversampling Technique (SMOTE)** - Similar to KNN, Create a new point in minority class that is between two nearest neighbors
	
3. **ADAptive SYNthetic oversampling (ADASYN)** - generates point where the class imbalance is the greatest; 

Note: Each approach comes at a cost (e.g. classifying more of minority class could cause more misclassification of majority class). The best solution depends on your problem and dataset.

</p>
</details>

### Method 2: Undersampling 

<details><summary>Approaches</summary>
<p>
1. **Random** - Randomly select observations in majority class so that the size of each class is equal. 
2. **Near Miss** - only sample points from the majority class necessary to distinguish between the classes
3. **NearMiss-1** select samples from the majority class for which the average distance of the N _closest_ samples of a minority class is smallest.

</p>
</details>

Note: If these methods don't work, see Anomaly Detection Algorithm. 
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTI1ODU5NjA3MiwtMTUzOTEzOTkxMCwyNz
g4MjMyODMsMTkzODk2ODkwNSw2Mjk3MjU5NjksLTEzNTk3OTI3
ODQsLTIwNjU2MjYzNTMsLTE3MTg4OTc3OTUsNzI0NjY3MzczLD
ExNTk0MzMyMTksNjM5NzY5NzY3LDMzMTU1ODY5Nl19
-->