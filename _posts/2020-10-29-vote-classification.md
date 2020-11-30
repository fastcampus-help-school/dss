---
date: 2020-10-29 12:26:40
layout: post
title: 투표에 참여한 사람일까, 아닐까
subtitle: 머신러닝 분류모델 개발 프로젝트
description: 개인의 [심리성향 테스트 답변]과 [인적사항 데이터]를 기반으로 [국가투표 참여여부] 예측하기
image: https://user-images.githubusercontent.com/68367393/99255786-c5c1a480-2857-11eb-9b5a-345f4dac5a19.png
optimized_image: https://user-images.githubusercontent.com/68367393/99255786-c5c1a480-2857-11eb-9b5a-345f4dac5a19.png
category: Machine Learning
tags:
  - ML
  - classification
  - finance
author: 박경원, 전진경, 정성용
---

# 머신러닝 분류모델 개발 프로젝트
[발표자료 다운로드(pdf)](https://github.com/dss-14th/ml-repo-3/raw/main/Who's_Voted.pdf)
* * *
## 🗳 투표에 참여한 사람일까, 아닐까?!
- **프로젝트 주제**   
   개인의 [심리성향 테스트 답변]과 [인적사항 데이터]를 기반으로 [국가투표 참여여부] 예측하기   
   
- **팀원**   
   박경원 [pkw-May](https://github.com/pkw-May)   
   전진경 [JJIN-1916](https://github.com/JJIN-1916)   
   정성용 [DODO-YONG](https://github.com/DODO-YONG)   

* * *
## 🔎 프로젝트 개요

### 활용 데이터
- **데이터 내용**   
   마키아벨리즘 성향 테스트 답변 및 성격, 연령 등 인적사항 설문조사 답변 (총 73,490건)

- **데이터 수집기간 & 방법**   
   2017.07~2019.03, 온라인 조사   

- **조사대상**   
   전세계 불특정 다수

- **데이터 출처**   
   심리학 공공데이터 사이트 (미국) <https://openpsychometrics.org/>

### 활용 모델   
- LGBM, GBC, XGB, ADA

### 모델링 프로세스   
<img src="https://user-images.githubusercontent.com/68367393/99242046-06aebe80-2842-11eb-8a83-18d5b8b14ece.png" width="60%" height="60%" alt="process"></img>

* * *
## 💻 핵심 프로세스   
### 1. EDA
\>> [edagraph.html](https://github.com/dss-14th/ml-repo-3/blob/main/EDA_data_association.html)   
\>> [edagraph.py](https://github.com/dss-14th/ml-repo-3/blob/main/edagraph.py)   
   <img src="https://user-images.githubusercontent.com/68367393/99255786-c5c1a480-2857-11eb-9b5a-345f4dac5a19.png" width="50%" height="50%" alt="1st_process"></img>

### 2. 1차 전처리   
\>> [preprocessing.py](https://github.com/dss-14th/ml-repo-3/blob/main/preprocessing.py)   
   <img src="https://user-images.githubusercontent.com/68367393/99242278-4c6b8700-2842-11eb-89ec-e293a8bccd55.png" width="50%" height="50%" alt="1st_process"></img>

### 3. N차 데이터 전처리   
\>> [nthpreprocessing.py](https://github.com/dss-14th/ml-repo-3/blob/main/nthpreprocessing.py)   
   <img src="https://user-images.githubusercontent.com/68367393/99243857-9b1a2080-2844-11eb-81ab-0296c8697f80.png" width="50%" height="50%" alt="Nth_process"></img>

### 4. 모델성능 고도화     
\>> [hyperparameter.py] ```추가 예정```   
   <img src="https://user-images.githubusercontent.com/68367393/99244010-d7e61780-2844-11eb-9f9d-cb4e42d35378.png" width="50%" height="50%" alt="Hyperparameter_Tuning"></img>


* * *
## 📈 최종 모델 성능   
### AUC VALUE OF LGBM MODEL
   <img src="https://user-images.githubusercontent.com/68367393/99248451-ceac7900-284b-11eb-979b-23f76656f936.png" width="50%" height="50%" alt="Model_Performance"></img>

* * *
## 📚 추가 해결 과제   
   <img src="https://user-images.githubusercontent.com/68367393/99245035-4a0b2c00-2846-11eb-9241-175ee1628a7e.png" width="50%" height="50%" alt="Review"></img>

* * *
## 🧐 프로젝트 자세히 보기   
\>> [발표자료 다운로드(pdf)](https://github.com/dss-14th/ml-repo-3/raw/main/Who's_Voted.pdf)

* * *
## ⌨️ 사용언어 
   <img src="https://user-images.githubusercontent.com/68367393/99245317-b7b75800-2846-11eb-9b62-77be67f3b17b.png" width="7%" height="7%" alt="python"></img>
