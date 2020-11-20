---
date: 2020-10-29 12:26:40
layout: post
title: Recommend articles
subtitle: fit users taste on the brunch platform
description: Implementing customized content recommendation system using Machine Learning.
image: https://user-images.githubusercontent.com/67793544/99781231-ed1bb880-2b5a-11eb-93ca-fb4481ee757b.png
optimized_image: https://images.unsplash.com/photo-1476242906366-d8eb64c2f661?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=60
category: ML
tags:
  - ML
  - recommendation
author: 김희주, 최은비, 황지수
---

># ✔ [카카오 아레나] 브런치 사용자를 위한 글 추천 대회
### ◾ 프로젝트 개요
  - 공식 홈페이지 : https://arena.kakao.com/c/6
  - 프로젝트 목표 : 2018년 10월 ~ 2019년 3월 기간동안 등록된 글과 읽은 글에 대한 정보를 바탕으로 2019년 3월 시점에서 독자에게 글을 추천해주는 추천 시스템 개발

---
># ✔ 추천 알고리즘
### ◾ *Articles of Following Author*
- 전체 독자의 98%는 구독하고 있는 작가가 있음
- 1명의 독자는 평균 8.6명의 작가를 구독함
- 독자가 선호하는 작가의 글 우선추천
### ◾ *Articles of Magazine* 
- 매거진에 등록된 글은 최근 글이 소비되는 경향이 개인의 글보다 높음
- 신규 유저는 brunch 매거진의 글을 많이 보는 경향이 있음
- 독자가 읽었던 글과 유사한 매거진의 글 추천
### ◾ *Popular & Recent Articles*
- 많은 독자들이 읽었으며, 최신에 등록된 글 추천
### ◾ *interest-based recommendation (collaborative filtering)*
- 태그리스트를 활용하여 유사 취향을 가진 독자와 작가를 찾음
- tag 형태소 분석, 형태소 vector화 및 cosine 유사도를 통한 추천
- 유사 취향 독자 10명, 작가 10명을 추출하여 읽거나 쓴 글 중 최근/인기글 순으로 최종 100개의 글 추천
  - tf-idf vectorizer, Doc2vec 사용
---
># ✔ 추천시스템 구성
### ◾ *reader segmentation*
- test 기간 동안 읽은 글의 수를 기준으로 3개의 그룹으로 구분
  - group1 : 해당 기간동안 글을 전체 평균 이하로 읽은 독자 그룹 (0-7편)
  - gropu2 : 해당 기간동안 글을 전체 평균 이상으로 읽은 독자 그룹 (8-64편)
  - grouo3 : 종사자, 전문가, 크롤러 등으로 예상 (65편 이상)
### ◾ *recommendation for each segment*
- 그룹별 다른 방법을 활용하여 글 추천
  - group1 : following based - magazine based - popularity based 순으로 추천하여 100개의 글 추천
  - group2: interest-based 추천 방법을 사용하여 100개의 글을 추천
  - group3: recent/popularity based 추천방법을 사용하여 100개의 글 추천

