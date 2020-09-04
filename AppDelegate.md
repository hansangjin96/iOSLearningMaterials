# App Delegate & Scene Delegate

[참고 블로그](https://velog.io/@dev-lena/iOS-AppDelegate%EC%99%80-SceneDelegate)

[자세한 설명 (Zedd)](https://zeddios.tistory.com/811)

![image](/uploads/a9dbe301ca0298d633af5afcf69c0dc0/image.png)

## window 의 개념이 scene 으로 대체됨

## AppDelegate 의 역할 중 UI의 상태에 대한 부분을 SceneDelegate가 처리

![image](/uploads/4c928b5d6a5605d5f6c546050b087c82/image.png)

## AppDelegate 에 Session LifeCycle에 대한 역할 추가

![image](/uploads/bb6488a9741c027dffd69383e0c83ecd/image.png)

## AppDelegate 에서는 Scene Session을 통해 Scene의 정보를 업데이트 받음

![image](/uploads/bb6af60405ef227c7288ac7b979d88dd/image.png)

## AppDelegate 가 하는 일

![image](/uploads/235b4777b26860799d74edf5be6d9a4d/image.png)

## Deployment Target이 13미만인 상황에서

![image](/uploads/1289e8ac52a121f0b9c21f5fa7e6b9d8/image.png)



# Session Lifecycle

1. 앱을 누르면 [ didFinishLaunchingWithOptions ] 호출

2. 시스템에서 Scene Session을 만듬

3. "실제 UI Scene"이 만들어지기 전 [ configurationForSession ]을 요청해야함  
(이 configuration은 scene delegate, 스토리보드 및 scene을 생성할 scene subclass를 지정)

4. 만들어진 Scene Session 에 Scene Delegate 연결 [ willConnectToSession ]

5. Home Button을 누르면 [ willResignActive ], [ didEnterBackground ] 메소드 호출

6. 시간이 지나면 리소스 회수를 위해 scene을 메모리에서 해제할 수 있음 [ sceneDidDisconnect ]

7. 이렇게 해제된 세션은 scene-based state restoration API를 통해 복구 가능 [ stateRestorationActivity]

8. Scene Sync 를 하려면 event를 받은 VC 가 model 을 update하고, model controller 가 VC들을 업데이트 하는구조로 해야함 ![image](/uploads/4475f31a59c47d78b66b0139136998ed/image.png)

9. 사용자가 앱을 명시적으로 종료 [ didDiscardSceneSession ]
