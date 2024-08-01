[세부 내용 엑셀](https://turingbio.sharepoint.com/:x:/r/sites/msteams_bb2a82/_layouts/15/Doc2.aspx?action=edit&sourcedoc=%7B15e90a2b-6af5-4442-b31c-7e9e3a2c464b%7D&wdOrigin=TEAMS-MAGLEV.teamsSdk_ns.rwc&wdExp=TEAMS-TREATMENT&wdhostclicktime=1718946304636&web=1)

## 데이터 요약

|   |   |
|---|---|
|Dataset 명칭|K-emoPhone|
|논문 명|K-EmoPhone: A Mobile and Wearable Dataset with In-Situ Emotion, Stress, and Attention Labels|
|데이터 수집 기간|7일(2019년 4월 30일부터 2019년 5월 8일)|
|인원|77명|
|수집기기|자신의 Android 스마트폰과 MS Band 2 스마트워치|
|특징|PHQ수집을 단 2번(사전/사후) 시행|
|EMA 데이터|주기적 수집: valence (감정의 긍정적/부정적 정도), arousal (감정의 흥분/차분 정도), stress (스트레스 수준), attention (현재 과제에 대한 주의력 수준), emotion duration (현재 감정의 지속 , 간) ,disturbance (설문 응답이 현재 과제에 미친 방해 정도), emotion change (설문 응답 중 감정의 변화 정도)  <br>  <br>사전/후 수집: PHQ-9, PSS (Perceived Stress Scale), GHQ-12 (General Health Questionnaire-12)|

## 데이터 항목
- 안드로이드 데이터(이벤트 기반)
	- Connectivity.csv
	- DataTraffic.csv
	- CallEvent.csv
	- MessageEvent.csv
	- AppUsageEvent.csv
	- InstalledApp.csv
	- RingerModeEvent.csv
	- PowerSaveEvent.csv
	- ScreenEvent.csv
	- OnOffEvent.csv
	- ChargeEvent.csv
	- MediaEvent.csv
	- Battery.csv 
	- ActivityEvent.csv 
	- ActivityTransition.csv 
	- Location.csv 
	- WiFi.csv
	
- MS Band2 스마트워치 데이터(특정 주기)
	- Acceleration.csv
	- StepCount.csv
	- Distance.csv
	- AmbientLight.csv
	- UltraViolet.csv
	- HR.csv
	- SkinTemperature.csv
	- Calorie.csv
	- EDA.csv
	- RRI.csv