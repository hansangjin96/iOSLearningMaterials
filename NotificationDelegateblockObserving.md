# Notification

[noti1](https://zeddios.tistory.com/157)

[noti2](https://zeddios.tistory.com/589)

1. 알람 권한 설정

1. 컨텐트 설정

1. 트리거 설정

1. 리퀘스트 설정

1. 애드 리퀘스트

# delegate

protocol : 무조건 있어야 하는 기능 == interface인듯?

delegate : 대리자 즉 누군가 할 일을 대신 처리

![image](/uploads/b049b66c02e29997513bb9f9b473166b/image.png)

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fk.kakaocdn.net%2Fdn%2FOpXTS%2FbtqDL4XZXiY%2FijI8KJWq1FXK5gIjQGNaP0%2Fimg.gif" width="20%" height="20%" title="mainRunLoop"></img>

# block

[블로그1](https://beankhan.tistory.com/48)

[블로그2](http://minsone.github.io/mac/ios/how-to-using-block-in-objc)


선언

<img src="/uploads/6738e733e390cc78488b54c3e54acef9/image.png" width="50%" height="50%" title="mainRunLoop"></img>

사용

<img src="/uploads/b933b960a573aeb0f471d63fcda066ec/image.png" width="50%" height="50%" title="mainRunLoop"></img>

외부 변수 변경 불가(Read Only)

<img src="/uploads/4cf7d26c4f4cfbd5745c639750172db2/image.png" width="50%" height="50%" title="mainRunLoop"></img>

<img src="/uploads/673d0e6218c05b4fe0bde0cef7df276f/image.png" width="50%" height="50%" title="mainRunLoop"></img>

<img src="/uploads/660b4e2dc5d54519b8deb0aad69959be/image.png" width="50%" height="50%" title="mainRunLoop"></img>

순환참조 발생가능 - 피하는 방법

![image](/uploads/27a41ecc8d8995a4da9772c563d8b746/image.png)


- 실행속도 최적화를 위해 기본적으로 스택에 할당

- 함수를 만들지 않고도 동적으로 코드를 동작

- 객체로써 저장이 가능

- 강한 참조를 가지므로 순환 참조로 메모리 누수 되는 부분을 방지할 것v