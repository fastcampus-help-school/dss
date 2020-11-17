---
date: 2020-10-29 12:26:40
layout: post
title: Recommend articles
subtitle: fit users taste on the brunch platform
description: Implementing customized content recommendation system using Machine Learning.
image: https://user-images.githubusercontent.com/67793544/99050458-73744f80-25db-11eb-8b2e-d2048c17b560.png
optimized_image: https://user-images.githubusercontent.com/67793544/99050458-73744f80-25db-11eb-8b2e-d2048c17b560.png
category: ML
tags:
  - ML
  - recommendation
author: 수강생1, 수강생2
---

># project info.
### *theme of project*
- Recommend articles that fit users taste on the brunch platform.

### *objective of project*
- Implementing customized content recommendation system using Machine Learning.

### *Introduction to Datasets*
- Composed of five data sets

![image](https://user-images.githubusercontent.com/67793544/99050458-73744f80-25db-11eb-8b2e-d2048c17b560.png)
---
># project detail
### *project execution procedure*
- Repeat EDA and modelling and upgrade model

![image](https://user-images.githubusercontent.com/67793544/99219708-993e6600-2820-11eb-86b5-8582ae0cc554.png)

### *1st modeling* 
### contents based and Collaborative filtering for all users
- Content-based recommendation and collaborative filtering methods were attemped
- Massive data makes analysis difficult

### *2nd modeling*
### period limitation
- We find that within 14 days of the publication of the article, most consumption takes place.
![image](https://user-images.githubusercontent.com/67793544/99056115-2db88680-25dd-11eb-88dc-ddceabd6c51a.png)

- Users tend to read more up-to-date articles
- we would like to recommend registered articles to target users within two weeks of the registration date.
![image](https://user-images.githubusercontent.com/67793544/99056624-ec74a680-25dd-11eb-9dfb-a1252c81d16a.png)

### *3rd modeling*
### target segmentation
- The number of articles read by target users during validation periods is divided into three groups using descriptive statistics.
![image](https://user-images.githubusercontent.com/67793544/99057742-8e48c300-25df-11eb-84e7-9d412f52f67f.png)

- We tried to apply the recommendation system to each group in a different way   
  - Users in group1 will recommended by their following author list, magazine list they've read and recent popular articles   
  - Users in group2 will recommended by similarity of their taste with other users or authors using cosine similarity   
  - Users in group3 read more 65 articles within 2weeks. we considered them to be realted. we will recommend them to recent & popular articles except for they read   
![image](https://user-images.githubusercontent.com/67793544/99058061-00210c80-25e0-11eb-97f4-e789dbcb8063.png)