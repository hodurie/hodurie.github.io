---
title: "Titanic 필사"
category : 
    - Study
tag :
    - Kaggle
    - Titanic
siderbar_main : true
---
안녕하세요. 

처음으로 Kaggle 글을 필사 해보려고 합니다.

제가 참고한 커널입니다.
- [타이타닉 튜토리얼 1 - Exploratory data analysis, visualization, machine learning]('https://kaggle-kr.tistory.com/17?category=868316')
- [[GUIDE, KOR, DG] 데이터 분석 어떻게 시작해야 하나요?]('https://www.kaggle.com/daehungwak/guide-kor-dg')
---
### Work FLow
0. 문제 정의
1. 데이터 셋 탐색
2. 탐색적 데이터 분석(EDA)
3. 데이터 전처리
4. 특성 공학 (feature Engineering)
5. 모델 적합 및 평가


#### 0. 문제 정의
우리가 예측해야 할 문제는
타이타닉 데이터의 여러 정보들을 이용하여
생존자를 예측하는 것 입니다.

평가 방식은 `accuracy`로
생존자를 얼마나 잘 예측 했는가를 판단 합니다.


다음은 `Feature` 들에 대한 설명입니다.

##### Feature

|변수|정의|설명|
|:-:|:-:|:-:|
|Survival|생존 여부|사망 : 0, 생존 : 1|
|Pclass|티켓 클래스|1st = 1, 2nd = 2, 3rd = 3 이며, categorical|
|Sex|성별|male, female로 구분|
|Age|나이(세)|탑승객의 나이|
|SibSp|함께 탑승한 형제/자매와 배우자의 수|-|
|Parch|함께 탑승한 부모와 자녀 수|-|
|Ticket|티켓 번호|-|
|Fare|탑승 요금|-|
|Cabin|객실 번호|-|
|Embarked|탑승 항구|-|
