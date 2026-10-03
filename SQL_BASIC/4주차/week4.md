# 📘 SQL_BASIC 4주차 정규 과제

SQL_BASIC 정규 과제는 매주 정해진 분량의 `초보자를 위한 BigQuery(SQL) 입문` 강의를 듣고, 핵심 개념을 정리한 뒤 간단한 SQL 문제를 직접 풀어보는 방식으로 진행합니다.

이번 주는 SQL 쿼리를 작성하는 흐름, 쿼리 작성 템플릿, 데이터 타입 변환, 문자열 함수를 학습합니다.

완성된 과제는 Github에 업로드하고, 링크를 스프레드시트 'SQL' 시트에 입력해 제출해주세요.

**👀 수행 인증란은 필수입니다.**

---

## 📚 SQL_BASIC_4th_TIL

### 섹션 4. SQL 쿼리 잘 작성하기, 쿼리 작성 템플릿 및 오류를 잘 디버깅하기

### 3-2. SQL 쿼리를 작성하는 흐름

### 3-3. 쿼리 작성 템플릿과 생산성 도구

### 섹션 5. 데이터 탐색 - 변환

### 4-1. INTRO

### 4-2. 데이터 타입과 데이터 변환(CAST, SAFE_CAST)

### 4-3. 문자열 함수(CONCAT, SPLIT, REPLACE, TRIM, UPPER)

---

## ✨ 선택 강의

- 3-4. 오류를 디버깅하는 방법: 오류 메시지 해석과 디버깅 흐름을 더 익히고 싶을 때 선택 수강

---

## 🏁 전체 강의 수강 계획

| 주차 | 필수 강의 범위 | 선택 강의 | 완료 여부 |
| --- | --- | --- | --- |
| 1주차 | 1-1 ~ 2-1 | 1 | ✅ |
| 2주차 | 2-2 ~ 2-3 | 2-4 | ✅ |
| 3주차 | 2-5, 2-7 ~ 2-8 | 2-6 | ✅ |
| 4주차 | 3-2 ~ 4-3 | 3-4 | ✅ |
| 5주차 | 4-4 ~ 4-6 | 4-5, 4-7 | 🍽️ |
| 6주차 | 5-2 ~ 5-5 | 5-6 | 🍽️ |
| 7주차 | 필수 강의 없음 | 6-2, 6-3, 6-4, 6-5 | 🍽️ |

---

<br>

<!-- 여기까진 그대로 둬 주세요-->

---

# 1️⃣ 개념 정리

아래 키워드 중 중요하다고 생각한 개념을 2개 이상 골라 짧게 정리해주세요. 3개보다 더 많이 정리하고 싶다면 자유롭게 항목을 추가해도 좋습니다.

이번 주 키워드:
- 쿼리 작성 순서
- 쿼리 작성 템플릿
- 데이터 타입
- CAST
- SAFE_CAST
- CONCAT
- REPLACE
- TRIM

## 01.

```
개념 이름:CAST
개념 설명: 자료 타입을 변경하는 함수이다 예를들어 문자열 "1 2 3" 을 정수형 " 1 2 3 "으로 바꿀 수 있다.
예시 쿼리:
SELECT
    CAST(1 AS STRING) 
=> 숫자 1을 문자 1로 변경

SELECT 
    CAST("김기열" AS INT64)
=> 김기열은 숫자로 변경하려고 해도 불가능

```

## 02.

```
개념 이름:SAFE_CAST
개념 설명:SAFE_ 가 붙은 함수는 변환이 실패할 경우 NULL을 반환한다. 예를 들어 숫자로 바꿀 수 없는 문자열을 정수로 변환하려고 하면 오류가 발생한다.
예시 쿼리:
SELECT
    SAFE_CAST(""김기열" AS INT64)
=> 변환 실패로 NULL값 반환
```

## (선택) 03.

```
개념 이름: ctrl + / 
개념 설명: 주석처리
헷갈린 점:
```

---

# 2️⃣ 수행 인증란

![alt text](week4_image/스크린샷(769).png) ![alt text](week4_image/스크린샷(770).png) ![alt text](week4_image/스크린샷(778).png) ![alt text](week4_image/스크린샷(779).png) ![alt text](week4_image/스크린샷(780).png) ![alt text](week4_image/스크린샷(788).png) ![alt text](week4_image/스크린샷(789).png) ![alt text](week4_image/스크린샷(790).png) ![alt text](week4_image/스크린샷(791).png) ![alt text](week4_image/스크린샷(792).png) ![alt text](week4_image/스크린샷(793).png) ![alt text](week4_image/스크린샷(794).png) ![alt text](week4_image/스크린샷(811).png) ![alt text](week4_image/스크린샷(813).png) ![alt text](week4_image/스크린샷(814).png) ![alt text](week4_image/스크린샷(815).png) ![alt text](week4_image/스크린샷(816).png) ![alt text](week4_image/스크린샷(817).png)

