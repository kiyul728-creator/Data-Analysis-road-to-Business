# 📘 SQL_BASIC 5주차 정규 과제

SQL_BASIC 정규 과제는 매주 정해진 분량의 `초보자를 위한 BigQuery(SQL) 입문` 강의를 듣고, 핵심 개념을 정리한 뒤 간단한 SQL 문제를 직접 풀어보는 방식으로 진행합니다.

이번 주는 날짜/시간 데이터와 조건문을 학습합니다. 특히 `CASE WHEN`은 SQL 문제 풀이와 데이터 분석에서 자주 사용되므로, 직접 분류 기준을 만들고 결과를 확인하는 연습을 해주세요.

완성된 과제는 Github에 업로드하고, 링크를 스프레드시트 'SQL' 시트에 입력해 제출해주세요.

**👀 수행 인증란은 필수입니다.**

---

## 📚 SQL_BASIC_5th_TIL

### 섹션 5. 데이터 탐색 - 변환

### 4-4. 날짜 및 시간 데이터 이해하기

### 4-6. 조건문(CASE WHEN, IF)

--- 

## ✨ 선택 강의

- 4-5. 시간 데이터 연습문제: 날짜/시간 함수를 더 연습하고 싶을 때 선택 수강
- 4-7. 조건문 연습문제: CASE WHEN과 IF를 더 연습하고 싶을 때 선택 수강

---

## 🏁 전체 강의 수강 계획

| 주차 | 필수 강의 범위 | 선택 강의 | 완료 여부 |
| --- | --- | --- | --- |
| 1주차 | 1-1 ~ 2-1 | 1 | ✅ |
| 2주차 | 2-2 ~ 2-3 | 2-4 | ✅ |
| 3주차 | 2-5, 2-7 ~ 2-8 | 2-6 | ✅ |
| 4주차 | 3-2 ~ 4-3 | 3-4 | ✅ |
| 5주차 | 4-4 ~ 4-6 | 4-5, 4-7 | ✅ |
| 6주차 | 5-2 ~ 5-5 | 5-6 | 🍽️ |
| 7주차 | 필수 강의 없음 | 6-2, 6-3, 6-4, 6-5 | 🍽️ |

---

<br>

<!-- 여기까진 그대로 둬 주세요-->

---

# 1️⃣ 개념 정리

아래 키워드 중 중요하다고 생각한 개념을 2개 이상 골라 짧게 정리해주세요. 3개보다 더 많이 정리하고 싶다면 자유롭게 항목을 추가해도 좋습니다.

이번 주 키워드:
- DATE
- DATETIME
- TIMESTAMP
- EXTRACT
- DATETIME_TRUNC
- FORMAT_DATETIME
- CASE WHEN
- IF

## 01.

```
개념 이름: DATETIME

개념 설명: DATE와 TIME 까지 표시하는 데이터로서 TIME ZONE 정보가 없다 EX. 2026-10-02-21:43

예시 쿼리: DATTIME(TIMESTAMP_MILLIS(1704176819711)) AS DATETINE_VALUE
(TIMESTAMP를 DATTIME으로 바꾸는 쿼리)

```

## 02.

```
개념 이름: TIMESTAMP

개념 설명: DATETIME 값 + TIME ZONE 정보까지 있는 값으로 UTC(Universal Time Coordinated)로부터 경과한 시간을 나타낸다 / 한국시간 : UTC+9

예시 쿼리: TIMESTAMP_MILLIS(1704176819711) AS milli_to_timestamp_Vlaue
(millisecond 값을 TIMESTAMP 값으로 바꾸는 쿼리)
```

## (선택) 03.

```
개념 이름: FORMAT_DATIME

개념 설명:DATETIME 데이터를 특정 형태의 문자열로 변환하고 싶은경우 사용한다

헷갈린 점:
문자열 => DATETIME : PARSE_DATETIME(파싱 데잇 타임)
DATETIME => 문자열 : FORMAT_DATETIME

```

