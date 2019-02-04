
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
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTAzNDc0MDEzMywxOTM4OTY4OTA1LDYyOT
cyNTk2OSwtMTM1OTc5Mjc4NCwtMjA2NTYyNjM1MywtMTcxODg5
Nzc5NSw3MjQ2NjczNzMsMTE1OTQzMzIxOSw2Mzk3Njk3NjcsMz
MxNTU4Njk2XX0=
-->