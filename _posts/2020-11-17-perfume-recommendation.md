---
date: 2020-11-17 15:29:40
layout: post
title: 여러분에게 향기를 추천해 드립니다.
subtitle: 머신러닝 추천모델 개발 프로젝트
description: 이전에 사용했던 향수와 비슷한 성향을 찾아주거나 좋아하는 향기 기반으로 향수를 추천해주기
image: https://user-images.githubusercontent.com/68212420/98763511-7de8ea80-241d-11eb-8587-dad43d413719.png
optimized_image: https://user-images.githubusercontent.com/68212420/98763511-7de8ea80-241d-11eb-8587-dad43d413719.png
category: ML
tags:
  - ML
  - recommendation
author: 김연수, 이원진
---

<p align="center">
  <img src="https://user-images.githubusercontent.com/68212420/98763511-7de8ea80-241d-11eb-8587-dad43d413719.png">
</p>

<h1 align="center">Perfume Recommendation System: Wikiscent👃 </h1>
<h3 align="left">Machine Learning project using scents for perfume lovers and newbies</h3>
<h3 align="left">Try to make a neat recommendation system</h3>
<h3 align="left">Team👨‍👨‍👧</h3>
- KIM YUNSOO (https://github.com/sue-data056):

- Making blueprint of the project / Applying Deep learning models also (Keras, Surprise) / Visualize with Flask

- LEE WONJIN (https://github.com/AlanulousL):
  - Scrapping wide range of info from web / EDA with Yunsoo / Categorizing scent notes of perfumes

<h3 align="left">Purpose📊</h3>

- Building a recommendation system for perfume lovers base n their prefernece and perfumes they've been using😃

- We also find out recommendation system like below, however we try to make our own one

- https://paffem.me/ (Korean perfume recommendation web page using their own algorithm)

<h3 align="left">Data Collection💾</h3>
![image](https://user-images.githubusercontent.com/68212420/98764807-e9cc5280-241f-11eb-91cd-8592bce2e013.png)

- 1st trial: Using Kaggle to get datasets / Too vague to use it for our project 🤣

- 2nd trial: Making a decision to scrap some info from websites / the biggest perfume forum called 'Fragrantica; https://www.fragrantica.com/' is not accessible.

- 3rd trial: The 2nd biggest perfume form called 'Basenotes; https://www.basenotes.net/' is our target to scrap required info.

<h3 align="left">EDA💻</h3>

- From total 6400 perfumes to 423 perfumes

- Distributions are shown by histograms
  ![image](https://user-images.githubusercontent.com/68212420/98765157-c8b83180-2420-11eb-928c-6d655e05fd61.png)

- 900 scent notes in 423 perfumes are categorized into 11 groups. (Too many typos, non-English notes have to be categorized manually 🤯)

<h3 align="left">What we've done👻</h3>

1. Vectorize our notes to check similarity between them

- CountVerctorizer: We chose CountVectorizer, because a frequency of perfume notes is quite important to get
  recognizable ones.Based on CountVectorizer, we could compute similarity of every pair of perfumes.

- TfidfVectorizer: We’ve tried to get similarity between perfumes based on reviews given by various users.
  However, we couldn’t get a satisfying score even though we’ve been using stop-words, Word2Vec because we  
   didn’t have a label for perfumes from the beginning.

2. Clustering

- We wanted to get label for perfumes (we could not get proper clusters even we do a mnual categorization)

- Soyclustering: To use Cosine distance, we have to exploit Spherical k-means.
  (sklearn.cluster.Kmeans doesn’t provide such method)

- proper K?
  - Silhouette score might be great only for low-dimensional vector data clustering.
  - So, we set large K than we expect, then grouping a similar groups by post-processing.

3. Collaborative Filtering

- Considered user-similarity or item-similarity [ sim (u, v) ], <b> predict r (u, i) </b>
  ![image](https://user-images.githubusercontent.com/68212420/98770573-e340d980-2425-11eb-80ce-3bbcf84b4c3c.png)

- Using Surprise
  ![image](https://user-images.githubusercontent.com/68212420/98770628-01a6d500-2426-11eb-8fcf-7e9ac0629ea9.png)
  - BaselineOnly model is the best one for us limited on our datasets. We even try GridSearch to average RMSE
    below 0.65
- Keras part... plz help Yunsoo.

<h3 align="left">Features💻</h3>

- Hybrid Recommedation model

  - User has to select 3 categories of scent notes that are grouped by 11 categories.

  - Top 10 perfumes which are filtered by average ratings would be shown on another page. (Based on 3
    categories that user chosen.)

  - User has to select 2 good ones and 2 unattractive perfumes among them.

  - Based on 2 good perfumes, user could get total 20 perfumes that are similar to preferred perfumes and each
    including si and so-so ones from users who have similar preferences.

\*\*\* Please try our demo :)

<h3 align="left">Takeovers👊</h3>

- Validation of our recommendation

- Hard to build test dataset

- Clustering is not done properly

- RMSE & Accuracy of our model is not the best one

<h3 align="left">Languages and Tools:</h3>
<p align="left"> <a href="https://www.python.org" target="_blank"> <img src="https://devicons.github.io/devicon/devicon.git/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> <a href="https://www.w3.org/html/" target="_blank"> <img src="https://devicons.github.io/devicon/devicon.git/icons/html5/html5-original-wordmark.svg" alt="html5" width="40" height="40"/> </a><a href="https://www.w3schools.com/css/" target="_blank"> <img src="https://devicons.github.io/devicon/devicon.git/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40"/> </a> <a href="https://flask.palletsprojects.com/" target="_blank"> <img src="https://www.vectorlogo.zone/logos/pocoo_flask/pocoo_flask-icon.svg" alt="flask" width="40" height="40"/> </a> <a href="https://scikit-learn.org/" target="_blank"> <img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="scikit_learn" width="40" height="40"/> </a> <a href="https://www.tensorflow.org" target="_blank"> <img src="https://www.vectorlogo.zone/logos/tensorflow/tensorflow-icon.svg" alt="tensorflow" width="40" height="40"/> </a> <a href="https://git-scm.com/" target="_blank"> <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="40" height="40"/> </a> </p>

<p>&nbsp;<img align="center" src="https://github-readme-stats.vercel.app/api?username=sue-data056&show_icons=true&locale=en" alt="sue-data056" /></p>
<p>&nbsp;<img align="center" src="https://github-readme-stats.vercel.app/api?username=alanulousl&show_icons=true&locale=en" alt="alanulousl" /></p>
