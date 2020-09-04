# Key value coding(KVC)

//kvc는 objc에만 있고, kvo는 swift에도 있는듯?

[참고 블로그](http://minsone.github.io/mac/ios/ioskey-value-coding-key-value-observing)

[blog](http://funnyrella.blogspot.com/2013/10/27.html)

## 정의

앱의 정보를 의미하는 문자열을 사용하여 간접적으로 객체의 속성값을 접근하는 매커니즘

## 특징

- 키가되는 문자열은 런타임시 결정
- 소스코드가 간결해지고 유지보수가 쉬워짐
- 클래스간 의존성이 낮아짐

<img src="/uploads/292db56e41c9f5e0112e7b7684163adc/image.png" width="50%" height="50%" title="mainRunLoop"></img>

<img src="/uploads/125e49b09125e5529b2a784d20b29c0b/image.png" width="50%" height="50%" title="mainRunLoop"></img>

# Key Value Observing (KVO)

## 정의

모델 객체의 어떤 값이 변경되었을 경우 이를 UI에 반영하기 위해 컨트롤러는 모델 객체에 Observing을 도입하여 델리게이트에 특정메시지를 보내 처리할 수 있도록 함

## 특징

일대일, 일대다 관계에 대해서도 Observing 가능

모델 데이터에 반영되는 구조를 가진 앱은 코코아 바인딩을 사용하면 코드 최소화

<img src="/uploads/5afff1330fb70ad038ecad491ffeb12c/image.png" width="50%" height="50%" title="mainRunLoop"></img>

<img src="/uploads/b944a6d5e861393b1546e5499fed6aea/image.png" width="50%" height="50%" title="mainRunLoop"></img>

<img src="/uploads/8bdda57a0f76754d4140f8ba24333ff1/image.png" width="50%" height="50%" title="mainRunLoop"></img>

