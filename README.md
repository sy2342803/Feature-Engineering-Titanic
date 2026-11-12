# Titanic Dataset Feature Engineering

실제 데이터를 활용하여 특성 공학(Feature Engineering)과 전처리 전략에 따른 머신러닝 모델의 성능 차이를 비교·분석하는 과제입니다.

---

## 1. 과제 정보

- **과목명:** 빅데이터분석
- **분반:** 01분반
- **학번:** 2342803
- **이름:** 문서영 (MoonSeoyeong)
- **과제 주제:** 머신러닝 성능 향상을 위한 Feature Engineering 파이프라인 설계 및 비교 분석

## 2. 프로젝트 개요

본 프로젝트에서는 Titanic 생존자 데이터를 활용하여 데이터 전처리 및 특성 공학 전략이 머신러닝 모델의 예측 성능에 미치는 영향을 분석하였습니다.

결측치 처리, 범주형 변수 인코딩, 데이터 스케일링, 파생변수 생성 및 특성 선택을 수행하고, 여러 실험 조건에서 Logistic Regression과 Random Forest 모델의 성능을 비교하였습니다.

## 3. 데이터셋 소개

- **데이터셋:** Titanic Dataset
- **데이터 출처:** [Kaggle Titanic Dataset - Data Science Dojo](https://github.com/datasciencedojo/datasets/blob/master/titanic.csv)
- **데이터 크기:** 891행 × 12열
- **예측 대상(Target):** `Survived`
- **문제 유형:** 이진 분류(Binary Classification)

생존 여부(`Survived`)를 예측하기 위해 승객의 성별, 나이, 객실 등급, 요금 등의 변수를 활용하였습니다.

## 4. 주요 실험 내용

### STEP 1. 환경 설정 및 데이터 수집
- 분석 환경 및 라이브러리 설정
- Titanic 데이터셋 수집 및 로드

### STEP 2. 탐색적 데이터 분석(EDA)
- 데이터 구조 및 변수 확인
- 결측치 비율 분석
- 이상치 분석
- Histogram, Boxplot, Heatmap, Countplot 시각화
- 생존 여부와 주요 변수 간 관계 분석

### STEP 3. Feature Engineering
- 결측치 처리 전략 비교: Mean, Median, Most Frequent
- 범주형 변수 인코딩: One-Hot Encoding, Ordinal Encoding
- 데이터 스케일링: StandardScaler, MinMaxScaler, RobustScaler
- 파생변수 생성: FamilySize, IsAlone, FarePerPerson, Title, AgeGroup, HasCabin

### STEP 4. Feature Selection
- SelectKBest 기반 특성 선택
- 특성 선택 적용 전후 모델 성능 비교

### STEP 5. 머신러닝 모델 학습 및 평가
- Logistic Regression
- Random Forest Classifier
- Accuracy, Precision, Recall, F1-score, ROC-AUC 평가
- Base 및 Exp-1, Exp-2, Exp-3 실험 비교

### STEP 6~10. 추가 분석 및 성능 개선
- Feature Selection 적용 전후 비교 실험
- GridSearchCV를 이용한 하이퍼파라미터 최적화
- Permutation Importance를 활용한 변수 중요도 분석
- SHAP을 이용한 모델 예측 해석
- RandomizedSearchCV 기반 추가 모델 및 하이퍼파라미터 탐색

### STEP 11. 종합 분석 및 결론
- 실험 결과 종합 비교
- 최적 전처리 전략 분석
- Feature Engineering의 효과 및 한계점 정리

## 5. 주요 실험 결과

필수 실험에서 가장 높은 F1-score를 기록한 조합은 다음과 같습니다.

| 구분 | 결과 |
|---|---|
| 실험 | Exp-1 |
| 모델 | Logistic Regression |
| 결측치 처리 | Mean |
| 인코딩 | One-Hot Encoding |
| 스케일링 | StandardScaler |
| Feature Selection | 미적용 |
| Accuracy | 0.8324 |
| F1-score | 0.7761 |
| ROC-AUC | 0.8722 |

추가 AutoML 실험에서는 교차검증 기준 Random Forest가 가장 높은 F1-score를 기록하였으며, 테스트 데이터에서는 Logistic Regression이 가장 높은 F1-score를 기록하였습니다.

이를 통해 전처리 전략과 모델 선택에 따라 예측 성능이 달라질 수 있음을 확인하였습니다.

## 6. 실행 방법

1. 위 저장소에서 `BigData_Feature_Engineering.ipynb` 파일을 선택합니다.
2. 노트북 파일을 다운로드하거나 Google Colab에서 엽니다.
3. 필요한 라이브러리 설치 및 데이터 수집 코드를 실행합니다.
4. 노트북 상단부터 마지막 셀까지 순서대로 실행합니다.
5. 각 STEP의 분석 결과와 시각화 및 모델 평가 결과를 확인합니다.

**Google Colab에서 실행하기**

[Google Colab 바로가기](https://colab.research.google.com/)

Google Colab에서 GitHub 탭을 선택한 뒤 다음 저장소 주소를 입력하면 노트북을 불러올 수 있습니다.

`https://github.com/sy2342803/Feature-Engineering-Titanic`

## 7. 저장소 구성

| 파일명 | 설명 |
|---|---|
| `README.md` | 프로젝트 및 실험 내용 안내 |
| `BigData_Feature_Engineering.ipynb` | 전체 분석 코드 및 실행 결과 |

## 8. 참고 사항

본 프로젝트는 Titanic 데이터셋을 활용한 머신러닝 특성 공학 및 성능 비교 실습입니다. 실험 결과는 사용한 데이터 분할, 전처리 조건 및 모델 설정에 따라 달라질 수 있습니다.
