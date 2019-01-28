### TCP
- 1대1 연결지향, 신뢰할 수 있는 통신 서비스를 제공한다.
- 연결확립과 보내진 패킷의 확인, 순서화, 전달 중 손상된 패킷을 복구하는 책임을 지는 역할이다.

### UDP
- 1대다 연결지향, 신뢰성 보장 X

### Http
- TCP + UDP를 사용하며, 80번 포트 사용

### StateLess
- Client의 이전 상태를 기록하지 않는 접속

### ConnectionLess 
- 클라이언트가 서버에 요청을 하고 서버가 클라이언트에게 응답을 보내면 접속을 끊는다


## 쿠키

### 세션 쿠키 (session Cookie)
- 통신이 연결된 상태에서만 사용하는 점이 특징

### 지속 쿠키 (pesistent Cookie)
-  하드디스크에 직접 저장