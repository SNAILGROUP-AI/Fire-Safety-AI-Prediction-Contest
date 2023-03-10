## 🔎 DF_OG

<details><summary><h3>수치형 변수</h3></summary>

- **유동인구정보 (28개 칼럼)**
  - 자료형 : 숫자형
  - 정보 : 통신사 제공 자료를 토대로 측정한 해당 row의 성별 및 연령별 유동인구수
  - 이상치 존재함
    - 4사분위수와 1, 2, 3사분위수 간 격차가 상당함
    - 모든 칼럼의 4사분위수가 네 자릿수 이상임
    - 이에 반해 3사분위수는 한 자릿수임
  - 세부 칼럼 목록
    - 남성 : `M00`, `M10`, `M15`, …, `M70` (14개)
    - 여성 : `F00`, `F10`, `F15`, …, `F70` (14개)

- **사고유형별 소방지수정보 (31개 칼럼)**
  - 자료형 : 숫자형
  - 정보 : 해당 row의 사고유형별 소방차량 출동횟수
  - 이상치 존재함
    - 모든 칼럼의 4사분위수는 2건을 넘지 않음
    - 모든 칼럼의 3사분위수는 0임
    - 즉, 0건의 비율이 매우 높음
    - 또한 하루 동안 동일 격자에 동일 사고유형으로 소방차량이 출동한 횟수는 최대 2건을 넘지 않음
  - 세부 칼럼 목록
<div align="center">

| 순번 | 사고유형(영문) | 사고유형(한글) | 비고 |
|---|---|---|---|
| 0 | HGTPOJ_ACDNT_OCRN_CNT | 고온체사고 |  |
| 1 | PNTRINJ_OCRN_CNT | 관통상 |  |
| 2 | MCHN_ACDNT_OCRN_CNT | 기계사고 |  |
| 3 | ETC_OCRN_CNT | 기타 |  |
| 4 | BLTRM_OCRN_CNT | 둔상 |  |
| 5 | ACDNT_INJ_OCRN_CNT | 사고부상 |  |
| 6 | EXCL_DISEASE_OCRN_CNT | 질병외 |  |
| 7 | VHC_ACDNT_OCRN_CNT | 탈것사고 |  |
| 8 | HRFAF_OCRN_CNT | 낙상 |  |
| 9 | AGRCMCHN_ACDNT_OCRN_CNT | 농기계사고 | 연간 총소방지수 0 |
| 10 | DRKNSTAT_OCRN_CNT | 단순주취 |  |
| 11 | ANML_INSCT_ACDNT_OCRN_CNT | 동물곤충사고 |  |
| 12 | FLPS_ACDNT_OCRN_CNT | 동승자사고 |  |
| 13 | UNKNWN_OCRN_CNT | 미상 |  |
| 14 | PDST_ACDNT_OCRN_CNT | 보행자사고 |  |
| 15 | LACRTWND_OCRN_CNT | 열상 |  |
| 16 | MTRCYC_ACDNT_OCRN_CNT | 오토바이사고 |  |
| 17 | THML_DAMG_OCRN_CNT | 온열손상 |  |
| 18 | DRV_ACDNT_OCRN_CNT | 운전자사고 |  |
| 19 | DRWNG_OCRN_CNT | 익수 |  |
| 20 | PRGNTW_ACDNT_OCRN_CNT | 임산부사고 |  |
| 21 | BCYC_ACDNT_OCRN_CNT | 자전거사고 |  |
| 22 | ELTRC_ACDNT_OCRN_CNT | 전기사고 |  |
| 23 | POSNG_OCRN_CNT | 중독 |  |
| 24 | ASPHYXIA_OCRN_CNT | 질식 |  |
| 25 | FALLING_OCRN_CNT | 추락 |  |
| 26 | FLAME_OCRN_CNT | 화염 |  |
| 27 | CHMC_SBSTNC_ACDNT_OCRN_CNT | 화학물질사고 |  |
| 28 | WETHR_ACDNT_OCRN_CNT | 날씨사고 | 연간 총소방지수 0 |
| 29 | SXAL_ASALT_OCRN_CNT | 성폭행 | 연간 총소방지수 0 |
| 30 | BURN_OCRN_CNT | 화상 |  |  

