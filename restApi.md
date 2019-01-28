## REST

### REpresentational State Transfer

- 분산 하이퍼미디어 시스템(웹)을 위한 아키텍쳐 스타일

- 자원(RESOURCE) - URI
- 행위(Verb) - HTTP METHOD
- 표현(Representations)

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

- **uniform interface**

- layered system

- code-on-demand (optional)


### uniform interface

- uri가 resource로 식별 가능

- Http message에 표현을 담아서 전송해야한다.

- **메세지는 스스로를 설명해야한다.**


```
GET / HTTP/1.1

GET / HTTP/1.1
HOST: www.kickgoing.io
```

```
HTTP/1.1 200 OK
[ { "op": "remove", "path": "/a/b/c"} ]


HTTP/1.1 200 OK
Content-Type: application/json
[ { "op": "remove", "path": "/a/b/c"} ]


HTTP/1.1 200 OK
Content-Type: application/json-patch+json
[ { "op": "remove", "path": "/a/b/c"} ]


```

- **HATEOAS** (Hypermedia as the engine of application state)
어플리케이션의 상태는 Hyperlink를 이용해 전이되어야한다.'


### 독립적 진화

- 서버와 클라이언트가 각각 독립적으로 진화한다.

- 웹

- 모바일

```
GET /todos HTTP/1.1
Host: kickgoing.io

Http/1.1 200OK
Content-Type: application/

[
  {'id': 1, 'title': 'ABA',
  {"id": 2, 'title': 'BBB'.
]
```

IANA에 미디어 타입 등록
https://www.iana.org/assignments/media-types/media-types.xhtml

```
GET /todos HTTP/1.1
Host: kickgoing.io

Http/1.1 200OK
Content-Type: application/vnd.todos+json
Lick: <https://kickgoing.io/docs/totods>; rel="profile">

[
  {'id': 1, 'title': 'ABA',
  {"id": 2, 'title': 'BBB'.
]
```
