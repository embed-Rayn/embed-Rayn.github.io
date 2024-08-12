제목:  Passive Sensing of Prediction of Moment-To-Moment Depressed Mood among Undergraduates with Clinical Levels of Depression Sample Using Smartphones
[PDF_LINK](https://www.mdpi.com/1424-8220/20/12/3572)

저자:  NC Jacobson, YJ Chung
출판사: Sensors, 2020•mdpi.com

데이터: [[자체 데이터]]
모델: XGBoost

- 목적: 대학생들 사이에서 우울증의 증상 변화를 시간 단위로 예측하기 위해 스마트폰 센서 데이터를 사용하는 것입니다.
- 방법: 참가자들의 스마트폰에서 수집된 센서 데이터를 기반으로 기계 학습 모델을 사용하여 시간대별 우울한 기분의 수준을 예측합니다.
- 결과: 연구 결과는 스마트폰 데이터를 사용하여 시간대별 우울한 기분을 평균 상관계수 0.587로 정확하게 예측할 수 있음을 보여줍니다.
- 한계점: 연구는 자가 보고된 우울증 수준에만 근거하고 있으며, 이 연구가 임상 면담을 통해 확인된 우울증 진단에 일반화될 수 있는지는 미지수입니다. 또한, 연구는 우울한 기분의 두 가지 구성 요소인 '슬픔’과 '외로움’에만 초점을 맞추고 있습니다.

# ㅇ
$$  
\text{outcome}_{i,t} \sim \beta_0 + \beta_1 \cdot \text{prediction}_{i,t} + \beta_2 \cdot \text{race} + \beta_3 \cdot (\text{prediction}_{i,t} \cdot \text{race}_i) + u_i  
$$
        
$$  
\text{outcome}_{i,t} \sim \beta_0 + \beta_1 \cdot \text{prediction}_{i,t} + \beta_2 \cdot \text{lagged outcome}_{i-1,t} + u_i  
$$



## 4\. 연구 결과

### 3.1 Compliance (참가자 응답률)
- 평균적으로 각 참가자는 총 **51.74회**의 시간 별 평가를 완료
- 응답 횟수:  **32회 ~ 93회** 
- 총 **1982개의** 시간별 우울한 기분 데이터 포인트가 수집

### 3.2 Sensing Data
- 센서 데이터는 참가자 간(interindividual) 및 참가자 내(intraindividual) 변동성을 모두 나타냄
- 각 참가자의 생활 패턴과 환경적 요인이 다르며, 이러한 차이가 **우울증 예측에 중요한 역할**을 할 수 있음을 시사

### 3.3. Predicting Depressed Mood(우울감 점수 예측)
- 모델 예측 상관 계수: **r = 0.587** (95% 신뢰구간: 0.552 ~ 0.621)
- 개인 간 변동성(interindividual variability)과 개인 내 변동성(intraindividual variability) 포함

### 3.4. Idiographic Predictions(개인 맞춤형 예측)

이 섹션에서는 개인 맞춤형 예측(idiographic predictions)의 성능을 분석했습니다.

- **결과**:
    - 개인 내 변동성에 대한 예측의 평균 상관 계수는 **r = 0.376** (95% 신뢰구간: 0.226, 0.508)로 나타났습니다.
    - 모델은 대부분의 개인에 대해 유의미한 예측 성능을 보였습니다.
    - 31명 중 한 명을 제외한 모든 개인에 대해 모델의 예측은 유의미했으며, 그 한 명의 경우에도 상관 계수는 **r = 0.18** (95% 신뢰구간: -0.022, 0.299)로, 거의 유의미한 수준에 근접했습니다.
    - 가장 높은 상관 계수는 **r = 0.731** (95% 신뢰구간: 0.645, 0.799)로 나타났습니다.
### 3.5 Follow-up Sensitivity Analyses 요약

이 섹션에서는 모델의 민감도 분석 결과를 다룹니다.

- **결과**:
    1. **인종 간 예측 성능 비교**:
        
        - **인종 변수**가 모델 예측 성능에 미치는 영향을 분석한 결과, 인종 간 예측 성능 차이는 유의미하지 않았습니다 (F(4, 3693.7) = 0.754, p = 0.555).
        - 이는 모델이 인종에 관계없이 일관된 예측 성능을 보였음을 의미합니다.
    2. **이전 시간의 우울증 결과를 고려한 예측**:
        
        - 모델이 이전 시간의 우울증 결과를 단순히 반영한 것이 아니라는 것을 확인하기 위해, 이전 시간의 우울증 결과를 통제한 상태에서도 예측 성능이 유의미했습니다 (β1 = 0.543, SE = 0.016, t(4353) = 34.877, p < 0.001).
        - 이는 모델이 시간에 따라 변화하는 우울증 증상을 정확하게 예측할 수 있음을 나타냅니다.