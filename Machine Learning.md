
# Machine Learning

# Table of Contents
* [Overview](#overview)
* [Regression](#regression)
* [Classification](#classification)
	* [Classification Algorithms](#classification-Algorithms)

# Overview

## What is Machine Learning?


## Types of Machine Learning**
|  Types         |  Description      |
|----------------|------------------|
|Supervised      |-labed data      |
|Unsupervised    | -unlabed data   |
|Semi-Supervised |                 |
  
## Regression versus Classification


# Regression

## Algorithms

### Decision Trees
* For numerical data, each leaf node is a predicted value (basically choose average of last leaf node)

# Classification

## Classification Algorithms

| **Algorithm** 				|**Description** |
|-------------------------------|----------------|
| **Logistic Regression**       |                |
|**Naive Bayes** 			    |                |
|**Linear Support Classifiers** |				 |
|**K-Nearest Neighbors**        |				 |
|**Decision Trees**             |				 |
|**Random Forests**             |				 |
|**Support Vector Machine**     |				 |



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

#### Variations/Methods
Ensemble (of Decision Trees) - using multiple trees
1. Bagging (Bootstrap Aggregating) - take randomly sampled subsets of training set (with replacement); Find different splits for each tree; predicts class that was choosen the most
2. Random Forests - using bagging but choose sqrt(n_features); then finds best split amoung those features; predicts class with majority vote (but can use weighted vote)


#### Additional
1. Pruning - take off nodes to generalize/prevent overfitting and improve performance
2. Boosting - improve model based on previously constructed classifiers

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


# Ensemble Methods

## Bagging

**Bootstrap aggregating**, or  **bagging**, is a type of machine learning algorithm that is designed to improve the accuracy and stability of the model (reduces variance). [Diagram](https://www.oreilly.com/library/view/python-machine-learning/9781783555130/graphics/3547_07_06.jpg)

<details><summary>More</summary>
<p>

1. **Bootstrapping** - sampling technique; Out of the 𝑛 samples in our dataset, 𝑘k samples are chosen **with replacement**.
	a. Without bootstapping, we may fail to generalize median of distribution (goal is to decrease variance in distribution of data) 
	b. As 𝑛 increases,  bootstraping will select approximately 2/3 unique samples (make sure model isn't biased to true sample)
2. **Aggregating** 
	b. Aggregate of the predictions of the models (that use the different bootstapped samples)
3. **Voting Classifier**
	a. Max Voting - assign the class that has the largest number of predictions for each model.
	b. Average Voting - average voting (aka soft voting) predicts the class that has the highest sum of predicted probabilities
	c. Weighting Voting - assignings weights to each model's predicted probability to adjust its contribution to the final prediction; Sometimes add additional weight to models that are performing better to optimize metric
		i. Tuning the Weights - can only tune weights in a regression problem (using OLS)
4. Prediction 

**Note:** an ensemble of decision trees is called a Random Forest. Decision trees are prone to high variance and overfitting.

</p>
</details>

## Boosting

<details><summary>More</summary>
<p>


</p>
</details>

## Stacking

<details><summary>More</summary>
<p>


</p>
</details>
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEzODk2MjU0OCwtMjA2MDYwOTA2NSwxNz
M0ODUyMjEwLC0xMzE1MjAxNzA0LDExNDY3NjMwODIsLTEzNzE5
Njk5MzYsODM5MTEwNDUsNDIxNDA1OTQ4LC0zNTI3ODQyODksMT
I5ODE1NDEzMyw3NDg1Njk0NTcsMTIzNDMzMTYxNSwxMTAyNDMz
MjExLC0xMTAxMjk1ODQ2LC0xODgxNzMwMjg5LDgyMzI3OTQ5Ny
wtMTk5MTc0OTY0OSwyMDEwNzkwMDYzLDQwNDM4NTg4MiwxNzI4
NTUzMzM0XX0=
-->