# 클라우드 기반 AI 모델을 이용한 DDos 공격 탐지 및 완화

## 목차
1. [프로젝트 개요](#프로젝트-개요)
   - [연구 동기](#연구 동기)
   - [관련 연구와의 차별점](#관련 연구와의 차별점)
   - [개발 기간](#개발-기간)
   - [주요 기능](#주요-기능)
2. [모델 설계](#모델 설계)
3. [아키텍처](#아키텍처)
   - [서비스 아키텍처](#서비스-아키텍처)
   - [플로우차트](#플로우차트)
   - [ERD](#데이터베이스)
4. [기능 상세 설명](#기능-상세-설명)

<br><br><br>

## 프로젝트 개요 
### 제작 이유
- 최근 증가한 DDos공격을 탐지하고 예방하기 위한 챗봇 개발

### 개발 기간 
- 2024.10.20 ~ 2024.12.09
   #### 세부 일정
  - 1주차 (~10/28): 데이터 전처리 및 모델 학습 준비 , CICIDS2017 데이터셋 전처리
  네트워크 트래픽 데이터를 LLM 모델에 맞게 토크나이징 작업 완료. BERT모델 학습
  학습 결과 분석 및 성능 평가 지표(정확도, 재현율, 정밀도) 측정.
  - 2주차 (10/29~11/17): LLM 모델 학습 완료RoBERTa, GPT(GPT-3, GPT-4), XLNet, T5 모델 학습.
  학습 결과 분석 및 성능 평가 지표(정확도, 재현율, 정밀도) 측정.
  - 3주차 (11/18~11/22): 상위 3개 모델 선정 및 앙상블 구성
  성능 평가 결과에 따라 상위 3개의 모델 선정.
  Voting 또는 가중치 기반 앙상블 모델 구성.
  - 4주차 (11/23~12/3): 데이터 증강 적용
  데이터 증강 기법 적용하여 네트워크 트래픽 데이터 변형 및 추가 학습.
  앙상블 모델에 데이터 증강 적용 후 성능 평가.
  - 5주차 (12/4~12/6): 모델 설명력 확보
  SHAP, LIME을 통해 앙상블 모델의 예측 과정 해석.
  설명 가능한 AI 기법을 통한 모델 설명력 분석.
  - 6주차 (12/7~12/9): 최종 평가 및 보고서 작성
  최종 성능 평가 및 데이터 증강과 모델 해석 가능성 결과 정리.
  최종 보고서 작성 


