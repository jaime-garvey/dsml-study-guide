
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


### Naive Bayes
<details><summary>More</summary>
<p>
**Binomial**  - Looking through the data you notice that certain kinds of spam emails will include your email handle (the part before the @ sign) somewhere in the subject line. You then build a feature that captures this as  **0**  if it’s not present and **1**  if it is. The algorithm will use this concept to classify emails as spam/ham and is named “Binomial” because it assumes your features are drawn from a  [binomial distribution](https://en.wikipedia.org/wiki/Binomial_distribution).

**Multinomial** - Similarly as before, we notice that the more dollar signs ($) there are in an email, the more likely that email is spam. We can do this for many kinds of words, say (CASH or Lottery), but instead of labeling them 0 or 1, we actually count how many times each word appears in the email. This helps the model by giving it information, not just on whether the word was there, but also how many times the word appeared because we know that this is a signal to help our classifier. The algorithm assumes that the features are drawn from a  [multinomial distribution](https://en.wikipedia.org/wiki/Multinomial_distribution).

For Gaussian, let’s assume we’re trying to classify whether a college student can dunk a basketball based only on their height.

**Gaussian** - As you may recall from any intro stats class, the distribution of heights in humans is continuous and  [normally distributed](https://en.wikipedia.org/wiki/Normal_distribution)  (the normal distribution is also called a Gaussian distribution, hence the name). So the algorithm will look at the height of all of the students we polled and determine where the cut-off should be to maximize the model performance (usually accuracy) to classify dunkers vs non-dunkers.

</p>
</details>

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

Ensemble methods use multiple models to improve performance. (Use for suspected high variance/overfitting or want a performance boost)

**Pros:**

-   Reduces variance
-   (generally) better model performance

**Cons:**

-   Loss of model interpretability
-   Possibility of high bias if data is not modeled properly
-   Computationally expensive

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
		i. Tuning the Weights - 
				- Regression  - can tune weights using OLS
				- Classification - use Stacked Classifier Method: meta-classifier (classifies classifiers), passes predictions though additional model (e.g. logistic regression)
4. Prediction 

**Note:** an ensemble of decision trees is called a Random Forest. Decision trees are prone to high variance and overfitting.

</p>
</details>

## Boosting

<details><summary>More</summary>
<p>
* Takes series of weaker learners and combines them

</p>
</details>

## Stacking

<details><summary>More</summary>
<p>


</p>
</details>

# Generalized Linear Models

**Three Models**
1. Linear Regression - prediction/forecasting (y ~Normal)
2. Logistic Regression - classification (y ~ Bernoulli)
3. Poisson Regression - count variables (y ~ Poisson exp(XB))




<!--stackedit_data:
eyJoaXN0b3J5IjpbNTM3NzE0NTQwLC0yMTAyNTY0ODYwXX0=
-->