
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
* 

#### How to Optimize
* Build split by split to determine best splits (find feature that gives the best separation)
* Uses greedy algorithm - with always choose feature that has the greatedt imbalance at each split 

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
eyJoaXN0b3J5IjpbNDA0Mzg1ODgyLDE3Mjg1NTMzMzQsLTE1Mz
kxMzk5MTAsMjc4ODIzMjgzLDE5Mzg5Njg5MDUsNjI5NzI1OTY5
LC0xMzU5NzkyNzg0LC0yMDY1NjI2MzUzLC0xNzE4ODk3Nzk1LD
cyNDY2NzM3MywxMTU5NDMzMjE5LDYzOTc2OTc2NywzMzE1NTg2
OTZdfQ==
-->