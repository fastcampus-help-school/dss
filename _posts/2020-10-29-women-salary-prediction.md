---
date: 2020-10-29 12:26:40
layout: post
title: 여성인력 임금예측 프로젝트
subtitle: 여성 패널 조사 자료를 활용한 여성인력 임금 예측
description: 여성 패널 조사 자료를 활용한 여성인력 임금 예측
image: https://user-images.githubusercontent.com/67793544/99473563-26eb9400-298e-11eb-8efa-68801c4b73ca.png
optimized_image: https://user-images.githubusercontent.com/67793544/99473563-26eb9400-298e-11eb-8efa-68801c4b73ca.png
category: ML
tags:
  - prediction
  - regression
author: 전진경, 최은비
---

## 여성인력 임금예측 프로젝트
- 프로젝트 개요: 여성 패널 조사 자료를 활용한 여성인력 임금 예측
- 참여인력: 전진경, 최은비
- 주요 역할
  - 전진경 :데이터 수집, EDA, 시각화, 전처리, 모델적용
  - 최은비 :데이터 수집, EDA, 전처리, 모델적용, 문서정리
  
### 분석 결과
---
- 결과 개요
  - 최종 활용 모델: RandomForest Regressor
  - accuracy: RMSE 53 (단위 만원)
  - 예측값과 실제값 사이 53만원 정도의 오차가 있을 수 있음을 의미함
- 예측 예시
![image](https://user-images.githubusercontent.com/67793544/99473563-26eb9400-298e-11eb-8efa-68801c4b73ca.png)

  - 예시1. 21세, 경력1년, 미혼, 비정규직 고졸 여성 : 108만원으로 예측
  - 예시2. 30세, 경력5년, 기혼, 정규직, 대졸 여성 : 228만원으로 예측

- 한계점
  - 설문 데이터로 임금 입력에 50만 단위로 응답이 집중됨을 확인 (정확한 급여 확인이 어려움)
  - 급여 예측을 목적으로 수집된 데이터가 아니기 때문에 변수 선정이 제한적
  - 경력을 최대한 반영하고자 하였으나, 직접 경력을 묻는 항목이 없어 여성인력의 경력공백이 제대로 반영되지 못함
  

### 데이터 구성
---
- 데이터 출처: 여성가족패널
- 데이터 항목 (일부 데이터 발췌 사용)
  - 여성 개인용 (가족관계)
    - 성장과정 및 학교생활
    - 혼인 상태
    - 첫 직장의 경험
    - 자녀 및 부모님과의 관계
  - 일자리용
    - 현재의 경제활동
    - 이전 일자리
    
### 분석 프로세스
---
- 데이터 전처리
  - 결측치 확인 및 제거& 대체
  - 노후 데이터 제거
  - 경력 데이터 삽입
  - 범주형 데이터 변환
- 데이터 탐색
  - 응답자 주요 특성 분석
  - 변수간 관계 확인
- 모델 Fit & 성능 확인
  - 사용 모델
    - OLS
    - Linear Regressor
    - DecisionTree Regressor
    - RandomForest Regressor
    - GradientBoosting Regressor
    - XGBRegressor
- 예측 모델 성능 향상
  - 변수 변경 및 조정
  - 최적 모델 도출
  