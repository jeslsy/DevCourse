## SQL을 이용한 데이터 분석

### 예제 테이블 소개
#### 1️⃣ 웹서비스 사용자/세션 정보
  - 세션 id : 세션마다 부여되는 id
  - 세션 : 사용자의 방문을 논리적 단위로 나눈 것
  - 채널 : 접점(경유지)
  - 마케팅 관련 기여도 분석 위함
  - DAU, WAU, MAU등의 일주월별 Active User 차트

<br>

#### 2️⃣ Redshift 액세스 정보

<br>

#### 3️⃣ 문법과 예시
**1. DISTINCT**

유일한 채널 이름을 알고 싶은 경우
```sql
SELECT DISTINCT channel
FROM raw_data.user_session_channel;
```

**2. CASE WHEN**
CASE
WHEN 조건1 THEN 값1 WHEN 조건2 THEN 값2 ELSE 값3
END 필드이름

**3. NULl**
- NULL이 사칙연산에 사용되면 그 결과는?
- SELECT 0 + NULL, 0 - NULL, 0 * NULL, 0/NUL
- 결과 : NULL


**4. count 함수 제대로 이해하기**
- null 무시하고 반환
- COUNT(열): 주어진 열(column)의 총 레코드 수를 반환합니다. 이 때, NULL 값을 제외한 레코드 수가 반환
- COUNT(상수): 상수(constant) 1을 인수로 사용하여 주어진 테이블의 총 레코드 수를 반환합니다. 이 때, NULL 값을 제외한 레코드 수가 반환
- COUNT(DISTINCT 열): 주어진 열(column)의 고유한 값의 수를 반환


**5. where**
- in
- like & ilike, not like & not ilike
- between
- * case when에서 사용 가능

**6. string function**
- LEFT(str, N)
- REPLACE(str, exp1, exp2)
- UPPER(str)
- LOWER(str)
- LEN(str)
- LPAD, RPAD
- SUBSTRING

**7. order by에서 null 순서**
- 오름차순이면 마지막
- 내림차순이면 제일 처음
- 바꾸고 싶으면, NULLS FIRST 혹은 ULLS LAST를 사용


**8. 타입 변환**
1. DATE Conversion:
  - 타임존 관련 변환
    - CONVERT_TIMEZONE('America/Los_Angeles', ts)
    - select pg_timezone_names();
  - DATE, TRUNCATE
  - DATE_TRUNC
    - 첫번째 인자가 어떤 값을 추출하는지 지정 (week, month, day, ...)
  - EXTRACT or DATE_PART: 날짜시간에서 특정 부분의 값을 추출가능
  - DATEDIFF
  - DATEADD
  - GETDATE
  - ...
2. TO_CHAR, TO_TIMESTAMP


**9. 타입 캐스팅**
1. 1/2의 결과는?
  - 0이 됨. 정수간의 연산은 정수가 되어야하기 때문
    - 분자나 분모 중의 하나를 float로 캐스팅해야 0.5가 나옴
    - 이는 프로그래밍 언어에서도 일반적으로 동일하게 동작함
  - 뒤에서 예제를 살펴볼 예정
2. :: 오퍼레이터를 사용 ○ category::float
  - cast 함수를 사용
3. cast(category as float)
