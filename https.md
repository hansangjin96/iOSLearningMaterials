# HTTPS
```
보안이 강화된 버전
SSL 프로토콜을 통해 세션 데이터를 암호화 한다.
사용자 데이터의 무결성과 기밀성을 유지할 수 있게 해주는 인터넷 통신 프로토콜
```
![image](/uploads/a9098858144ba7e3b2879941031a3a64/image.png)

# HTTP vs HTTPS
```
HTTPS URL 은 "https : //"로 시작하고 기본적으로 포트 443을 사용 하는 반면, 
HTTP URL은 "http : //"로 시작하고 기본적으로 포트 80을 사용합니다.

HTTP는 암호화되지 않았기 때문에 MITM (Man-in-the-Middle) 및 도청 공격에 취약 하여 
공격자가 웹 사이트 계정 및 중요한 정보에 액세스하고 웹 페이지를 수정하여 맬웨어 또는 광고 를 주입 할 수 있습니다 .
```
![image](/uploads/1c1ca1ed5d2246530f761082c9e2071a/image.png)



# SSL 
```
클라이언트가 접속한 서버가 신뢰 할 수 있는 서버임을 보장
SSL 통신에 사용할 공개키를 클라이언트에게 제공
CA(Certificate Authority)로부터 신뢰할 수 있는 사이트라는 것을 인증받으면 공개키를 얻을 수 있고, 공개키를 통해 데이터를 암호화, 복호화
```
![image](/uploads/d51b184672e9d3780d1d82c10b1a393b/image.png)


<img src="/uploads/c2b86808aa9d2ccfd8d24d69def289c4/image.png" width="50%" height="50%" ></img>

[HTTP Persistent Connection, Web Socket, BOSH, Server-sent events](HTTP3)