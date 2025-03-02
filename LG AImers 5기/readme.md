# LG AImers 5기

## 📌 프로젝트 개요
본 프로젝트는 LG AImers 5기에 참여하여, **차량 디스플레이 생산 공정 과정에서 발생하는 불량들을 예측하고 판별하는 AI 모델 개발**을 수행하였습니다.

- **예선**: `2024.08.01` ~ `2024.08.30`  
- **본선 (오프라인 해커톤)**: `2024.09.28` ~ `2024.09.29` 
- 팀프로젝트(5인)
- 🏆예선 : 4위/740팀, 본선 : 9위/27팀

## 📂 데이터
제공된 차량 디스플레이 생산 공정 데이터 활용
- **예선 데이터:** 
  - `train`: 40,506 rows × 465 columns  
  - `test`: 17,361 rows × 464 columns  
- **본선 데이터:** 예선 데이터에 4개 컬럼이 추가됨  
  - `train`: 40,506 rows × 469 columns  
  - `test`: 17,361 rows × 468 columns
 
## 🔍 EDA 및 데이터 전처리
- **Null 값 처리:**
  - 전체 행의 절반 이상이 결측치인 컬럼은 삭제  
  - 데이터 일부가 옆으로 밀려 있음 -> 밀려있는 값들을 수정 후 NULL 값 재확인  
- **데이터 타입 확인:**
  - 같은 값이지만 숫자형, 문자형으로 다르게 인식되는 데이터 -> 숫자형으로 변환  
- **범주형 처리:**  
  - `Model.Suffix`, `Workorder` 등의 컬럼에서 특정 패턴을 발견  
  - 단순 수치형 데이터가 아니라 범주형 변수로 변환  
- **중복 컬럼 제거:**  
  - 동일한 값을 갖는 컬럼이 다수 존재 → 한 개의 컬럼만 남김  
  - Machine Tact Time 제외하고 모두 범주형으로 처리
- **시간 파생 변수 생성:**  
  - 총 소요 시간, 각 공정의 소요 시간 등 시간 관련 파생 변수 생성
   
-> 모델링에 활용한 최종 데이터셋 크기 (본선 기준)
  - `train`: 40,506 rows × 121 columns  
  - `test`: 17,361 rows × 120 columns 

❗해당 데이터는 class 불균형이 심한 데이터
- Normal : 38,156 rows
- AbNormal : 2,350 rows

## 📈 모델링 
1. **모델 선택**
- `CatBoost`,`XGBoost`, `LGBM`,`Extreme Randomized Tree`,`TabNet`, `SVM` 등 다양한 모델 시도
- 대부분의 변수가 범주형이므로 범주형 데이터 처리에 뛰어난 `CatBoostClassifier`을 최종적으로 선택  

2. **하이퍼파라미터 튜닝**
- 클래스 불균형 문제를 고려하여 class_weights 튜닝
- Optuna를 활용하여 최적의 파라미터 탐색 : `iterations`, `depth`, `learning_rate`, `class_weights`, `l2_leaf_reg`  
  
3. **모델 검증 및 최종 예측**
- Train-Validation 7:3 Split 
- 5-Fold Cross Validation 적용
- StratifiedCV 및 Seed 변경  

-> 가장 안정적인 성능을 보이는 4개의 모델 선정하여 **Soft Voting 앙상블 모델** 생성

## 🔧 분석툴
파이썬
