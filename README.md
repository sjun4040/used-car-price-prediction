🚗중고차 가격 예측 머신러닝 프로젝트
---
프로젝트 소개 
중고차 데이터를 기반으로 머신러능으로 중고차 시세를 예측하는 프로젝트 입니다
---
⚙️ 분석 및 예측 흐름<br>
1. EDA & 주요 인사이트<Br>
   - 가격 분포 : 로그 스케일적용<Br>
   - 연식, 주행 거리 : 연식, 주행거리에 따른 가격변화, 가격 패턴<Br>
   - 브랜드, 트림, 바디타입 : 시장별 인기모델 쏠림 정리<Br>
   - 결측/ 이상치 : horsepower, 실린더 수 의 결측치 KNN기법 보안<Br>
2. 데이터 전처리<Br>
   - 수치형, 범주형 결측/ 이상치 대체 : 대표값, KNN 임퓨팅 활용<Br>
   - 희귀값 통합 & 그룹화 : 모델/트림 상위 N개 외엔 'Other'로 그룹화<Br>
   - 파생 변수 생성<Br>
   - 원-핫 인코딩/ 타겟 인코딩 : 컬럼 각각의 특성에 맞춰 인코딩<Br>
   - 스케일링 : 회귀계열 모델에 맞춰 표준화<Br>
3. 사용 모델<Br>
   - XGBoost<Br>
   - HistGBR<Br>
   - RandomForest<Br>
4. 하이퍼 파라미터 튜닝 및 성능 결과<Br>
ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ<Br>
모델명 | RMSE | R² | Best Params요약|<Br>
ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ<Br>
XGBoost     | 0.245 | 0.935 | learning_rate=0.05, max_depth=10 |<Br>
HistGBR     | 0.249 | 0.933 | learning_rate=0.05, max_depth=15 |<Br>
RandomForest| 0.273 | 0.920 | n_estimators=500, max_depth=15 |<Br>
--- 
📈 최종 결론 및 해설 <br>
가장 성능이 뛰어난 모델 : XGBoost Regressor<br>
R² = 약0.936, RMSE = 약 0.245로 매우 높은 성능과 높은 신뢰도를 가진 모델입니다
--- 
🛠️ 사용기술 
<p align="left"> <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" /> <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" /> <img src="https://img.shields.io/badge/RandomForest-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" /> <img src="https://img.shields.io/badge/XGBoost-006B3E?style=for-the-badge&logo=python&logoColor=white" /> </p>
