---
date: 2020-10-29 12:26:40
layout: post
title: Socar Fraud Detection Project
subtitle: Fraud Detection
description: The purpose of this project is to build an optimal machine learning model for fraud detection with our focus on the recall score for model evaluation.
image: https://user-images.githubusercontent.com/68367214/100838698-40283080-34b6-11eb-8467-9351b5bbbca5.png
optimized_image: https://user-images.githubusercontent.com/68367214/100838698-40283080-34b6-11eb-8467-9351b5bbbca5.png
category: ML
tags:
  - Fraud detection
author: 이진서, 임상우, 김재욱
---

![SOCAR_LOGO_RGB_시그니처로고](https://user-images.githubusercontent.com/68367214/100838698-40283080-34b6-11eb-8467-9351b5bbbca5.png)



# Socar Fraud Detection Project



Members : 이진서, 임상우, 김재욱 (FastCampus Datascience School 14th)

  <A href="https://drive.google.com/file/d/1LD09arvFxmVrNI5tDJ2nc9Ra7MLVEpup/view?usp=sharing"> Presentation Slide </A>
<P>

## Introduction

Incorporated in 2011, SOCAR has become the largest car-sharing service provider in South Korea. Operating about 12K vehicles, SOCAR has over 5.8 million accumulated users, 200K of whom use the service each month. While strong demand growth for SOCAR service is expected to continue in the foreseeable future, there are growing concerns with an increasing number of insurance fraud cases. The purpose of this project is to build an optimal machine learning model for fraud detection with our focus on the recall score for model evaluation. The dataset is provided by SOCAR but some information in the attached presentation is hidden as requested by the data provider for security reasons. 




## Architecture

![Socar_project-Page-4 (4)](https://user-images.githubusercontent.com/68367214/100840581-75824d80-34b9-11eb-96a5-4d4cc7f54ab4.png)




## Machine Learning Model

![그림1](https://user-images.githubusercontent.com/68367214/98902177-86faba00-24f8-11eb-92cc-5edd15d121ab.png)



## Procedure

1. EDA 
2. Pre-processing
3. Modeling
4. Validation
5. Conclusion



## Details

Step 1. Baseline Set (with Raw Data)

Original Models
- Logistic Regression
- SupportVectorMachine
- RandomForestClassifier

Extended Models
- EasyEnsembleClassifier
- BalancedRandomForestClassifier
- RUSBoostClassifier



Step 2. Preprocessing

- One-Hot-Encoding
- Outlier Removal
- Scaling : RobustScaler, MinMaxScaler
- Train/Test Split



Step 3. Hyperparameter Tuning 

 + Gridsearch (Recall Priority)


Step 4. Imbalanced Data Tuning

 + Resampling (Oversampling, Undersampling)


Step 5. Validation

 + Easy Ensemble Classifier with StratifiedKFold

 
Step 6. Conclusion
- Limitation
- Interpretation


## Presentation Resourses

1. Sweetviz
2. Draw.io


## Reference

1. Terms of Socar : https://www.socar.kr/terms
2. Hands-On Machine Learning with Scikit-Learn and TensorFlow / Aurélien Géron