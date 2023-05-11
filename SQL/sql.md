
## SQL을 이용한 데이터 분석


### CTAS
- **SELECT**를 가지고 테이블 생성
- 간단하게 새로운 테이블을 만드는 방법
- 자주 조인하는 테이블들이 있다면 이를 CTAS를 사용해서 조인해두면 편리해짐

```sql
DROP TABLE IF EXISTS adhoc.keeyong_session_summary;
CREATE TABLE adhoc.keeyong_session_summary AS
SELECT B.*, A.ts FROM raw_data.session_timestamp A
JOIN raw_data.user_session_channel B ON A.sessionid = B.sessionid;
```
