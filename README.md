# 2025 AICS Bloom AI Stock Model 📈

## AI Model
### Data Processing
- 주식 데이터와 계절 데이터 병합
- 강수량 데이터의 결측치는 선형 보간법을 사용하여 보완

</br>

### Model Training
- 데이터 특성 상 

## Data 🧩
### Dataset

**1. 주식 데이터** (2024.01.01 - 2024.12.31 / KOSPI 기준 상위 10개 기업)
  - 일자
  - 기업명
  - 당일 시가 (주식 시장 열릴 때 가격)
  - 당일 고가 (장 중 최고 가격)
  - 당일 저가 (장 중 최저 가격)
  - 당일 종가 (장 마감 시 가격)
  - 당일 거래량 (해당 주식이 거래된 총 주식 수)
  - 전일 대비 가격 변화량 (종가 - 전일 종가)
  - 전일 대비 변화 비율 (가격 변화량 / 전일 종가 * 100)

![image](https://github.com/user-attachments/assets/14cf1762-0b54-4823-bfba-47b2f867be24)

</br>

**2. 계절 데이터** (2024.01.01 - 2024.12.31 / 전라북도 전주 기준)
   - 일 강수량 데이터
   - 일 평균 기온 데이터

### Raw Data
| 데이터명 | 기준 | 출처 | 링크 |
|:------:|:------:|:------:|:------:|
| 강수량 | 2024.01 - 2024.12 / 전북 전주시 | 기상청 기상자료개방포털 | https://data.kma.go.kr/stcs/grnd/grndRnList.do?pgmNo=69 |
| 기온 | 2024.01 - 2024.12 / 전북 전주시 | 기상청 기상자료개방포털 |  https://data.kma.go.kr/stcs/grnd/grndTaList.do?pgmNo=70 |
| KOSPI 상위 10개 종목 | 2024.01 - 2024.12 | KRX | FinanceDataReader |
