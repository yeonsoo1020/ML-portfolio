# 전통시장 활성화를 위한 청년몰 입지 예측 및 운영 전략  

## 📌 프로젝트 개요
본 프로젝트는 2024 빅콘테스트 공모전에 참가하여, 데이터분석 분야의 OD데이터 분석을 통한 활용방안을 제시하고자 하였습니다. 이를 위해 "**전통시장 활성화를 위한 청년몰 입지 예측 및 운영 전략-OD데이터 분석을 중심으로**"이라는 주제를 정하고 분석을 진행하였습니다.

- 진행기간 : `2024.09` ~ `2024.11` 
- 팀프로젝트(4인)
- [최종보고서](https://github.com/yeonsoo1020/portfolio/blob/main/OD%20%EB%8D%B0%EC%9D%B4%ED%84%B0%20%EB%B6%84%EC%84%9D/%EB%8D%B0%EC%9D%B4%ED%84%B0%EB%B6%84%EC%84%9D%EB%B6%84%EC%95%BC_%EC%B2%AD%EB%85%84%EB%AA%B0%ED%8B%B0%EC%A0%B8%EC%8A%A4%ED%8C%80_%EA%B2%B0%EA%B3%BC%EB%B3%B4%EA%B3%A0%EC%84%9C.pdf)

## 📝 역할
주차장 데이터 수집, Variable Selection, 모델링, 초량2동 유동인구 및 체류인구 분석, 고객 클러스터링

## 🏷️ 주제 선정 배경
- 전통시장은 현대 소비 패턴 변화로 인해 쇠퇴하고 있으며, 청년몰 사업이 활성화 방안으로 도입되었으나 효과적인 입지 선정과 운영 전략이 부족한 상황
- 데이터 분석을 통해 최적의 청년몰 입지를 선정하고, 맞춤형 운영 전략을 제안하여 전통시장 활성화를 도모하는 것이 목표

## 📂 활용 데이터
공모전에서 제공되는 SKT 유동인구 데이터 및 외부 데이터 활용

| 출처 | 데이터 | 설명 |
|------|--------|------|
| SKT | 유동인구, 체류인구 | 행정동 간 유동인구, 행정동별 체류인구 데이터 |
| 행정안전부 | 주민등록인구 | 지역별 주민등록 인구수 도출 |
| 국토교통부 | 주차장, 버스정류장 정보 | 전통시장 반경 500m 내 주차장, 버스정류장 수 도출 |
| 블랙키위 | 키워드 검색량, 콘텐츠 발행량 | 특정 전통시장의 관심도를 반영하는 검색량 데이터 |
| 소상공인시장진흥공단 | 전통시장별 점포 수, 편의시설 수 | 전국 전통시장의 점포 수, 편의시설 현황 데이터 |
| 소상공인시장진흥공단 | 청년몰 영업률 | 2023년 기준 전국 청년몰의 영업률 데이터 |


## 🔎 분석 방법
**1. 전통시장별 데이터 구축**  
   - 인구특성, 교통 접근성, 시장 인프라, 관심도를 나타내는 데이터 수집
   - 상관계수, Feature Importance, Variable Selection 결과를 종합적으로 고려하여 주요 변수 선택 후 최종 데이터셋 구축
   
**2. 영업률 예측 모델**  
   - `RandomForestRegressor`, `XGBRegressor` 등의 모델을 활용
         
**3. 최적 청년몰 입지 선정**
   - 점포 수, 운영률, 교통 접근성 등을 고려하여 후보 전통시장 9곳 선정 
   - 예측된 영업률을 기준으로 청년몰 조성에 가장 적합한 시장 선정 (최종: `초량전통시장`)
 
## 📈 활용 방안 
**1. 홍보 전략: 부산역 광고 활용**
- 체류인구 분석 결과 인접한 부산역과의 유사한 분포 → 부산역의 유동인구 분석을 통해 주요 이용층 확인  
- 부산역 내 디지털 광고판을 활용하여 청년몰 홍보 진행  
- 광고 최적 시간대를 파악해 집중 타겟팅 방안 제시  

**2. 운영 전략: 주말 야시장 활성화**
- 체류인구 분석 결과, 주말 저녁 시간대에 여행·쇼핑여가 목적의 인구 증가
- 해당 행정동의 야경 명소(`북항친수공원`)와 연계한 "야경과 함께하는 청년 야시장" 기획  
- 야경명소와 야시장을 연계한 관광콘텐츠를 통해 공원과 시장활성화의 시너지 효과 기대

**3. 고객 맞춤형 전략 (K-means 클러스터링)**
   
유동인구 데이터를 활용해 방문객의 패턴을 분석한 결과 3개의 유형으로 분류 → 각 고객군별 맞춤형 운영 전략 제안

  | 주요 특징 | 대표 방문객 예상 | 맞춤 운영 전략 |
  |----------------------|----------------------|-----------------------|
  | 주말 방문, 장거리 이동 | 관광객, 여행객 | 포토존과 SNS 이벤트, 저녁 라이브 공연과 먹거리 투어, 청년몰 루트 지도 제공 |
  | 평일 방문, 단거리 이동, 청년 남성 비율 높음 | 직장인, 인근 거주자 | 점심시간 및 해피아워 프로모션, 리프레시 프로그램 |
  | 평일 방문, 단거리 이동, 중년 여성 비율 높음 | 지역 주민, 인근 거주자 | 지역 특산물 판매, 주부 대상 체험 프로그램 |

## 💡 의의 및 한계점 
#### 의의
- 청년몰 현황 및 분석 필요성 제고 
- 청년몰 최적 입지 선정
- 관광객 유치를 위한 방안 제안
- 클러스터링을 통한 고객군 파악
#### 한계점 및 개선방안
- 정성적 요인 반영의 어려움 → 소비자 설문조사 및 상인 인터뷰 데이터 등을 추가하여 보완 필요
- 행정동 단위 데이터로 인해 실제 상권의 세부적 특성을 반영하는 데 한계 → 개별 인구 단위 및 카드 매출 데이터 등을 활용하여 보다 정밀한 입지 분석이 필요  

## 🔧 분석툴
파이썬
