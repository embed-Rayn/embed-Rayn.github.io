제목:  Personalized Multi-task Attention for Multi-modal Mental Health Detection and Explanation
[PDF_LINK](app://obsidian.md/index.html)

저자:  D Song, Q Shen, H Feng, R Song, F Giunchiglia, H Xu
출판사: Proceedings of the Annual Meeting of the Cognitive Science Society, 2023•escholarship.org

 
데이터: [[자체 데이터]]
모델:Multi-modal `self Attention` CNN model

### 데이터
#### 데이터 수집 과정
- 데이터 수집 과정은 2019년 11월 25일부터 12월 8일까지 대학에서
1. 참여자 모집: 
	- 2019-2020 및 2018-2019 학년도에 등록한 학생들이 파일럿에 초대되었습니다.
	- 프로젝트 및 파일럿의 기본 정보를 제공하는 소개 프레젠테이션에 참석했습니다.
	- 개인 정보 보호 및 윤리에 대한 동의서를 작성했습니다.
	- 총 60명의 학생들이 참여에 동의했고, 그 중 54명(남성 23명, 여성 31명)이 데이터를 제공했습니다.
2. 데이터 수집 도구:
	- 모든 참가자들은 스마트폰에 i-Log 앱을 설치했습니다.
	- 이 앱은 하드웨어 센서(예: GPS, 가속도계)와 소프트웨어 센서(예: 실행 중인 애플리케이션) 데이터를 기록했습니다.
	- 또한, 앱은 30분마다 참가자들에게 개인 컨텍스트를 추적하기 위해 시간 일지를 생성했습니다.
3. 시간 일지 질문:
	- 활동: "무엇을 하고 있습니까?"
	- 위치: "어디에 있습니까?"
	- 사회적 관계: "누구와 함께 있습니까?"
	- 기분, 스트레스, 우울증 등의 정신 건강 상태를 5점 Likert 척도로 평가했습니다.
	- 각 시간 일지는 150분 이내에 응답할 수 있었고, 최대 5개의 알림이 누적될 수 있었습니다.
#### 수집 항목
1. accelerometer
2. context
3. magneticfield
4. orientation
5. linearacceleration
1. gravity
2. gyroscope
3. wifinetworks
4. location
5. betterychargemonitor

## 모델
#### 1. 단일 모드 특징 추출 (Single-modal Feature Extraction):
- 각 감각 데이터의 모드별 특징을 추출하기 위해 CNN(Convolutional Neural Network)을 사용합니다.
- 각 센서 데이터의 시퀀스를 여러 미니 윈도우로 나누고, 시간 도메인 및 주파수 도메인 정보를 추출하여 CNN에 입력합니다.
- CNN은 2D 필터와 1D 필터를 사용하여 특징을 추출하고, 이를 벡터로 변환하여 센서 융합 레이어에 입력합니다.
#### 2. 다중 모드 특징 융합을 위한 어텐션 메커니즘 (Attention for Multi-modality Features Fusion):
- 주의 메커니즘을 사용하여 다양한 모드의 센서 데이터가 정신 건강 상태 감지에 기여하는 정도를 가중치로 반영합니다.
- 각 센서 데이터의 특징 벡터에 주의 점수를 부여하고, 이를 가중치로 사용하여 단일 특징 벡터로 융합합니다.
#### 3. 시간적 특징 학습을 위한 글로벌 어텐션 (Global Attention for Temporal Feature Learning):
- Bi-LSTM(Bidirectional Long Short-Term Memory) 네트워크를 사용하여 센서 데이터의 시간적 의존성을 학습합니다.
- Bi-LSTM의 출력은 다시 주의 메커니즘을 통해 각 시간 윈도우의 기여도를 반영하여 시간적 특징을 융합합니다.
#### 4. 분류 층 (Classification Layer):
- Bi-LSTM 네트워크의 출력을 소프트맥스 함수와 완전 연결 층(Fully Connected Layer)에 입력하여 각 정신 건강 상태의 확률을 계산하고, 최종 라벨을 예측합니다.
