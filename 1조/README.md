[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FDataScience-Lab-Yonsei%2F9th_EDA%2F1%25E1%2584%258C%25E1%2585%25A9&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)



## 금융(KOSPI 일간 등락, 종가, 시가 등의 금융 관련 데이터)
#### 참여자 : 도승범, 서연우, 신소연, 유선재, 정주영
#### EDA 프로젝트 자료 소개
> * Dataset
>   * [kospi_data.csv](https://dacon.io/competitions/official/235980/data) : KOSPI의 일간 등락률, 종가, 시가 등의 정보를 담고 있는 데이터
>   * [kosdaq_data.csv](http://data.krx.co.kr/contents/MDC/MAIN/main/index.cmd) : KOSDAQ의 일간 등락률, 종가, 시가 등의 정보를 담고 있는 데이터
>   * [nasdaq_data.csv](https://kr.investing.com/indices/nasdaq-composite) : NASDAQ의 일간 등락률, 종가, 시가 등의 정보를 담고 있는 데이터 
>   * [S&P_data.csv](https://kr.investing.com/indices/us-spx-500) : S&P500의 일간 등락률, 종가, 시가 등의 정보를 담고 있는 데이터 
>   * [volume_investors.csv](http://data.krx.co.kr/contents/MDC/MAIN/main/index.cmd) : 투자자 유형별 일별 순매수금액을 담고 있는 데이터
>   * [소비지출.xlsx](https://ecos.bok.or.kr/#/SearchStat) : 통계청 분기별 가계소비지출 데이터
>   * [반도체.csv](https://kosis.kr/statHtml/statHtml.do?orgId=127&tblId=DT_092_115_2009_S023&conn_path=I2) : 통계청 월별 반도체 수출액 데이터 
>   * [삼성전자.csv](http://data.krx.co.kr/contents/MDC/MAIN/main/index.cmd) : 삼성전자 주식의 일간 등락률, 종가, 시가 등의 정보를 담고 있는 데이터
>   * [sk하이닉스.csv](http://data.krx.co.kr/contents/MDC/MAIN/main/index.cmd) : SK하이닉스 주식의 일간 등락률, 종가, 시가 등의 정보를 담고 있는 데이터
>   * [KOVIX.csv](http://data.krx.co.kr/contents/MDC/MAIN/main/index.cmd) : VKOSPI의 일간 등락률, 종가, 시가 등의 정보를 담고 있는 데이터
>   * [지표.csv](https://datacenter.hankyung.com/economic-calendar) : 경제지표 발표일정
> * [1조 EDA 발표자료](https://github.com/SeungbeomDo/9th_EDA/blob/main/1%E1%84%8C%E1%85%A9/EDA_1%EC%A1%B0_%EB%B0%9C%ED%91%9C%EC%9E%90%EB%A3%8C.pdf) : EDA 발표 때 사용한 ppt
> * [1조 EDA 코드](https://github.com/SeungbeomDo/9th_EDA/tree/main/1%E1%84%8C%E1%85%A9/EDA_1%EC%A1%B0_%EC%BD%94%EB%93%9C) : EDA 발표와 관련하여 사용된 코드. 이하 tree 참조
<br>



## EDA 프로젝트 요약

1. 데이터 소개

        - kospi_data.csv : KOSPI의 일간 등락, 종가, 시가 등의 정보를 담고 있는 데이터
   
2. 데이터 전처리

        - 주가 시계열 자체의 비정상성을 감안하여, 로그 차분을 통해 정상시계열화(수익률 시계열)
 
3. 분석 방법 및 결과
    
        - 1월효과, 연말효과, 서머랠리, 월요일효과 등 주식시장의 이례현상(Anormalies) 존재 여부 가설 검정
        - 존재한다고 검정된 이례현상에 대하여 경제학/경영학 이론 기반 가설 제시
        - 설명가설의 타당성 검토하기 위한 통계적 검증
    
4. 결론

        - 월요일효과 존재: 금요일 장마감 이후 축적된 미반영 정보들에 의해 월요일 시장의 변동성 증가, 월요일 주가 수익률 하락 압력
        - 연말효과 존재: 연말 경기 호조에 따른 주가 상승 압력과 절세전략 및 배당금 효과에 의한 주가 등락의 전형적 패턴 존재
        - 1월효과 존재: 연말 주가 하락에 따른 기저효과에 기인, 특히 개인투자자 영향력 큰 코스닥에서 더 뚜렷한 패턴 발견
        - 서머랠리 존재: 3분기 반도체 산업 호황에 대한 선반영, 상반기 양호한 수익률에 기반한 기관투자자들의 낙관주의
    
5. 아쉬운 점
    
        - 존재하는 이례현상들에 대하여 부분적인 설명만 제시할 뿐, 완벽한 설명으로는 부족함

6. 추가로 하면 좋을 분석 방법
    
        - 분석에서 다룬 이례현상들을 기반으로, 실제 투자 수익을 거둘 수 있는지 백테스팅
<br>



 ## 각 팀원의 역할
 
|이름|활동 내용| 
|:---:|:---| 
|도승범| -프로젝트 리딩 <br> -통계/금융 이론 및 코드 구현 조언<br>| 
|서연우| -프로젝트 리딩 <br> -1월효과 존재 여부 가설 검정<br> -1월효과 설명 가설 제시 및 검정<br> -1월효과 관련 기타 시각화<br> -발표|
|신소연| -연말효과 존재 여부 가설 검정<br> -연말효과 설명 가설 제시 및 검정<br> -연말효과 관련 기타 시각화<br> -발표 자료 제작|
|유선재| -월요일효과 존재 여부 가설 검정<br> -월요일효과 설명 가설 제시 및 검정<br> -월요일효과 관련 기타 시각화<br>|
|정주영| -서머랠리 존재 여부 가설 검정<br> -서머랠리 설명 가설 제시 및 검정<br> -서머랠리 관련 기타 시각화<br>|
<br/>



## tree 
```bash
├── Dataset
│   ├── kospi_data.csv
│   ├── kosdaq_data.csv
│   └── nasdaq_data.csv
│   └── S&P_data.csv
│   └── volume_investors.csv
│   └── 반도체.csv
│   └── 삼성전자.csv
│   └── sk하이닉스.csv
│   └── 소비지출.xlsx
│   └── KOVIX.csv
|
├── 도승범
│   └── dummy.txt
├── 서연우
│   └── 기초세션과제
├── 신소연
│   └── 기초세션과제
├── 유선재
│   └── 기초세션과제
├── 정주영
│   └── 기초세션과제
│
├── EDA_1조_발표자료.pdf
├── EDA_1조_코드
│   ├── 월요일효과
|   │     ├── 월요일_평균_수익률.ipynb : 월요일 효과 가설 검정 코드
|   │     └── 요일별_변동성.ipynb : 요일별 VKOSPI 지수 비교하는 코드
|   │     └── 경제지표.ipynb : 요일별 경제지표 발표 횟수 비교 코드
|   │     └── 월요일효과_all_date.ipynb : 여타 국가의 월요일 효과 가설 검정 코드
│   └── 연말효과
|   │     ├── 분기별_소비지출.ipynb : 분기별 소비지출 비교 코드
|   │     └── 수익률_코드_정리.ipynb : 월간, 분기간 수익률 산출 코드
|   │     └── 순매수_코드_정리.ipynb : 12월 동안의 거래주체별 순매수량 비교 코드
│   └── 1월효과
│   │     ├── 1월_코스피_코스닥_비교.ipynb : 1월 동안의 코스피, 코스닥 종가 패턴 비교 코드
│   │     └── 1월효과.ipynb : 1월 효과 가설 검정 코드
│   │     └── 1월효과_all_data.ipynb : 여타 국가의 1월 효과 가설 검정 코드
|   └── 서머랠리
│         ├── 기업_주가변화율과_반도체_수출금액_변화율_상관관계.ipynb : 주가변화율과 반도체 수출액 상관관계 분석 코드 
│         └── 반도체_수출금액.ipynb : 월간 반도체 수출금액 분석 코드
│         └── 상반기_수익률_7월_주가.ipynb : 상반기 수익률에 따른 7월 주가 패턴 분석 코드
│         └── 코스피_등락률과_대기업_주가변화율_상관관계.ipynb : 코스피 및 대기업 주가변화율 상관분석 
└── README.md
``` 
