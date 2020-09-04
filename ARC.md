# ARC (Automatic Reference Counting)

[blog](https://jinshine.github.io/2018/07/08/iOS/ARC(Automatic%20Reference%20Counting)/)

Cocoa(어플리케이션 개발환경)에서 사용하는 메모리 관리 모델에는 MRC와 ARC가 있다.

Stack에 저장된 데이터는 자동으로 제거되지만,

Heap에 저장된 데이터는 직접 제거해야하고 메모리 관리 모델이 이 데이터를 관리한다.

Reference Type인 Class와 Closure이 힙 메모리에 된다.
![image](/uploads/eb5b90168256295aee09115beb60e7ae/image.png)

MRC는 Manual Reference Counting 의 약자로 개발자가 직접 메모리 관리하는 코드를 작성해야 합니다. 인스턴스의 기본 메소드인 retain 과 release 를 호출하면서 말이죠. 이렇게 되면 코드양이 많아지고 메모리 오류 가능성이 높아지게 됩니다. 즉, 프로그램의 안정성이 낮아지게 됩니다.

ARC는 Automatic Reference Counting의 약자입니다. 컴파일러가 알아서 메모리 관리 코드를 삽입해 줍니다. 코드의 양은 적어지고 프로그램의 안정성을 높일 수 있게되었습니다. ARC가 등장하면서 부터 거의 모든 프로젝트는 ARC를 사용한다고 봐도 무방합니다.

![image](/uploads/88d0c2b4b4cf574c1176bbfb0ab4269c/image.png)

# 참조타입
![image](/uploads/741ea53f15ff48861ca5cf9059a748f6/image.png)

# 예제코드

## Strong Reference 가 연결될때마다 카운트 +1, nil 일 경우 -1
//[link]Appdelegate.m 14번째 줄 - 나중에 다시 추가