[OSI](https://medium.com/harrythegreat/osi%EA%B3%84%EC%B8%B5-tcp-ip-%EB%AA%A8%EB%8D%B8-%EC%89%BD%EA%B2%8C-%EC%95%8C%EC%95%84%EB%B3%B4%EA%B8%B0-f308b1115359)

# OSI model
```
OSI model : 컴퓨터와 컴퓨터 사이에 데이터 전송을 분류한 모델

OSI model에서는 Application Layer을 사용자 인터페이스로 정의함
사람이 인식하고 Application Layer아래 Presentation Layer과 상호작용 할 수 있는 데이터와 그림을 보여주기 때문
```
![image](/uploads/6115a8f2c3f8a977010d5348f9b5d2be/image.png)

![image](/uploads/97dddf13555260ee65efd0e4c0c3d829/image.png)


# Application Layer
```
인터넷 프로토콜(IP) 컴퓨터 네트워크를 통하는 프로세스 간 통신 접속을 위해 설계되어
통신 프로토콜과 방식을 위해 보유된 추상 계층

http는 전송프로토콜을 의미
```

[TCP/IP](https://medium.com/@chrisjune_13837/web-http-tcp-ip-%EB%A9%94%EC%8B%9C%EC%A7%80%EB%9E%80-4b2721fe296f)
# TCP/IP(Transmission Control Protocol/Internet Protocol)
```
TCP :  데이터 전달을 관리하는 규칙

데이터를 작게 나누어서 한쪽에서 다른쪽으로 옮기고, 이를 다시 조립하여 원래의 데이터로 만드는 규칙

잘게 나눈 데이터 단위를 패킷이라고 합니다.

TCP는 패킷을 조립하고, 손실된 패킷을 확인하고, 재전송하도록 요청하는 기능을 합니다.
```
```
IP는 인터넷상의 주소 규칙

인터넷상에 연결된 모든 컴퓨터의 위치에도 규칙이 필요

이전에는 2⁸*4자리의 주소인 IPv4를 사용하였지만 주소가 고갈이 되고 있어서 16⁴*8자리인 IPv6로 전환하고 되고 있습니다.
```
![image](/uploads/d7bfc75dc9ae6d5496e4a6f27dbc5c4e/image.png)

# DNS
```
DNS 또는 Domain Name System은 사람이 읽을 수 있는 도메인 이름(예: www.amazon.com)을 
머신이 읽을 수 있는 IP 주소(예: 192.0.2.44)로 변환합니다.
```
![image](/uploads/3353ebc05e5d02a75e84e15e05e79819/image.png)

# IP, Domain, URL, URI
```
ip : 인터넷에 연결되어있는 장치를 식별할 수 있는 주소
115.68.24.88

Domain = 컴퓨터의 이름 + 최상위 도메인 (?)
naver.com

URL(Uniform Resource Locator) = Domain + 경로
http://endic.naver.com/endic.nhn

URI(Uniform resource Identifier) = 자원을 식별하기 위한 문자열의 구성
http://endic.naver.com/endic.nhn?docid=1232950

URI vs URL
URI가 상위개념으로 URL을 포함함

https://example.com --> URI이면서 URL
https://example.com/123 --> 123 이라는 Identifier가 필요하므로 URI but not URL
```
![image](/uploads/e42f017c5e8c018a32d4115d5a0d0cb7/image.png)

![image](/uploads/7db0342d896669d7973319ef14b885b3/image.png)


# Protocols

![image](/uploads/6e14de98b811a8a44fcc75c4bb083ed4/image.png)
