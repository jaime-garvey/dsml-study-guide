
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

<details><summary>More</summary>
<p>
#### How to Optimize <br>
<li>Look at every feature and decide which to split up
<li>Build split by split to determine best splits (find feature that gives the best separation)
<li>Uses greedy algorithm - always choose feature that optimizes on one of the following metrics:

#### Metrics for Fitting
1. Max Entropy Rule (for categorical)
	a. [Information Entropy Graph](https://upload.wikimedia.org/wikipedia/commons/2/22/Binary_entropy_plot.svg)
2. Gini Coefficient (for continuous feature)
3. Misclassification Error - how many things you get wrong as a percentage (goal minimize)

Pruning - take off nodes to generalize/prevent overfitting and improve performance

#### Variations
1. Ensemble - using multiple trees
	a. Bagging (Bootstrap Aggregating) - take randomly sampled subsets of training set (with replacement); Find different splits for each tree; predicts class that was choosen the most
2. Random Forests - using bagging but choose sqrt(n_features); then finds best split amoung those features

</p>
</details>

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
eyJoaXN0b3J5IjpbLTE3NjU3MDkyNzUsODIzMjc5NDk3LC0xOT
kxNzQ5NjQ5LDIwMTA3OTAwNjMsNDA0Mzg1ODgyLDE3Mjg1NTMz
MzQsLTE1MzkxMzk5MTAsMjc4ODIzMjgzLDE5Mzg5Njg5MDUsNj
I5NzI1OTY5LC0xMzU5NzkyNzg0LC0yMDY1NjI2MzUzLC0xNzE4
ODk3Nzk1LDcyNDY2NzM3MywxMTU5NDMzMjE5LDYzOTc2OTc2Ny
wzMzE1NTg2OTZdfQ==
-->