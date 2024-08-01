## 목표
  - VitalTracker에서 수집한 데이터를 바탕으로 우울증 중증도 Prediction 모델 생성
  - VitalTracker에서 수집을 하지 않는 데이터는 추가적인 Feature로 정의하여 최종적으로 저희가 수집하고자 하는 모든 Feature Set을 확정
  -  [[정신 질환 기존 치료 방법]]과 비교하여 효과성 평가

## 논문 키워드
### Technology Keyword
- (smartphone)
- (wearable)
- (remote + monitoring)
- (home + monitoring)
- (mobile + sensors)
- (mobile + montoring)
- (behavioral + sensing)
- (geolocation)
- (mHealth)
- (passive + monitoring)
- (digital + phenotype)
- (digital + phenotyping)
- (digital + biomarker)

### Analysis Keyword
- (machine + learning)
- (random + forest) 
- (neural + network) 
- (time + series) 
- (regression) 
- (SVM) 
- (knn) 
- (dynamics + model) 
- (decision + tree) 
- (discriminant + analysis) 
- (feature + engineering) 
- (feature + selection) 
- (data + mining) 
- (model) 
- classification 
- diagnostic 
- (prognostic) 
- (symptom + severity) 
- (prediction) 
- (monitoring)

### Population
- (bipolar)
- (depression)
- (depression + severity)
- (depressive + symptom)


## 주요 우울증 연구 관련 단어
- EMA: 생태순간평가(ecological momentary assessment)  PHQ-4, PHQ-8, PHQ-9 등
- PHQ-9: [test Link](https://www.mpm.go.kr/mpm/info/compens/compens08/compens0801/)
- DSM-5: 정신질환 진단 및 통계편람의 5번째 개정판(American Psychiatric Association, 2013)으로, 다양한정신장애에 대한 진단기준과 통계정보를 담고 있다.	
- 우을증 평가의 골드 스텐다드: Montgomery & Åsberg depression rating scales (MADRS) , Hamilton depression rating scale (HAMD)
- 디지털 피노타이핑(digital phenotyping): 개인의 디지털 기기(특히, 스마트폰)의 데이터를 사용하여 개개인의 표현형을 개별적, 순간적으로 정량화하는 기술
   - active data: 수집하는 데이터로는 사용자의 직접 입력이 요구
   - passive data: 센싱 기술 등의 이용으로 사용자의 입력 없이 수집

## 데이터
  - [[(2014)StudentLife]]
  - [[(2019)tesserae]]
  - [[(2022)K-EmoPhone]]
  - [[자체 데이터]]


## 우울증 연구
|          |                                                                                                           |                                                                                                                                                                                                                                                                       |                                                                                                                                                                                                                      |
| -------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 항목       | PHQ-9                                                                                                     | BDI (Beck Depression Inventory)                                                                                                                                                                                                                                       | HAM-D (Hamilton Depression Rating Scale)                                                                                                                                                                             |
| 총 문항 수   | 9                                                                                                         | 21                                                                                                                                                                                                                                                                    | 17 (또는 21)                                                                                                                                                                                                           |
| 평가 방식    | 자가 보고                                                                                                     | 자가 보고                                                                                                                                                                                                                                                                 | 임상 인터뷰                                                                                                                                                                                                               |
| 평가 기간    | 지난 2주 동안                                                                                                  | 지난 2주 동안                                                                                                                                                                                                                                                              | 지난 1주 동안                                                                                                                                                                                                             |
| 점수 범위    | 0-27                                                                                                      | 0-63                                                                                                                                                                                                                                                                  | 0-52 (17문항 기준)                                                                                                                                                                                                       |
| 점수 해석    | - 0-4: 최소 우울증<br>- 5-9: 경미한 우울증<br>- 10-14: 중등도 우울증<br>- 15-19: 중증 우울증<br>- 20-27: 매우 중증 우울증              | - 0-13: 최소 우울증<br>- 14-19: 경미한 우울증<br>- 20-28: 중등도 우울증<br>- 29-63: 중증 우울증                                                                                                                                                                                             | - 0-7: 정상<br>- 8-16: 경미한 우울증<br>- 17-23: 중등도 우울증<br>- 24 이상: 중증 우울증                                                                                                                                                  |
| 주요 문항 내용 | 1. 활동에 대한 흥미<br>2. 기분<br>3. 수면 문제<br>4. 피로<br>5. 식욕 문제<br>6. 자기 평가<br>7. 집중력 문제<br>8. 움직임과 불안<br>9. 자살 충동 | 1. 슬픔<br>2. 미래에 대한 비관<br>3. 실패감<br>4. 만족감 상실<br>5. 죄책감<br>6. 벌받고 있다는 느낌<br>7. 자기 혐오<br>8. 자기 비판<br>9. 자살 충동<br>10. 울음<br>11. 짜증<br>12. 사람들과의 거리감<br>13. 결정 장애<br>14. 자신감 상실<br>15. 유용감 상실<br>16. 에너지 상실<br>17. 수면 장애<br>18. 과민성<br>19. 식욕 변화<br>20. 집중력 감소<br>21. 피로감 | 1. 우울 기분<br>2. 죄책감<br>3. 자살 생각<br>4. 수면 유지<br>5. 불안/정신적 긴장<br>6. 활동 수준<br>7. 정신 운동 지연<br>8. 피로<br>9. 불면증<br>10. 체중 변화<br>11. 신체 증상<br>12. 성적 관심 상실<br>13. 주관적 우울감<br>14. 주관적 불안<br>15. 공포<br>16. 내적 긴장<br>17. 자살 경향성 |
| 사용 목적    | - 일차 진료에서의 우울증 선별 및 평가<br>- 증상의 심각도 평가                                                                    | - 심리치료 및 연구 환경에서의 우울증 평가<br>- 치료 전후 비교 및 모니터링                                                                                                                                                                                                                         | - 임상적 우울증 평가<br>- 치료 효과 모니터링<br>- 연구 환경에서 사용                                                                                                                                                                         |
| 장점       | - 간편하고 신속함<br>- 표준화된 진단 기준 적용                                                                             | - 심리적, 인지적 우울증 증상에 대한 세부 평가 가능                                                                                                                                                                                                                                        | - 임상 전문가의 심층적 평가 가능<br>- 포괄적 증상 평가 가능                                                                                                                                                                                |
| 단점       | - 자기 보고 방식의 한계<br>- 주관적 편향 가능성                                                                            | - 자기 보고 방식의 한계<br>- 주관적 편향 가능성                                                                                                                                                                                                                                        | - 시간과 비용이 많이 듬<br>- 주관적 판단 개입 가능성                                                                                                                                                                                    |
|          |                                                                                                           |                                                                                                                                                                                                                                                                       |                                                                                                                                                                                                                      |
- **PHQ-9**: 빠르고 간편하게 우울증 증상의 심각도를 평가할 수 있는 자가 보고 설문지로, 일차 진료에서 널리 사용됩니다.
- **BDI**: 우울증의 심리적, 인지적 증상을 상세하게 평가할 수 있는 자가 보고 설문지로, 심리치료 및 연구 환경에서 자주 사용됩니다.
- **HAM-D**: 임상 전문가가 수행하는 심층적인 인터뷰를 통해 우울증의 심각도를 평가하는 도구로, 임상적 평가와 치료 효과 모니터링에 널리 사용됩니다.