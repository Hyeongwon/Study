## REST

### REpresentational State Transfer

- 분산 하이퍼미디어 시스템(웹)을 위한 아키텍쳐 스타일

### Http/1.0

- Http/1.0이 출시전 이미 WWW 전송 프로토콜, 웹 확산

- 어떻게 호환성을 유지할까?

### HTTP Object Model -> REST


## API (Application Programming Interface)

- SOAP

- REST


### REST API Guidelines

- uri는 https://{serviceRoot}/{collection}/{id}

- GET, PUT, DELETE, POST, HEAD, PATCH, OPTIONS를 지원해야한다.

- API 버저닝은 Major.minor로 하고 uri에 버전 정보를 포함시킨다.

- https://docs.microsoft.com/ko-kr/azure/architecture/best-practices/api-design#introduction-to-rest


### roy fielding

- https://www.ics.uci.edu/~fielding/pubs/dissertation/fielding_dissertation.pdf

## 아키텍처 스타일

### 제약조건의 집합

- client-server

- stateless

- cache

- #uniform interface

- layered system

- code-on-demand



