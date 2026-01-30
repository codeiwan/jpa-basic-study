### H2 라이브러리 직접 실행

프로젝트의 Maven 라이브러리에 이미 다운로드된 H2 jar 파일을 이용해 웹 콘솔을 띄우기

```bash
java -cp ~/.m2/repository/com/h2database/h2/2.4.240/h2-2.4.240.jar org.h2.tools.Server -tcp -tcpPort 9092 -web -webPort 8082
```

이후 http://localhost:8082 로 접속 후 테스트

- 저장한 설정: Generic H2 (Embedded) 
- 드라이버 클래스: org.h2.Driver
- JDBC URL: jdbc:h2:tcp://localhost/./data/test
- 사용자명: sa

## DB 활용

### Member 테이블 만들기

```sql
CREATE TABLE member (
    id BIGINT NOT NULL,
    name VARCHAR(255),
    PRIMARY KEY (id)
);
```
