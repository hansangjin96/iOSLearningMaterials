# HTTP Persistent Connection, Web Socket, BOSH, Server-sent events

![image](/uploads/0f60d3f4b79df2eab49f999563301f44/image.png)

# HTTP Persistent Connection
```
HTTP 1.0에서는 keep-alive헤더가 포함되어있지 않으면 연결이 영구적인 것으로 간주되지 않음
HTTP 1.1에서는 모든 연결이 영구적으로 간주됨

장점 : 
CPU 사용량 감소
네트워크 정체 감소
```

# Pipe Lining
```
응답을 기다리지 않고 요청을 연속적으로 보내는 기능 -> 지연 회피

구현하기 복잡하고 미미한 수준의 향상
파이프라이닝은 더 나은 알고리즘인 멀티플렉싱으로 대체되었는데, 이는 HTTP/2에서 사용
```
![image](/uploads/5490f1651428f579feedc9d96bb9404d/image.png)

![image](/uploads/9d0261e921f6fccd44393a406fe675d7/image.png)

# AJAX
```
새로운 HTML을 받아서 새 창을 띄우는 것이 아닌
XMLHttpRequest객체를 통해 XML이나 JSON의 형태로 데이터를 주고 받으며 
HTML의 부분만 바꿀 수 있음

HTTP는 웹 브라우저가 서버에 니즈 요청
AJAX는 XMLHttpRequest객체가 요청

protocol -> X
```
![image](/uploads/63bef61256f21a6a4ed833e2e17d06db/image.png)


# WebSocket
```
서버와 클라이언트 간 효율적인 양방향 통신을 실현하기 위한 구조

클라이언트의 요청이 없어도 서버에서 데이터를 받아올 수 있음

실시간 채팅, 게임 등에서 유리함
```
![image](/uploads/30594949b07bafb626ef61f366cc2841/image.png)


# Server Sent Event
```
SSE는 클라이언트가 HTTP연결을 통해 서버의 데이터를 실시간으로 지속적으로 푸쉬받는 기술 (HTML5 표준)

websocket의 경우 별도의 서버와 프로토콜로 통신하기 때문에 구현하는 비용이 많이 들고 무거움

SSE는 작동하려면 특별한 프로토콜이나 서버 구현이 필요하지 않음

웹소켓과 같은 양방향 통신이 아니므로 보낼때는 ajax를 활용

ex)주식차트, 뉴스피드, 푸시 노티피케이션

```
![image](/uploads/dac304e2ea2be4c418ab5ba98610c16b/image.png)

