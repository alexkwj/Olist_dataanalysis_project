## [1] 분석 개요
# E‑Commerce Data Analysis

> 본 프로젝트는 Olist가 제공하는 E‑Commerce Public Dataset을 활용하여 이커머스 시장의 다양한 데이터 분석을 수행한 결과물입니다.
>
> Olist의 “1회성 고객을 재구매 고객으로: 이탈 방지 요인 분석 및 전략 제안” 
> 전자상거래 플랫폼의 매출에 중요한 재구매고객의 비중을 높이고, 안정적 매출향상을 위한 로열티를 구축해야 한다. 
---

## [1] 분석 개요

- **분석 질문**: 어떻게 하면 1회성 구매고객의 이탈을 방지하고 재구매고객으로 전환할 수 있을까? 
    - 전자상거래 플랫폼의 매출에 중요한 재구매고객의 비중
    - Olist 플랫폼의 재구매고객은 3%, 1회성 구매고객 97%
    - 고객경험단계에서 1회성 구매고객의 이탈구간을 파악해 이탈방지 및 재구매고객으로 전환
  
- **기대 효과**: "고객경험 개선을 통해 1회성고객의 재구매전환 및 로열티 강화"

---

## [2] 주요 분석 결과

 고객경험 4단계 '주문단계->결제단계->배송단계->사후관리단계(리뷰)' 에서
 재구매고객과 1회성구매고객의 패턴을 분석해 
 Olist 고객의 재구매 전환 및 이탈 포인트를 찾았습니다.

- **인사이트 1**
    : 고객경험 4단계 중 '주문단계','배송단계','사후관리단계(리뷰)'는 재구매전환율과 큰 관계가 없다. 
  
- **인사이트 2**
    : 고객경험 4단계 중 '결제단계' 가 재구매고객과 1회성구매고객의 현저한 차이를 보이는 구간이다.
    : '결제단계' 중 '결제취소건 및 결제불가능건'의 90%가 1회성구매고객이다. 

- **인사이트 3**
    : 결제취소건의 결제수단은 voucher가 전체 평균에 비해 높았기에 기존의 voucher 프로모션이 효과적이지 않다는 것을 파악했다.  
    : 결제불가능건의 결제수단은 boleto가 전체 평균에 비해 높았기에 boleto 결제시스템에 Olist 호환성 등 문제점을 파악했다. 
    : 결제취소 건의 결제시점 대비 예상배송일이 지나치게 길었고, 실제배송일보다도 길게 설정되어있음을 파악했다.   

## [3] 시사점

- **시사점 1**
- Voucher 프로모션 개선 : 기존 첫구매유도 voucher 프로모션을 재구매유도 프로모션으로 개선한다. 
- **시사점 2**
- Boleto 결제시스템 개선 :  Olist 호환성을 높이고, 별도의 결제시한 알람 서비스등의 장치를 마련한다.
- **시사점 3**
- 예상배송일 UX 개선 : 플랫폼 내 판매자와의 협의를 통해 예상배송일을 단축한다. 

# 사용 기술
- Language: Python 3.11
- Libraries: Pandas, Matplotlib, Seaborn 등
- Environment: Jupyter Notebook

## [3] 프로젝트 구조

```
ecommerce-analysis/
├── README.md
├── .gitignore
├── requirements.txt
├── notebooks/
│   └── analysis.ipynb
├── src/
│   ├── preprocessing.py
│   └── visualization.py
└── data/   (※ 실제 저장소에는 포함하지 않으며, .gitignore로 관리)
```

- `notebooks/` : 데이터 분석 및 시각화용 Jupyter 노트북
- `src/` : 데이터 전처리, 함수, 시각화 등 파이썬 코드
- `requirements.txt` : 분석에 필요한 Python 패키지 목록

## [4] 데이터셋 안내

이 프로젝트는 데이터 파일을 직접 저장소에 포함하지 않습니다.
데이터셋은 아래 링크를 통해 다운로드하신 후, 로컬 환경의 `data/` 폴더에 직접 저장해 주시기 바랍니다.

- **Dataset:** E‑Commerce Public Dataset by Olist
- **Provider:** Olist (via Kaggle)
- **Original Link:** [Kaggle URL](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
- **License:** [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)

**※ 다운로드 방법**

1. 위의 Kaggle 링크에서 데이터셋을 다운로드합니다.
2. 본인의 로컬 저장소 내에 `data/` 폴더를 생성하고, 압축을 해제한 csv 파일을 해당 폴더에 저장합니다.

---

## [5] 데이터셋 라이선스 및 사용 조건

`CC BY-NC-SA 4.0` 라이선스를 따르므로, 데이터 사용 시 해당 라이선스 규정을 준수해야 합니다. 데이터의 상업적 이용 및 원본 라이선스와 다른 조건의 2차 배포는 금지됩니다.
자세한 사항은 [CC BY-NC-SA 4.0 라이선스 안내](https://creativecommons.org/licenses/by-nc-sa/4.0/)를 참고하시기 바랍니다.