---

# 2️⃣ 수행 인증란
  ![alt text](week5_image/스크린샷(821).png) ![alt text](week5_image/스크린샷(822).png) ![alt text](week5_image/스크린샷(824).png) ![alt text](week5_image/스크린샷(825).png) ![alt text](week5_image/스크린샷(826).png) ![alt text](week5_image/스크린샷(827).png) ![alt text](week5_image/스크린샷(828).png) ![alt text](week5_image/스크린샷(829).png) ![alt text](week5_image/스크린샷(830).png) ![alt text](week5_image/스크린샷(831).png) ![alt text](week5_image/스크린샷(832).png) ![alt text](week5_image/스크린샷(833).png) ![alt text](week5_image/스크린샷(834).png) ![alt text](week5_image/스크린샷(835).png) ![alt text](week5_image/스크린샷(836).png) ![alt text](week5_image/스크린샷(837).png) ![alt text](week5_image/스크린샷(838).png) ![alt text](week5_image/스크린샷(839).png) ![alt text](week5_image/스크린샷(840).png) ![alt text](week5_image/스크린샷(841).png) ![alt text](week5_image/스크린샷(842).png) ![alt text](week5_image/스크린샷(844).png) ![alt text](week5_image/스크린샷(845).png) ![alt text](week5_image/스크린샷(846).png) ![alt text](week5_image/스크린샷(847).png) ![alt text](week5_image/스크린샷(848).png) ![alt text](week5_image/스크린샷(849).png) ![alt text](week5_image/스크린샷(850).png) ![alt text](week5_image/스크린샷(851).png) ![alt text](week5_image/스크린샷(852).png) ![alt text](week5_image/스크린샷(853).png) ![alt text](week5_image/스크린샷(854).png) ![alt text](week5_image/스크린샷(855).png)
---

# 3️⃣ 확인 문제

프로그래머스는 로그인이 필요하므로, 로그인 후 문제 풀이를 진행해주세요.

## 🧩 문제 1

