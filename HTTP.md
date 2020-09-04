```
기본 동작과 구조 소개
history, versions - 0.9 vs 1.0 vs 1.1 vs 2.0 vs 3.0
Methods - GET, HEAD, POST, PUT, DELETE, CONNECT, OPTIONS, TRACE, PATCH
HTTP vs HTTPS
HTTP Persistent Connection, Web Socket, BOSH, Server-sent events
HLS vs RTSP(RTP/RTCP)
```



# HTTP(HyperText Transfer Protocol)
```
HTTP : 텍스트 기반의 통신규약으로 인터넷에서 데이터를 주고받을 수 있는 프로토콜 
HTML 문서로 정보를 주고받음
-> Stateless Protocol

Stateless : 
이전 데이터 요청과 다음 데이터 요청이 서로 관련이 없다는 말
트렌젝션 발생 이후 연결이 종료됨

Stateless이점 : 세션같은 별도의 추가 정보를 관리하지 않아도 되고, 다수의 요청 처리 및 서버의 부하를 줄일 수 있는 성능 상의 이점이 생김

HTTP는 보통 TCP/IP통신 위에서 동작함
```
<img src="/uploads/a8ed751d384649bdab87013b0ca1de14/image.png" width="50%" height="50%" ></img>

<img src="/uploads/9faf7d02179ae0a3ae63815e91febde7/image.png" width="50%" height="50%" ></img>

# HTTP History & Versions
```
HTTP1.0 :  오버헤드가 발생 -> HTTP 1.1
1997년 RFC 2068로 HTTP 1.1가 표준이 됨
2015년 HTTP2 나옴
2018년 3 나옴
```
![image](/uploads/ced894102bb70ff747f3f9589630e3f1/image.png)
![image](/uploads/da0c909097ac1e431cf6e4a67358c58b/image.png)


# HTTP Request
```
GET 메소드는 지정된 자원의 표현을 요청
HEAD 메소드는 GET 요청과 동일하지만 응답 본문이없는 응답을 요청
POST 방식 요청은 서버의 새로운 부속물로서 요구에 포함 된 엔터티에 동의하도록 웹 리소스 URI를 식별
PUT 메소드는 동봉 된 엔티티가 제공된 URI 아래에 저장되도록 요청
DELETE 메소드는 지정된 자원을 삭제
TRACE 메소드는 수신 된 요청을 에코하여 클라이언트가 중간 서버에서 수행 한 변경 사항 또는 추가 사항을 볼 수 있음
OPTIONS 메소드는 서버가 지정된 URL에 대해 지원하는 HTTP 메소드를 리턴
CONNECT 메소드는 요청 연결을 투명한 TCP / IP 터널 로 변환하여일반적으로암호화되지 않은 HTTP 프록시를 통해 SSL 암호화 통신 (HTTPS)을 용이하게 합니다.
PATCH 메서드는 리소스에 부분 수정을 적용
```
![image](/uploads/2e5a73804a11d20168532113ba107ee2/image.png)

![image](/uploads/8d66d6283c3dd6cad7787b08c530aa6f/image.png)

# HTTP Response
![image](/uploads/066f5980ef8e6b854c2fb025d867be68/image.png)

![image](/uploads/34cb523361b8214ac831c558ac58a9b6/image.png)

[캐시쿠키](https://medium.com/@shaul1991/%EC%B4%88%EB%B3%B4%EA%B0%9C%EB%B0%9C%EC%9E%90-%EC%9D%BC%EC%A7%80-http-%ED%94%84%EB%A1%9C%ED%86%A0%EC%BD%9C%EC%9D%98-%EC%9D%B4%ED%95%B4-2-%EC%BA%90%EC%8B%9C-%EC%BF%A0%ED%82%A4-8f0bcc305597)

[HTTPS](https)