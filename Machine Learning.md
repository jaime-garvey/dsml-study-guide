
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

If we build a model on an imbalanced dataset, the model may predict the majority call all the time (which could lead to high acuracy - misleading). 

#### Method 1: Oversampling 

1. **Random** - Repeat data for minority class until it is balaned with the majority class. 
	
2. **Synthetic Minority Oversampling Technique (SMOTE)** - Similar to KNN, Create a new point in minority class that is between two nearest neighbors
	
3. **ADAptive SYNthetic oversampling (ADASYN)** - generates point where the class imbalance is the greatest; 

Note: Each approach comes at a cost (e.g. classifying more of minority class could cause more misclassification of majority class). The best solution depends on your problem and dataset.

#### Method 2: Undersampling 
1. Random - Randomly select observations in majority class so that the size of each class is equal. 
2. Near Miss - only sample points from the majority class necessary to distinguish between the classes
3. 


<!--stackedit_data:
eyJoaXN0b3J5IjpbMjUzOTAyOTQzLC0xMzU5NzkyNzg0LC0yMD
Y1NjI2MzUzLC0xNzE4ODk3Nzk1LDcyNDY2NzM3MywxMTU5NDMz
MjE5LDYzOTc2OTc2NywzMzE1NTg2OTZdfQ==
-->