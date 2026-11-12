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
- **데이터 출처:** [Titanic Dataset](https://github.com/datasciencedojo/datasets/blob/master/titanic.csv)
- **데이터 크기:** 891행 × 12열
- **예측 대상(Target):** `Survived`
- **문제 유형:** 이진 분류(Binary Classification)

## 4. 주요 실험 내용

### STEP 1. 환경 설정 및 데이터 수집
- 분석 환경 및 라이브러리 설정
- Titanic 데이터셋 수집 및 로드

### STEP 2. 탐색적 데이터 분석(EDA)
- 데이터 구조 및 변수 확인
- 결측치 비율 및 이상치 분석
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
- Feature Selection 적용 전후 비교
- GridSearchCV 하이퍼파라미터 최적화
- Permutation Importance 분석
- SHAP 기반 모델 해석
- RandomizedSearchCV 기반 추가 모델 탐색

### STEP 11. 종합 분석 및 결론
- 실험 결과 종합 비교
- 최적 전처리 전략 분석
- Feature Engineering의 효과 및 한계점 정리

## 5. 주요 실험 결과

필수 실험에서 가장 높은 F1-score를 기록한 조합은 Exp-1의 Logistic Regression입니다.

| 평가 지표 | 결과 |
|---|---:|
| Accuracy | 0.8324 |
| Precision | 0.8000 |
| Recall | 0.7536 |
| F1-score | 0.7761 |
| ROC-AUC | 0.8722 |

- 결측치 처리: Mean
- 인코딩: One-Hot Encoding
- 스케일링: StandardScaler
- Feature Selection: 미적용

## 6. 실행 방법

1. 저장소에서 `BigData_Feature_Engineering.ipynb` 파일을 선택합니다.
2. 파일을 다운로드하거나 Google Colab에서 엽니다.
3. 필요한 라이브러리 및 데이터 수집 코드를 실행합니다.
4. 노트북의 셀을 위에서부터 순서대로 실행합니다.
5. 각 STEP의 분석 결과와 시각화를 확인합니다.

[Google Colab 바로가기](https://colab.research.google.com/)

## 7. 저장소 구성

| 파일명 | 설명 |
|---|---|
| `README.md` | 프로젝트 및 실험 내용 안내 |
| `BigData_Feature_Engineering.ipynb` | 전체 분석 코드 및 실행 결과 |

## 8. 참고 사항

본 프로젝트는 Titanic 데이터셋을 활용한 특성 공학 및 머신러닝 성능 비교 실습입니다. 실험 결과는 데이터 분할, 전처리 조건 및 모델 설정에 따라 달라질 수 있습니다.