---

# 3️⃣ 확인 문제

프로그래머스는 로그인이 필요하므로, 로그인 후 문제 풀이를 진행해주세요.

## 🧩 문제 1

문제 링크: [특정 옵션이 포함된 자동차 리스트 구하기](https://school.programmers.co.kr/learn/courses/30/lessons/157343)

풀이 과정:
SELECT *
FROM CAR_RENTAL_COMPANY_CAR
WHERE OPTIONS LIKE '%네비게이션%'
ORDER BY CAR_ID DESC;
```
- 찾으려는 문자열 조건: CAR_RENTAL_COMPANY_CAR 테이블에서 '네비게이션' 옵션이 포함된 자동차 리스트를 출력하는 SQL문을 작성해주세요. 결과는 자동차 ID를 기준으로 내림차순 정렬해주세요.

- 사용한 문자열 조건 문법: LIKE '%네비게이션%'으로 앞뒤에 다른 문자가 있어도 검색

- 정렬 기준:CAR ID 기준으로 내림차순 정렬
```

![alt text](<week4_image/스크린샷 2026-09-28 101633.png>)

## 🧩 문제 2

문제 링크: [강원도에 위치한 생산공장 목록 출력하기](https://school.programmers.co.kr/learn/courses/30/lessons/131112)

풀이 과정:
SELECT FACTORY_ID, FACTORY_NAME, ADDRESS
FROM FOOD_FACTORY
WHERE ADDRESS LIKE '강원도%'
ORDER BY FACTORY_ID ASC;

```
- 문제에서 요구한 조건: FOOD_FACTORY 테이블에서 강원도에 위치한 식품공장의 공장 ID, 공장 이름, 주소를 조회하는 SQL문을 작성해주세요. 이때 결과는 공장 ID를 기준으로 오름차순 정렬해주세요.


- WHERE 절로 옮긴 방식: WHERE ADDRESS LIKE '강원도%'로 주소가 '강원도'로 시작하는 행 선택
```

- 정렬 기준: 공장 ID를 오름차순으로 정렬

![alt text](<week4_image/스크린샷 2026-09-28 101935.png>)

## 🧩 문제 3

문제 링크: [이름에 el이 들어가는 동물 찾기](https://school.programmers.co.kr/learn/courses/30/lessons/59047)

풀이 과정:
SELECT ANIMAL_ID, NAME
FROM ANIMAL_INS
WHERE ANIMAL_TYPE = 'Dog'
  AND LOWER(NAME) LIKE '%el%'
ORDER BY NAME ASC, ANIMAL_ID ASC;

```
- 찾으려는 문자열 패턴: LIKE '%el%'로 이름에 'el'이 포함된 개 검색
- 대소문자를 처리한 방식: LOWER(NAME)으로 이름을 소문자로 변환하여 비교
- 정렬 기준: 결과는 이름순으로 조회 만약 이름이 같은 경우 아이디 기준으롲 ㅗ회
```

![alt text](<week4_image/스크린샷 2026-09-28 102250.png>)

## 🧩 문제 4

문제 링크: [카테고리 별 상품 개수 구하기](https://school.programmers.co.kr/learn/courses/30/lessons/131529)

풀이 과정:
SELECT LEFT(PRODUCT_CODE, 2) AS CATEGORY,
       COUNT(*) AS PRODUCTS
FROM PRODUCT
GROUP BY LEFT(PRODUCT_CODE, 2)
ORDER BY CATEGORY ASC;

```
- 추출한 문자열 범위:LEFT(PRODUCT_CODE, 2)로 상품코드의 앞 2자리 추출
- 그룹화 기준:앞 2자리가 같은 상품끼리 GROUP BY로 묶고 COUNT로 개수 계산
- 정렬 기준: 상품 카테고리 코드를 기준으로 오름차순 정렬
```

![alt text](<week4_image/스크린샷 2026-09-28 102634.png>)

---

# 4️⃣ 이번 주 회고

```sql
1. 쿼리 작성 흐름을 잡을 때 도움이 된 방법:  
#쿼리를작성하는목표,확인할지표: 
#쿼리계산방법:
#데이터의기간: 
#사용할테이블: 
#JoinKEY:
#데이터특징: 
SELECT  

FROM 
WHERE

이렇게 espanso를 이용해서 흐름을 생각하고 쿼리 작성 흐름을 잡으니까 쿼리 흐름을 잡기가 더 수월했다

2. WHERE 열이름 LIKE '%XX%'

=> 해당 열의 값에 문자열 XX가 포함된 행을 찾는다

여기서 %는 문자가 0개 이상 있는 경우를 뜻해요. 공백뿐 아니라 글자, 숫자 등도 포함합니다.
- 'XX' → 일치
- 'abcXX123' → 일치
- ' XX ' → 일치
- 'X X' → 불일치 (XX가 붙어 있지 않음)

```

수고하셨습니다!

