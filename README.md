<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1B2A49,100:4A7BA7&height=220&section=header&text=Soonjae%20Lee&fontSize=50&fontColor=FFFFFF&fontAlignY=36&desc=Physics%20%C3%97%20Machine%20Learning&descSize=20&descAlignY=56" width="100%" alt="Soonjae Lee · Physics × Machine Learning"/>

<a href="mailto:soonjae.dev@gmail.com"><img src="https://img.shields.io/badge/Email-1B2A49?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>

</div>

---

## About

충북대학교 물리학과에서 머신러닝에 관심을 갖고 탐구하고 있습니다. 물리학을 배우며 습득한 정량적 문제 해결력을 기반으로 수학적 모델링, 시계열 분석을 위주로 다룹니다. LG Aimers 6기, POSTECH OIBC 빅데이터 챌린지에 참가하며 실제 데이터를 활용한 예측 모델 구축 경험을 쌓아가는 중입니다.

## Projects

### [Solar-Power-Forecasting](https://github.com/soonjae-dev/Solar-Power-Forecasting)

**Day-ahead PV forecasting · External NWP · 2026 POSTECH OIBC Big Data Challenge**

253개 태양광 발전소(42.7 MW)를 두 집합자원으로 묶고, 하루 전 17시에 시간별 발전량을 예측하는 대회 · with [@Xterbase](https://github.com/Xterbase)

- 최종 **134위 / 385팀** (상위 35%), 공식 베이스라인 대비 정산금 **+4,680만 원** (패널티 25% 감소)
- 서버 기준 성능 개선의 <b>91%</b>는 신규 정보 도입(제공 예보 기반 파생 변수 84개, GFS·LDAPS 외부 수치예보)에 기인
- 보정·튜닝·블렌딩의 기여는 수십만 원 수준에 그침
- 로컬 예측과 서버 결과 간의 오차 원인(검증 기간의 특정 연도 편중, 해당 연도의 과대예측 편향)을 [회고](https://github.com/soonjae-dev/Solar-Power-Forecasting/blob/main/docs/lessons.md)에 정리

### [IVF-Pregnancy-Prediction](https://github.com/soonjae-dev/IVF-Pregnancy-Prediction)

**Tabular ML · Leakage-free validation · LG Aimers**

256,351건의 시술 기록으로 임신 성공 여부를 예측한 LG Aimers 6기 해커톤 프로젝트

- 교차검증 분할 전 SMOTE 적용 및 GAIN 결측치 대치 과정의 타깃 변수 투입에 의한 데이터 누수를 식별하고, 각 누수의 영향 규모를 정량화
- 누수 제거 및 하이퍼파라미터 재튜닝 후 CV ROC-AUC를 0.89에서 out-of-fold 기준 **0.7385**(F1 **0.5156**)로 보정
- 보정된 기준선에서 SMOTE는 4개 모델 모두의 성능을 저하시켰으며, 앙상블의 기여는 +0.0002 AUC에 그쳐 단일 LightGBM을 최종 모델로 채택

## Focus

| Area | Interests |
| :--- | :--- |
| **Model Validation** | 시계열 교차검증 설계, 기준선 대비 성능 평가 |
| **Time-series Forecasting** | 수치예보(NWP) 등 외부 데이터를 활용한 시계열 예측 |

## Toolkit

<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/> <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch"/> <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white" alt="scikit-learn"/> <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy"/> <img src="https://img.shields.io/badge/SciPy-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white" alt="SciPy"/> <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git"/>

## Education

**Chungbuk National University · 충북대학교**<br>
B.S. in Physics · 2023.03 — Present

---

<div align="center">
<sub>Lee Soon-jae · Physics & Applied Machine Learning</sub>
</div>
