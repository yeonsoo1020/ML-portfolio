# 블랙보드 학습관리시스템(LMS) 데이터 분석 및 개선 연구

## 📌 프로젝트 개요
본 프로젝트는 **2022 블랙보드 데이터 분석·시각화 활용 공모전**에 참가하여, 블랙보드 만족도 조사 분석을 통해 개선사항 수렴 및 시스템 고도화 방안을 제시하고자 하였습니다. 이를 위해 **문/이과, 학부/대학원별 블랙보드 만족도 차이를 분석하고 개선 사항을 도출**하는 것을 목표로 하였습니다.  

- 진행기간 : `2023.01` 
- 팀프로젝트(5인)
- 🏆대상 수상
- [최종보고서](https://github.com/yeonsoo1020/portfolio/blob/main/%EB%B8%94%EB%9E%99%EB%B3%B4%EB%93%9C%20%EA%B3%B5%EB%AA%A8%EC%A0%84/%EB%B8%94%EB%9E%99%EB%B3%B4%EB%93%9C%20%EA%B3%B5%EB%AA%A8%EC%A0%84%20%EB%B3%B4%EA%B3%A0%EC%84%9C.pdf), [코드](https://github.com/yeonsoo1020/portfolio/blob/main/%EB%B8%94%EB%9E%99%EB%B3%B4%EB%93%9C%20%EA%B3%B5%EB%AA%A8%EC%A0%84/%EB%B8%94%EB%9E%99%EB%B3%B4%EB%93%9C%20%EA%B3%B5%EB%AA%A8%EC%A0%84.ipynb)

## 📝 역할
학부/대학원 만족도 차이 분석 및 시각화

## 🏷️ 주제 선정 배경
  - 코로나19 이후 온라인 학습 비중 증가로 LMS의 역할이 중요해짐에 따라 LMS 만족도를 분석하여 개선 방향 도출이 필요
  - 블랙보드 이용 실태를 분석하고 맞춤형 개선안 제시 

## 📂 활용 데이터
- **블랙보드 만족도 조사 데이터** : 교수학습개발원 원격교육센터 제공, 총 220명 응답


## 🔎 분석 방법
- **분석 대상** : 문과 vs 이과, 학부 vs 대학원 그룹별 만족도를 접근성, 학습성, 직관성 측면으로 세분화하여 비교  
- **독립표본 t-검정** : 문/이과, 학부/대학원의 만족도 차이 검정  
- **데이터 시각화** : 만족도 항목별 결과를 그래프, 트리맵, 워드클라우드로 표현  (파이썬 & 태블로 활용)  


## 📈 주요 분석 결과

#### 1. 전체 학생 만족도 
- 하루 1회 이상 접속 (70%), 오후(12~15시) 이용 많음  
- 주 사용 기능: Zoom 강의, 녹화 강의, 과제 제출  
- 개선 방향 : 모바일 앱 최적화, 강의 접속 오류 해결, HWP 파일 지원 확대  

#### 2. 문/이과 비교  
- 문과: 토론 선호, 이과 : 새벽·오전 이용↑, 과제·퀴즈 선호  
- 이과 학생의 접근성 만족도 낮음 
- 개선 방향 : UI/UX 개선, 자동 로그인 추가, 퀴즈 해설 제공  

#### 3. 학부/대학원 비교  
- 학부생 : 잦은 접속, 대학원생: 저녁 이용 많음, 토론 선호  
- 대학원생, 차세대 LMS 도입 희망↑
- 개선 방향 : 실시간 채팅 도입, 성적 평균 표시, 공지 푸시 알림 추가  


## 💡 의의 및 한계점 
#### 의의
- 블랙보드 만족도 분석을 통해 문/이과, 학부/대학원별 차이 파악  
- 접근성, 학습성, 직관성 개선 방향 제안으로 LMS 고도화 기여
#### 한계점
- 표본 수 220명 → 향후 데이터 확장 필요

## 🔧 분석툴
파이썬, 태블로
