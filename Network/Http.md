## HTTP와 HTTPS

### HTTP 프로토콜

- 개념
  - 웹상에서 클라이언트와 서버 간에 요청/응답으로 정보를 주고 받을 수 있는 프로토콜
- 특징
  - TCP와 UDP를 사용하며 80포트 사용
  - 비연결 -> 클라이언트가 요청을 서버에 보내고 서버가 적절한 응답을 클라이언트에 보내면 연결이 끊어짐
  - 무상태 -> 연결을 끊는 순간 클라이언트와 서버의 통신은 끝나며 상태 정보를 유지하지 않음.

### HTTPS 프로토콜

- 개념
  - HTTP의 보안이 강화된 버전
- 특징
  - 443번 포트 사용
  - HTTPS는 소켓 통신에서 일반 텍스트를 이용하는 대신에, 웹 상에서 정보를 암호화하는 SSL이나 TLS 프로토콜을 통해 세션 데이터를 암호화한다.
  
### 차이점
 - HTTPS는 암호화 하는 과정이 웹 서버에 부하를 준다.
 - HTTPS는 HTTP에 비해 느리다.
 - HTPP는 비연결형으로 인터넷이 끊겼다가 다시 연결되도 페이지를 계속 볼 수 있지만 HTTPS는 소켓(데이터를 주고 받는 경로) 자체에서 인증을 하기 때문에 연결이 끊어지면 소켓도 끊어져서 다시 인증이 필요하다.
 
  