</div>
</details>

<details><summary><h3>범주형 변수</h3></summary>

- **지역정보 (5개 칼럼)**  
  - `GRID_ID`
    - 자료형 : 숫자형
    - 정보 : 공모전 주최 측에서 임의로 설정한 강원도 원주시 지역구분코드
    - 고유값 856개
  - `GRID_X_AXIS`
    - 자료형 : 숫자형
    - 정보 : 해당 row의 `GRID_ID`가 가리키는 X축 좌표
    - 고유값 41개
  - `GRID_Y_AXIS`
    - 자료형 : 숫자형
    - 정보 : 해당 row의 `GRID_ID`가 가리키는 Y축 좌표
    - 고유값 40개
  - `DONG_NM`
    - 자료형 : 문자열
    - 정보 : 해당 row의 실제 지역구분명(동/리 단위)
    - 고유값 74개
  - `DONG_CD`
    - 자료형 : 숫자형
    - 정보 : 해당 row의 실제 지역구분코드
    - 고유값 73개

- **발생일자정보 (1개 칼럼)**
  - `OCRN_YMD`
    - 자료형 : 문자열
    - 정보 : 해당 row의 발생일자 (년/월/일)
    - 12월에 해당하는 자료가 누락되어 있음

</details>
  
<details><summary><h3>설명변수와 종속변수 구분</h3></summary>

- **설명변수(Feature Columns)**
  - 지역정보
  - 발생일자정보
  - 유동인구정보

- **종속변수(Target Columns)**
  - 각 사고유형별 소방지수
  
</details>

---

## DF_CLEAN

<details><summary><h3>지역정보</h3></summary>

- **`GRID_ID`**
  - 2021년 동안 사고가 발생한 적이 없는 격자 616개
  - 2021년 동안 사고가 발생한 적이 있는 격자 240개
  - 연간 사고발생이 0건인 격자 삭제

- **`GRID_X_AXIS`, `GRID_Y_AXIS`** : 지도 시각화 이후 삭제 예정

- **`DONG_NM`, `DONG_CD`** : 외부 API 추가 이후 삭제 예정

</details>

<details><summary><h3>발생일자정보</h3></summary>

- **변수 `OCRN_YMD`를 네 개 변수로 세분화함**
  
      MONTH, WEEKDAY, SEASON, HOLIDAY

- **`YEAR`** : 발생년도에 관한 정보  
  - 예측하고자 하는 일자에 대하여 유의미한 정보를 제공한다고 볼 수 없으므로 삭제함
    - 모든 자료의 발생년도는 2021년임

- **`MONTH`** : 발생월에 관한 정보

      1, 2, 3, ..., 12

- **`DAY`** : 발생일에 관한 정보
  - 해당 변수는 범주형 변수에 해당하므로 값의 크기가 하니라 고유값이 중요함
  - 예측하고자 하는 일자에 대하여 유의미한 정보를 제공한다고 볼 수 없으므로 삭제함
    - 예측하고자 하는 일자
    
          28(2월)
          30(4, 6, 9, 11월)
          31(1, 3, 5, 7, 8, 10, 12월)
    
    - 해당 변수가 제공하고 있는 정보
    
          1, 2, ..., 27(1~12월)
          28, 29(1, 3, ..., 12월)
          30(1, 2, 3, 5, 7, 8, 10, 12월)

- **`SEASON`** : 발생계절에 관한 정보

      0 : 봄(3, 4, 5월)
      1 : 여름(6, 7, 8월)
      2 : 가을(9, 10, 11월)
      3 : 겨울(12, 1, 2월)

