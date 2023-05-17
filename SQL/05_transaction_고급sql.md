## SQL을 이용한 데이터 분석

### 트랜잭션
#### 1️⃣ 트랜잭션이란?
- 묶어서 하나로 처리
- BEGIN, END;
- ROLLBACK

#### 2️⃣ 트랜잭션 커밋 모드 
- autocommit = True
   - 수정/삭제/추가 작업이 바로 db에 쓰여짐 = commit
 - autocommit = False
   - 작업이 commit 호출까지 커밋되지 않음

#### 3️⃣ 트랜잭션 방식
1. Google Colab
2. psycopg2


#### 4️⃣ DELETE FROM vs. TRUNCATE 차이
1. DELETE FROM
2. TRUNCATE

<br>

### 기타 고급 문법
1. union, except, intersect
2. coalesce, nullif
3. listagg
4. lag
5. window함수
  - lag, lead 함수
  - row_number over
  - sum over
  - first_value, last_value
6. JSON Parsing 함수

<br></br>

<img width="654" alt="image" src="https://github.com/jeslsy/DevCourse/assets/54103240/6eb56030-dde3-491f-9989-9f2c048c2dd1">
