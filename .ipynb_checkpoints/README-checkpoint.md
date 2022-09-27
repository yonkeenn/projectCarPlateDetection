# projectCarPlateDetection


<b> **Brief** </b> : The main idea of the project is to automate the car plate detection using LBP algorithm. For this, we create dataset from raw data using a set of Computer Vision techniques.
<!--more-->

## Objective
Automate car plate detection using LBP algorithm and compare supervised machine model like Decision Tree, Support Vector Machine, Logistic Regression.

# 1. Dataset:
The main idea for generating dataset is to use the original images in gray scale for generating small images of bounding box size of car plate in order to create two variables: plate images and background images.

## Raw data preprocessing:
For preprocessing, we need to convert one image into many small images which can cover car plate. Here some main steps:
- Create gray scale image if it is not already done.
- Apply gaussian filter for removing noise and smoothness the image.
- Apply solbel vertical filter for detecting vertical edges.
- Apply OTSU threshold for segmenting the image.
- Apply morphological closing operation to enhance car place image.
- Get contours of car plate in order to get mask which will be used as bounding box

## Dataset creation:
For creation we need to pre-process each image in the raw dataset and get the car plate images and background images. At the end we will have two variable class for training model.
- Aplply pre-processing steps for each images and get bounding box of each car plate.
- Use bounding box limits for create dataset background images.
- Use bounding box limits for create dataset plate images.
- Use LBP Algoritm for create descriptor for each class and save it in a file for later usage.

# 2. EDA

For exploration, we will focus on check how is the behaveior of data related to the following topics:

1. Checking Nulls 
2. Data Information revision to check if there is outliers, checking skewness.
3. Target value revision
4. Checking correlation
5. Checking data distribution

# 3. Pre-Processing

As found in exploration phase, we will pre-process the dataset for being accurate to train, test and prediction. So we will focus in the following topics:

1. Removing outliers
2. Scaling and mormalized
3. Feature selection
4. Balancing data
5. Splitting data for training and testing

# 4. Modeling & Evaluation

We use 4 models in order to compare metrics and evaluate which one is better than other. Also we use GridSearchCV package in order to find the best parameters.

## Supervised models

1. Decision Tree - with Imbalanced/Balanced data in order to check behavior.
2. Logistic Regresion
3. Support Vector Machine
4. K-Nearest Neighbors

## Evaluation metrics 

1. Confusion matrix
2. ROC, AUC
3. Precision 
4. Recall
5. F1-score
6. MSE, RMSE

