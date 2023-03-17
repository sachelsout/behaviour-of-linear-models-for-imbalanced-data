# behaviour-of-linear-models-for-imbalanced-data
This repository shows, how linear models behave if there is imbalanced dataset. Support Vector Machine(SVM) and Logistic Regression(LR) algorithms are used with different regularization strength.
<h1>What is imbalanced data</h1>

![image](https://user-images.githubusercontent.com/86348193/225904228-842df5f3-fdb6-4d5c-92a1-62ad46b88dc4.png)<br>
Imbalanced dataset is the dataset where one of the two or more classes dominates in terms of the number of datapoints. Example, suppose there is a dataset with 2 classes, positive and negative class. There are 1000 positive datapoints and 20 negative datapoints. This is an example of highly imbalanced dataset.<br>
<h1> Datasets used in this task</h1>

![image](https://user-images.githubusercontent.com/86348193/225905094-b2a16d42-6f70-4ff4-878d-1521461bb5e6.png) <br>
We have created 4 imbalanced datasets with ratios between positive and negative samples as 100:2, 100:20, 100:40, 100:80. The above given plots shows those datasets in which blue represents positive datapoints and red represents negative datapoints.<br>
<h1>Effect of imbalanced data on linear models</h1>
We are using SVM and Logistic Regression models as linear models to see the effect of imbalanced dataset on the best fit line/plane under different datapoints scenarios.
Regularization is done to reduce the adverse effect of imbalanced datasets. Different values of regularizers are used in the task and the linear models are trained on those values. [0.001, 1, 100] are the regularizer values considered.<br>
Below are the resultant plots for SVM and Logistic Regression models.<br>
<h2>Support Vector Machines</h2>

![image](https://user-images.githubusercontent.com/86348193/225906615-5840b8e2-d799-48ac-ae02-6b5bff344359.png) <br><br>
<b><ins>Observation for SVM :</b></ins> <br><br>
<b>1. <ins>When C = 0.001</b></ins><br>
As the regularization parameter(C) is very small(0.001), the hyperplane is unable to separate the positive points from negative points. The hyperplane observed is far away from the data points. The classifier fails to classify the points for balanced dataset as well as imbalanced dataset.<br>
<b>2. <ins>When C = 1</b></ins><br>
The hyperplane is unable to separate the positive and negative points of highly imbalanced dataset. But for dataset (100,80), the hyperplane is able to classify the points(positive and negative) with some misclassified points as well.<br>
<b>3. <ins>When C = 100</b></ins><br>
The hyperplane is able to classify the positive and negative points for all the datasets(very little missclassified points). This improvement in classification is due to C = 100. Even for the highly imbalanced dataset, SVC is able to classify the points.<br>
<h2>Logistic Regression</h2>

![image](https://user-images.githubusercontent.com/86348193/225907629-54c25180-389e-43cc-8c27-8e779c3ec746.png) <br><br>
<b><ins>Observation for Logistic Regression :</b></ins> <br><br>
<b>1. <ins>When C = 0.001</b></ins><br>
As the regularization parameter(C) is very small(0.001), the hyperplane is unable to separate the positive points from negative points. The hyperplane observed is far away from the data points. The classifier fails to classify the points for balanced dataset as well as imbalanced dataset.<br>
<b>2. <ins>When C = 1</b></ins><br>
The hyperplane is unable to separate the positive and negative points of highly imbalanced dataset. But for dataset (100,80), the hyperplane is able to classify the points(positive and negative) with close to none misclassified points.<br>
<b>3. <ins>When C = 100</b></ins><br>
The hyperplane is unable to classify the positive and negative points for (100,2) dataset. The classifier is somewhat successful to classify the positive and negative points for other datasets, with some misclassified points as well and close to none misclassified points for (100,80) dataset.<br>
