# UI Event handling/UIGestureRecognizer

[UIResponder](https://zeddios.tistory.com/538)

[Hit test 링크](http://monibu1548.github.io/2019/02/09/hittest/)

[Gesture 링크](https://zeddios.tistory.com/112)

[Event Handling](https://medium.com/@audrl1010/event-handling-guide-for-ios-68a1e62c15ff)

# UI Responder

UIKit 앱 이벤트 처리 백본(backbone)을 구성

이벤트가 발생하면, UIKit은 이를 처리할 수 있도록 앱의 리스폰더 객체에 전달

UIKit 리스폰더는 처리되지 않은 이벤트를 앱의 다른 부분으로 전달하는 작업을 관리

주어진 리스폰더가 이벤트를 처리하지않으면, 리스폰더 체인의 다음 이벤트로 해당 이벤트를 전달

![image](/uploads/f9ba34fdcbd5c41e08cb157c0fcaf3ef/image.png)

![image](/uploads/d0e35b5f76af63c1208cf2d1b05adcf8/image.png)


# UI Event handling

UIEvent는 하나의 touch event, shake-motion event, remote-control event를 캡슐화 합니다.

![image](/uploads/51f33d6cdae4dbca489adc400f8d28d3/image.png)

![image](/uploads/4e55aafc7bbaeae412c66900e15345d5/image.png)


# 제스쳐 구현에는 두 가지 방법이 있음

1. touchesBegan/Ended/Moved/Cancelled

2. Tap Gesture Recognizer을 포함한 다양한 제스쳐


# Configuring the Event-Related Behavior

## isUserInteractionEnabled

false일 경우 touch, press, keyboard 그리고 focus event는 event queue에서 무시되고 삭제

default value는 true

## isMultipleTouchEnabled

true로 set하면, view는 multi-touch sequence와 관련된 모든 touch를 받고 view의 bounds에서 시작

false로 set하면, view는 오직 multi-touch sequence안에 있는 first touch event만 받음

default value는 false

## isExclusiveTouch

isExclusiveTouch는 리시버가 touch event를 exclusively하게 다룰지를 나타내는 Boolean 값

true로 set하면, 리시버가 동일한 window의 다른 view에 대한 touch event전달을 차단

프로퍼티의 기본값은 false