- **`HOLIDAY`** : 휴일여부에 관한 정보

      0 : 휴일아님(공휴일이 아닌 평일)
      1 : 휴일임(공휴일 및 주말)
    
</details>

<details><summary><h3>유동인구정보</h3></summary>

- **성별 및 유사생활패턴에 따라 적절히 결합하여 7개 변수로 재구분함**
  
      PEOPLE, MAN, WOMAN, CHILD, YOUTH, MIDDLE, OLDER

- **`PEOPLE`** : 총유동인구

- **성별에 따른 구분**
  - `MAN` : 남성유동인구; `M00`, `M10`, `M15`, …, `M70`
  - `WOMAN` : 여성유동인구; `F00`, `F10`, `F15`, …, `F70`

- **유사생활패턴에 따른 구분**
  - `CHILD` : 미성년
    - 20세 미만 남성 및 여성
    - 미취학아동 및 초/중/고등학생으로서 보호자에 의해 활동이 제약되는 나이
  - `YOUTH` : 청년
    - 20세 이상 35세 미만 남성 및 여성
    - 자기결정권을 지니고 직장 등으로부터 비교적 자유로운 나이
  - `MIDDLE` : 중장년
    - 35세 이상 60세 미만 남성 및 여성
    - 경제권을 지니고 주로 직장에 상주하는 나이
  - `OLDER` : 노년
    - 60세 이상 남성 및 여성
    - 직장에서 은퇴하고 신체가 쇠약한 나이

</details>

<details><summary><h3>설명변수 종합</h3></summary>

- **범주형 변수**
  - 지역정보 : `GRID_ID`, ~`GRID_X_AXIS`~, ~`GRID_Y_AXIS`~, ~`DONG_NM`~, ~`DONG_CD`~
  - 발생일자정보 : `MONTH`, `WEEKDAY`, `SEASON`, `HOLIDAY`

- **수치형 변수**
  - 유동인구정보 : `PEOPLE`, `MAN`, `WOMAN`, `CHILD`, `YOUTH`, `MIDDLE`, `OLDER`

</details>

---

## DF_EDA

<details><summary><h3>설명변수와 총소방지수 간 상관관계 확인</h3></summary>

