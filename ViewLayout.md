# Viewlayout

[참고 블로그](https://zeddios.tistory.com/359)

## setNeedsDisplay : View 를 다시 그려야함을 시스템에 알리는 것은 개발자 책임 - 이 메소드는 다음 드로잉 사이클 동안 view를 업데이트 해야함을 시스템에 알림. 비동기

## setNeedsLayout : receiver(수신자)의 현재 레이아웃을 무효화하고, 다음 업데이트 주기 동안 레이아웃 업데이트를 트리거함. 비동기

## View의 레이아웃을 즉시 업데이트하려면, layoutIfNeeded()메소드를 호출합니다. 동기 호출

## displayIfNeeded : 현재 업데이트가 필요한것으로 표시된 경우, 레이어의 업데이트 프로세스를 시작합니다.

### "레이어를 업데이트하는 가장 좋은 방법은 setNeedsDisplay()를 호출하고, 다음주기 동안 시스템이 레이어를 업데이트 하도록 하는 것입니다."

### setNeedsLayout()와 layoutIfNeeded()의 차이점

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=http%3A%2F%2Fcfile2.uf.tistory.com%2Fimage%2F992C08485A44B5652DD127)

