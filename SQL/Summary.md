## SQL 수업 요약
> 키워드 위주로 정리, 필요하면 원본 ppt 확인 바람

### SQL과 DB 소개
1️⃣ 대표적 관계형 데이터베이스
  - 프로덕션 데이터베이스 
    - Star schema
    - 2단계로 구성
  - 데이터 웨어하우스
    - Denormalized schema

<br>

2️⃣ SQL 구성
   - DDL(테이블 구조 정의)
   - DML(질의 - 추가/삭제/갱신)

<br>

3️⃣ 빅데이터 세상에서 SQL
  - 대용량 데이터 웨어하우스는 sql기반
  - Spark(SparkSQL), Hadoop(Hive)

<br>

4️⃣ SQL 단점
  - 구조화된 데이터에 최적화
  - 비구조화엔 제약
  - RDBMS는 대부분 플랫 구조 지원(구글 빅쿼리는 nested structure 지원)
  - 이러한 이유로 Spark, Hadoop 같은 분산 컴퓨팅 환경 필요

<br>

5️⃣ 데이터 웨어하우스
  - 내부 직원 위한 데이터베이스
  - ETL(데이터 파이프라인) : 외부 데이터 읽고 넣어주는 코드


![image](https://github.com/jeslsy/DevCourse/assets/54103240/c45430c2-398a-4f41-ad17-c83557249d31)



### Cloud와 AWS
1️⃣ 클라우드
2️⃣ AWS
  - ec2
  - s3 : 대용량 클라우드 스토리지 서비스, 계층적 구조
  - Database Services 
    - RDS (Relational Database Service)
      – MySQL, PostgreSQL, Aurora
      – Oracle, MS SQL Server
    - DynamoDB
    - Redshift
    - ElastiCache
    - Neptune (Graph database)
    - ElasticSearch
    - MongoDB
  -  AI & ML Services
    - SageMaker : Deep Learning and Machine Learning end-to-end framework
    - Lex : Conversational Interface (Chatbot service)
    - Polly : Text to Speech Engine
    - Rekognition : Image Recognition Service
 
 
