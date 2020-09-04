# API(Application Program Interface)란?
```
API는 어떤 서버의 특정한 부분에 접속해서 그 안에 있는 데이터와 서비스를 이용할 수 있게 해주는 소프트웨어 도구

```

# REST API
```
REST(Representational State Transfer)는 네트워크를 통해서 컴퓨터들끼리 통신할 수 있게 해주는 아키텍처 스타일

REST API는 인터넷 식별자(URI)와 HTTP 프로토콜을 기반으로 합니다. 

해당 API를 사용하는 애플리케이션들이 동일한 경로를 통해서 접속해야 하고, 그 방식이 단순하게 됩니다.

REST는 웹에 최적화되어 있고, 데이터 포맷이 JSON이기 때문에 브라우저들 간에 호환성이 좋습니다. 
또한, 그 성능과 확장성이 뛰어난 것으로도 알려져 있죠. 

하지만 해결할 수 없는 문제들이 나와서 그래프 QL같은 언어가 생김
```

# REST 6 가지 원칙
```
- Uniform Interface
- Stateless
- Caching
- Client-Server
- Hierarchical system
- Code on demand
```

# RESTful 하게 API 를 디자인 한다는 것은 무엇을 의미하는가.(요약)
```
1. 리소스 와 행위 를 명시적이고 직관적으로 분리한다.
- 리소스는 URI로 표현되는데 리소스가 가리키는 것은 명사로 표현되어야 한다.
- 행위는 HTTP Method로 표현하고, GET(조회), POST(생성), PUT(기존 entity 전체 수정), PATCH(기존 entity 일부 수정), DELETE(삭제)을 분명한 목적으로 사용한다.

2. Message 는 Header 와 Body 를 명확하게 분리해서 사용한다.
- Entity 에 대한 내용은 body 에 담는다.
- 애플리케이션 서버가 행동할 판단의 근거가 되는 컨트롤 정보인 API 버전 정보, 응답받고자 하는 MIME 타입 등은 header 에 담는다.
- header 와 body 는 http header 와 http body 로 나눌 수도 있고, http body 에 들어가는 json 구조로 분리할 수도 있다.

3. API 버전을 관리한다.
- 환경은 항상 변하기 때문에 API 의 signature 가 변경될 수도 있음에 유의하자.
- 특정 API 를 변경할 때는 반드시 하위호환성을 보장해야 한다.

4. 서버와 클라이언트가 같은 방식을 사용해서 요청하도록 한다.
- 브라우저는 form-data 형식의 submit 으로 보내고 서버에서는 json 형태로 보내는 식의 분리보다는 json 으로 보내든, 둘 다 form-data 형식으로 보내든 하나로 통일한다.
- 다른 말로 표현하자면 URI 가 플랫폼 중립적이어야 한다.
```

# 어떠한 장점이 존재하는가?
```
1. Open API 를 제공하기 쉽다
2. 멀티플랫폼 지원 및 연동이 용이하다.
3. 원하는 타입으로 데이터를 주고 받을 수 있다.
4. 기존 웹 인프라(HTTP)를 그대로 사용할 수 있다.
```

# 단점은 뭐가 있을까?
```
1. 사용할 수 있는 메소드가 4 가지 밖에 없다.
2. 분산환경에는 부적합하다.
3. HTTP 통신 모델에 대해서만 지원한다.
```

# SOAP
```
SOAP(Simple Object Access Protocol)은 일반적으로 널리 알려진 HTTP, HTTPS, SMTP 등을 통해 
XML 기반의 메시지를 컴퓨터 네트워크 상에서 교환하는 프로토콜이다.

SOAP(Simple Object Access Protocol)는 그 자체로 프로토콜이며, 보안이나 메시지 전송 등에 있어서 
REST보다 더 많은 표준들이 정해져있기 때문에 조금 더 복잡합니다. 

은행용 모바일 앱처럼 보안 수준이 높아야 하거나, 신뢰할 수 있는 메시징 앱, 또는 ACID를 준수해야 하는 경우라면 SOAP 방식이 더욱 선호됩니다.

SOAP 표준에는 성공/반복 실행 로직이 규정되어 있기 때문에, SOAP API를 통해서 통신을 할 때 처음부터 끝까지 신뢰성을 제공합니다.

ACID를 준수하기 때문에 데이터의 변형을 줄여주고, 데이터베이스와의 상호작용에 대해서 사전에 정확하게 정하기 때문에 데이터의 무결성을 지켜주지요.
```

# SOAP 구성요소
```
SOAP 메시지는 다음 요소를 포함하는 일반적인 XML 도큐먼트.
SOAP(SOAP Envelope), SOAP Header, SOAP Body, SOAP Encoding Rule, SOAP RPC Representation의 5가지 요소로 구성
```

# SOAP 장점
```
1. SOAP은 기본적으로 HTTP 기반 위에서 동작하기 때문에, HTTP와 같이 프록시와 방화벽에 구애받지 않고 쉽게 통신이 가능하다. 
2. 플랫폼 및 프로그래밍 언어에 독립적이다. 
3. 간단하고 확장 가능하다. 
4. 멀티파트 MIME 구조를 사용하여 첨부를 통합하는 SOAP XML 메시지를 지원한다.
```

# SOAP 단점
```
 XML 포맷의 형태로 보내기 때문에 다른 기술과 비교해서 상대적으로 느리다고 하나, 
네트워크 속도의 발전과 성능 최적화 기술의 발전으로 많은 부분이 해결되고 있다고 한다.
```

# SOAP vs REST
```
SOAP는 프로토콜이고, REST는 아키텍처 스타일이다.

REST는 HTTP와 JSON을 사용하기 때문에 페이로드의 무게를 가볍게 할 수 있습니다. 하지만 SOAP에서는 XML에만 의존합니다.

SOAP는 WS-Security를 지원하는데, WS-Security는 전송 레벨에서 아주 뛰어나며 SSL보다도 조금 더 복잡하기 때문에 
기업용 보안 도구에 통합하는데 보다 이상적입니다. 

SOAP는 서버와 매우 긴밀하게 연결되기 때문에 그 통신 방식이 매우 엄격하며, 그래서 수정이나 업데이트를 하는 것이 보다 더 어렵습니다. 

REST 방식의 API에서는 클라이언트에서 해당 API가 필요하지 않지만, 
SOAP 방식의 API에서는 상호작용을 시작할 때조차도 클라이언트에서 API에 관한 모든 정보들을 필요로 합니다.
```

![image](/uploads/4c10e5e687672189a5cc37b778d68d66/image.png)


![image](/uploads/8c6ba7ae6c92da24ae180fd3dab5b525/image.png)