![상관계수](https://user-images.githubusercontent.com/116495744/206858084-63bd7d86-5ac2-4b07-a07a-4d45836689a3.png)

![1_기간별 총소방지수 비교](https://user-images.githubusercontent.com/116495744/206858096-a82cb69a-c431-4c41-af1e-e912a967f636.png)

</details>

<details><summary><h3>사고유형별 연간 총소방지수 비교</h3></summary>

![2-1_사고유형별 연간 총소방지수 비교](https://user-images.githubusercontent.com/116495744/206866048-fc723d71-2e5b-4e95-81a7-75e12f43901c.png)

- **`낙상(HRFAF_OCRN_CNT)` 연간 총소방지수가 다른 사고유형의 연간 총소방지수보다 압도적으로 높음**
  - `낙상(HRFAF_OCRN_CNT)` 연간 총소방지수는 `총소방지수(TOTAL_CNT)`의 약 34.70%를 차지함
    - 모든 사고유형의 소방지수를 종합한 `총소방지수(TOTAL_CNT)`는 2827건임
    - `낙상(HRFAF_OCRN_CNT)` 연간 총소방지수는 981건임
  - 첫 번째로 높은 사고유형과 두 번째로 높은 사고유형의 소방지수 간에는 약 4배의 격차가 있음
    - 두 번째로 높은 `질병외(EXCL_DISEASE_OCRN_CNT)` 총소방지수는 239건임

- **연간 총소방지수가 0건인 사고유형이 존재함**
  - `농기계사고(AGRCMCHN_ACDNT_OCRN_CNT)`
  - `날씨사고(WETHR_ACDNT_OCRN_CNT)`
  - `성폭행(SXAL_ASALT_OCRN_CNT)`

</details>

<details><summary><h3>사고유형별 건당 총유동인구수 비교</h3></summary>
  
![3_사고유형별 건당 유동인구수 비교](https://user-images.githubusercontent.com/116495744/206866096-b2cf2a9b-1552-49f1-a690-bc71feabc148.png)

- **사고유형별 연간 총소방지수와 건당 평균유동인구수 간 양의 상관관계가 존재한다고 볼 수 없음**

  - 연간 총소방지수 하위권 사고유형이 평균유동인구수도 반드시 하위권으로 나타나지는 않음
    - 연간 총소방지수가 1건인 `관통상(PNTRINJ_OCRN_CNT)`의 평균유동인구수가 가장 높음
  - 연간 총소방지수 상위권 사고유형이 평균유동인구수도 반드시 상위권으로 나타나지는 않음
    - 반면, 연간 총소방지수가 가장 높은 `낙상(HRFAF_OCRN_CNT)`의 평균유동인구수는 중위권임

</details>

<details><summary><h3>사고유형당 기간별 소방지수 비교</h3></summary>

- **계절별**

  ![4_사고유형당 기간별 소방지수 비교](https://user-images.githubusercontent.com/116495744/206866127-677e2b81-7b1e-49db-a621-1901dcc0ec8a.png)  

- **월별**
  
  ![4-1](https://user-images.githubusercontent.com/116495744/206866184-6727bb86-32ee-482e-b5f2-f8229af58548.png)

- **요일별**
  
  ![4-2](https://user-images.githubusercontent.com/116495744/206866200-e1217f56-7230-4f22-a00f-c0ef1aca8708.png)

- **휴일여부**  
  
  ![4-3](https://user-images.githubusercontent.com/116495744/206866201-3ab3cfc2-1430-430e-946b-e6e4362eb146.png)

- **전반적으로 봤을 때, 각 사고유형 소방지수의 기간별 양상이 `총소방지수(TOTAL_CNT)`와 유사하다고 볼 수 없음**
  - 계절별 : 가을, 여름, 봄, 겨울 순으로 소방지수가 높은 양상을 보이는 사고유형이 많지 않음
  - 월별 : 7월 소방지수가 높은 사고유형이 많지 않음
  - 요일별 : 수요일 소방지수가 가장 낮고, 수요일에서 멀어질수록 소방지수가 높아지는 양상을 보이는 사고유형이 많지 않음
  - 단, 휴일여부의 경우, 모든 사고유형에 대하여 휴일인 경우가 휴일아님인 경우보다 소방지수가 높지 않음

- **`낙상(HRFAF_OCRN_CNT)` 소방지수의 기간별 양상이 `총소방지수(TOTAL_CNT)`와 유사함**
  - 앞서 `낙상(HRFAF_OCRN_CNT)` 연간 총소방지수가 압도적으로 높다는 점을 확인했음
  - `총소방지수(TOTAL_CNT)` 집계 및 시각화 결과가 `낙상(HRFAF_OCRN_CNT)`에 편향된 결과로 나타난 것으로 보임
  - 다만, `낙상(HRFAF_OCRN_CNT)` 월별 소방지수의 경우, `총소방지수(TOTAL_CNT)`와 달리 7월이 아닌 8월이 가장 높았음
  
  
</details>

<details><summary><h3>사고유형 건당 평균 유동인구수 비교</h3></summary>

- **성별**
  
  ![5-1](https://user-images.githubusercontent.com/116495744/206866508-2b6b6595-10f6-4e9b-8034-3f944e02f9d0.png)

- **연령 및 생활패턴별**
  
  ![5_사고유형 건당 유동인구수 비교](https://user-images.githubusercontent.com/116495744/206866520-0fdf24ba-7d42-435f-9cb6-b6e352fc218d.png)

  
</details>