문제 링크: [자동차 대여 기록에서 장기/단기 대여 구분하기](https://school.programmers.co.kr/learn/courses/30/lessons/151138)

풀이 과정:
```SQL
SELECT
    HISTORY_ID,
    CAR_ID,
    DATE_FORMAT(START_DATE, '%Y-%m-%d') AS START_DATE,
    DATE_FORMAT(END_DATE, '%Y-%m-%d') AS END_DATE,
    CASE
        WHEN DATEDIFF(END_DATE, START_DATE) + 1 >= 30
            THEN '장기 대여'
        ELSE '단기 대여'
    END AS RENT_TYPE
FROM CAR_RENTAL_COMPANY_RENTAL_HISTORY
WHERE START_DATE >= '2022-09-01'
  AND START_DATE < '2022-10-01'
ORDER BY HISTORY_ID DESC;
```

```
- 장기/단기 대여를 나눈 기준: 대여일이 30일 이상이면 장기이며, 30일 미만이며 단기이다


- 사용한 날짜 계산 방식: DIFF함수를 이용해서 START 날짜와 END날짜의 차이를 계산하고 대여일을 포함해야 하기 때문에 1을 더해서 사용한 날짜를 계산한다.


- CASE WHEN으로 만든 컬럼: RENT_TYPE 즉, 대여기간 칼럼을 새로 만들었다.
```

![alt text](<week5_image/스크린샷 2026-10-02 230546.png>)

## 🧩 문제 2

문제 링크: [한 해에 잡은 물고기 수 구하기](https://school.programmers.co.kr/learn/courses/30/lessons/298516)

풀이 과정: 
```SQL
SELECT
 COUNT(*) AS FISH_COUNT
FROM FISH_INFO
WHERE YEAR(TIME) = 2021
```

```
- 문제에서 요구한 연도: 2021년도에 잡은 물고기 수

- 사용한 날짜 조건: WHERE 문으로 2021년 칼럼만 가져옴 

- 집계한 대상: 2021년도에 잡은 물고기
```

![alt text](<week5_image/스크린샷 2026-10-02 231547.png>)

## 🧩 문제 3

문제 링크: [조건에 부합하는 중고거래 상태 조회하기](https://school.programmers.co.kr/learn/courses/30/lessons/164672)

풀이 과정:
```SQL
SELECT
    BOARD_ID,
    WRITER_ID,
    TITLE,
    PRICE,
    CASE
        WHEN STATUS = "SALE" THEN "판매중"
        WHEN STATUS = "RESERVED" THEN "예약중"
        WHEN STATUS = "DONE" THEN "거래완료"
    END AS STATUS
   
FROM USED_GOODS_BOARD

WHERE CREATED_DATE = "2022-10-05"

ORDER BY BOARD_ID DESC
```

```
- 날짜 조건: 2022-10-05에 해당하는 거래만 가져와야 하므로 WHERE 문으로 2022-10-05 거래만 가져온다

- CASE WHEN으로 바꾼 값: SALE => 판매중 / RESERVED => 예약중 / DONE => 거래완료로 바꾼다

- ELSE에 해당하는 경우: SALE, RESERVED, DONE 값이 아니라면 ELSE [XX] 로 그 외 결과를 만들어 줄 수 있다 (EX. ELSE 추가확인 필요)

- 정렬 기준: 게시글 ID 기준으로 내림차순으로 정렬한다
```

![alt text](<week5_image/스크린샷 2026-10-03 125920.png>)

## 🧩 문제 4

문제 링크: [자동차 평균 대여 기간 구하기](https://school.programmers.co.kr/learn/courses/30/lessons/157342)

풀이 과정:
```SQL
SELECT
    CAR_ID,
    ROUND(AVG(DATEDIFF(END_DATE, START_DATE) +1), 1) 
    AS AVERAGE_DURATION
    
FROM CAR_RENTAL_COMPANY_RENTAL_HISTORY

GROUP BY 
    CAR_ID

HAVING  
    AVG(DATEDIFF(END_DATE,START_DATE) +1) >= 7

ORDER BY AVERAGE_DURATION DESC, CAR_ID DESC
```

```
- GROUP BY 기준: CAR_ID를 기준으로 값을 묶는다

- 평균을 계산한 방식: DIFF함수를 이용해서 END_TIME과 START_TIME의 차이를 구하고 대여일도 포함해야 하므로 +1을 하고 CAR ID의 평균을 계산한다. 그리고 소수점 첫 자리에서 반올림 하라고 했으므로 ROUND 함수를 사용한다

- HAVING에 사용한 조건: CAR ID의 평균 대여기간이 7일 이상인 함수들만 나타내달라는 함수를 사용한다

- 처음 헷갈렸던 점: 
(1) ROUND 함수를 사용해야 한다는 것
(2) DIFF 함수 사용이 아직 익숙하지 않은 것
(3) HAVING 문에서 별칭을 사용하면 안되는지 여부 (AVERAGE_DURATION)
```

![alt text](<week5_image/스크린샷 2026-10-03 132539.png>)

---

# 4️⃣ 이번 주 회고

```
1. 날짜 함수 중 가장 헷갈린 함수: 문제풀이를 할 떄 아직 날짜 함수가 익숙하지 않아서 그런지 DIFF 함수를 이용하여 날짜간 차이를 구해야 된다는 발상이 잘 떠오르지 않았다.

2. CASE WHEN을 사용할 때 기억해야 할 문법: CASE WHEN THEN ELSE END
이 5가지를 3+2로기억한다. 
=
> 3: CASE WHEN THEN + 2 : ELSE END


3. 날짜/시간 데이터나 조건문을 활용해보고 싶은 분석 상황: 특정 기업의 월별 매출과 손익을 분석해 보고싶다.
```

수고하셨습니다!



