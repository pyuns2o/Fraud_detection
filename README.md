# Fraud_detection_project
한화 생명 데이터를 활용한 보험 사기 분류 프로젝트

# 소개
- 3학년 1학기 ‘고객 데이터 분석론’ 수업에서 진행한 개인 프로젝트로, 학점 A+ 획득
- 성능뿐만 아니라 feature engineering, feature selection, 모델 선정에서 설득력 있는 근거 제시를 목표로 진행
- 보험사기 여부를 효과적으로 분류하는 모델 개발
- 보험 사기와 관련성이 높은 피처를 선별하여 보험사의 피해액 감소에 기여

# 요약
**보험 사기 예측 모델 개발**

### 1. 프로젝트 개요
- **프로젝트명**: 보험 사기 예측 모델 개발
- **진행 기간**: 2023.05 ~ 2023.06
- **역할**: 데이터 분석, 피처 엔지니어링, 모델 구축 및 성능 개선
- **목적**:
  - 매년 증가하는 보험 사기 적발 금액과 인원 문제 해결
  - 경험 기반 탐지 방식의 한계를 극복하고, 데이터 기반 머신러닝 모델을 활용한 보험 사기 탐지 시스템 구축

### 2. 문제 정의
- 보험사기는 보험사 및 가입자에게 금전적 손실을 초래하며, 기존 방식(경험 기반)의 탐지는 한계가 있음
- 다양한 변수들을 고려한 머신러닝 모델을 활용하여 사기 탐지를 자동화하고 성능을 극대화하고자 함

### 3. 데이터 분석 및 전처리
- **데이터 기본 분석**
  - 성별, 직업, 연령, 사고구분, 설계사 경력, 결혼 여부, 소득, 가입일, 실손처리 여부, 입원/통원일수, 병원 종류, 유의 병원 여부 등의 변수가 보험 사기 여부에 따라 차이를 보이는지 분석
- **전처리 과정**
  - 결측치 처리: 변수 특성에 따라 평균값 대체 또는 새로운 범주 추가
  - 데이터 정규화 및 인코딩: 모델 입력값으로 활용 가능하도록 변환

### 4. 피처 엔지니어링
- **유의미한 변수 선정**
  - 카이제곱 검정과 T-test를 활용하여 보험 사기 여부에 따른 유의한 차이를 분석
  - 금융감독원 자료와 실제 데이터에서 유의한 피처를 반드시 포함
  - 추가적으로 유의성이 높은 변수들을 분석하여 포함
- **새로운 피처 생성**
  - 보험 계약 개수 및 보험 청구 개수 추가
  - FP(보험 계약 주선자)의 리스크 점수 산출하여 반영

### 5. 모델 구축 및 평가
- **모델 선택 및 실험**
  - 랜덤 포레스트(Random Forest) 및 XGBoostClassifier 모델을 비교 테스트
- **평가 지표 선정**
  - F1 Score를 주 평가 지표로 활용 (균형적인 성능을 위해)
  - Precision(특이도)을 보조 지표로 활용 (보험 사기자인 경우를 정확하게 예측하는 것이 중요하다고 판단)
- **모델 개선 과정**
  - 데이터 불균형 해결을 위해 SMOTE를 적용했으나 성능 하락으로 제외
  - 범주형 데이터를 단순화하여 변수 대체
- **최종 성능**
  - XGBoostClassifier 단일 모델 사용
  - F1 Score: 0.9735, Precision: 0.9988 달성

### 6. 결론 및 기대 효과
- 머신러닝 모델을 활용하여 보험 사기 탐지의 자동화 및 정확도 향상
- 보험사의 손실 감소 및 효율적인 사기 탐지 시스템 구축 가능
- 금융감독원 및 연구 자료 기반의 변수 활용을 통해 신뢰성 있는 모델 개발
- 실무 적용 가능성이 높은 프로젝트로 확장 가능성 검토

# 상세 내용
블로그(https://ityunseo.tistory.com/44)
  
# 아쉬운 점
- 모델을 구성하는 피처를 만들어내고 선택을 하는데 집중하여 데이터 자체 분석에 미흡했다.
- feature importance를 사용하여 피쳐를 좀 더 줄여서 학습을 진행시켜보지 못한 점이 아쉽다.

