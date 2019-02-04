
# Machine Learning

## Overview

### What is Machine Learning?


### Types of Machine Learning**
|  Types         |  Description      |
|----------------|------------------|
|Supervised      |-labed data      |
|Unsupervised    | -unlabed data   |
|Semi-Supervised |                 |
  
## Theory

### Regression versus Classification


## Algorithms


## Classification

### Class Imbalances
(When one class that you are trying to classify is greater than the other - e.g. an unfair coin)

If we build a model on an imbalanced dataset, the model may predict the majority call all the time (which could lead to high acuracy - misleading). 

#### Method 1: Oversampling 
<details><summary>Approaches</summary>
<p>
1. **Random** - Repeat data for minority class until it is balaned with the majority class. 
	
2. **Synthetic Minority Oversampling Technique (SMOTE)** - Similar to KNN, Create a new point in minority class that is between two nearest neighbors
	
3. **ADAptive SYNthetic oversampling (ADASYN)** - generates point where the class imbalance is the greatest; 

Note: Each approach comes at a cost (e.g. classifying more of minority class could cause more misclassification of majority class). The best solution depends on your problem and dataset.

</p>
</details>

#### Method 2: Undersampling 

<details><summary>Approaches</summary>
<p>
1. **Random** - Randomly select observations in majority class so that the size of each class is equal. 
2. **Near Miss** - only sample points from the majority class necessary to distinguish between the classes
3. **NearMiss-1** select samples from the majority class for which the average distance of the N _closest_ samples of a minority class is smallest.

</p>
</details>

Note: If these methods don't work, see Anomaly Detection Algorithm. 
<!--stackedit_data:
eyJoaXN0b3J5IjpbNDI3MjkyOTA3LDE5Mzg5Njg5MDUsNjI5Nz
I1OTY5LC0xMzU5NzkyNzg0LC0yMDY1NjI2MzUzLC0xNzE4ODk3
Nzk1LDcyNDY2NzM3MywxMTU5NDMzMjE5LDYzOTc2OTc2NywzMz
E1NTg2OTZdfQ==
-->