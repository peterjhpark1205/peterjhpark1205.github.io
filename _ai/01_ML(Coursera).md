---
title: "머신러닝 (Based on: Coursera - Andrew Ng)"
permalink: /ai/ml-coursera/
excerpt: "코세라에서 강의(강사: Andrew Ng)하는 머신러닝에 대한 이해를 요약함."
tags:
  - Machine Learning
toc: true
toc_sticky: false
---

<br>

:pencil:: 코세라에서 강의(강사: Andrew Ng)하는 머신러닝에 대한 이해를 요약함.

<br>

# 01. 지도 학습(Supervised Learning)과 비지도 학습(Unsupervised Learning)
<br>

## 지도 학습(Supervised Learning)

**지도 학습(Supervised Learining)** 은 크게 <u>회귀(Regression)</u>와 <u>분류(Classification)</u>로 나뉜다. 회귀와 분류의 차이는 종속변수(반응변수)가 연속형(Continuous)인가 이산형(Discrete)인가에 따라 다르다고 할 수 있다. 우선 둘 다 현재의 자료를 바탕으로 미래를 예측한다는 것은 동일하다.<br>

회귀는 종속변수가 연속형일 경우이고, 분류는 종속변수가 이산형일 때라고 볼 수 있다. 그랬을 때 로지스틱 회귀분석이 회귀분석이 회귀분석모형을 사용하지만, 분류인가에 대한 의문이 들 수 있다. 결론부터 말하자면, 분류에 사용되는 방법이다.<br>
**이 부분은 나중에 `분류(Classification)`-`로지스틱 회귀분석(Logistic Regresstion)` 부분에서 자세히 설명해야지..**

- 종속변수가 이산형: 분류(Classification)
- 종속변수가 연속형: 회귀(Regression)

<br>
<br>
<br>

## 비지도 학습(Unsupervised Learning)
**비지도 학습(Unsupervised Learning)** 은 문제에 대한 해결 방법을 거의 또는 전혀 알지 못할 때, 결과가 어떠할 것인지를 예측하는 것이다. 우리는 설명변수가 어떤 영향을 미칠 지 모르는 상황(즉, 종속변수가 없는 상황) 속에서 해당 자료(Data)의 구조를 찾기 위해 비지도 학습을 사용한다.<br>

비지도 학습은 크게 <u>군집(Clustering)</u>과 <u>비군집(Non-Clustering)</u>으로 나뉜다. 군집은 자료 내 변수들(Variables) 간의 관계(Relationship)를 파악하여 군집을 구성하는 것이고, 비군집은 ['칵테일 파티 효과(Cocktail Party Effect)'](https://en.wikipedia.org/wiki/Cocktail_party_effect)를 예로 들 수 있다. 여러 노이즈로 생각되는 값들 중에서 특정값을 찾아내고 이를 강조(Amplify)하는 것으로 실제 신경과학(Neuroscience)에서 관심을 갖고 있는 부분이고, 이를 구현하는 ['칵테일 파티 알고리즘'(Cocktail Party Algorithm)](https://interestingengineering.com/researchers-look-to-the-brain-for-algorithms-for-the-cocktail-party-problem)이 있다.

<br>
<br>
<br>
<br>
<br>

# 02. 모델 구현(Model Representation)
<br>

향후 개념 설명을 위해, 다음과 같이 변수를 설명한다.<br>
- $\boldsymbol{x^{(i)}}$는 <u>입력값(Input, 설명변수)</u>을 나타내며, 우리가 입력하는 변수임.
- $\boldsymbol{y^{(i)}}$는 <u>출력값(Output, 반응변수)</u>을 나타내며, 우리가 예측하고자 하는 값임.
- $\boldsymbol{(x^{(i)}, y^{(i)})}$는 <u>훈련 예제(Training Example)</u>이며, 우리가 학습을 시킬 데이터 세트(Dataset)임.
  - $m$ 개의 훈련 예제 목록인 $\boldsymbol{(x^{(i)}, y^{(i)});\; i=1,...,m}$은 <u>훈련 세트(Training Set)</u>라고 함.
- 윗첨자(Superscript) $\boldsymbol{^{(i}}$는 <u>훈련 세트의 인덱스(Index)</u>를 나타내며, 승수(Exponentiation, 누승법/멱법)와는 관계가 없음.
- $\boldsymbol{X}$는 <u>입력값들의 공간(Space, 집합(Set)으로 생각해도 무방할 듯함.)</u>을 나타내며, $\boldsymbol{Y}$는 <u>출력값들의 공간</u>을 나타냄.
  - 여기서 $X$와 $Y$는 실수 공간임(정확히는 실수 공간에 존재함.).
  - 즉, $\boldsymbol{X=Y=\mathbb{R}}$이라고 하나, $\boldsymbol{X\subset Y\subset \mathbb{R}}$이 더 정확할 것 같은데 지극히 '사견'임.
- 우리의 목표는 주어진 훈련 세트로 $\boldsymbol{h: X \rightarrow Y}$ 함수를 잘 학습하는 것이며, $\boldsymbol{h(x)}$는 $y$에 대응하는 값에 대한 <u>좋은("good") 예측기(Predictor)</u>임.
  - 역사적인 이유로 $\boldsymbol{h}$는 <u>가정(Hypothesis)</u>을 뜻함.














