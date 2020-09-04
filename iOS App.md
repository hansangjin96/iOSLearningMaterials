# 앱의 실행과정

1. main 함수가 실행
1. main 함수는 UIApplicationMain함수를 호출
1. UIApplicationMain함수는 앱의 본체에 해당하는 객체인 UIApplication 객체를 생성한다.
1. nib파일을 사용하는 경우나, Info.plist 파일을 읽어들여 파일에 기록된 정보를 참고하여 그외에 필요한 데이터를 로드한다.
1. 앱 델리게이트 객체를 만들고 앱 객체와 연결하고 런루프를 만드는 등 실행에 필요한 준비를 한다.
1. 실행 완료를 앞두고 앱 객체가 앱 델리게이트에게 application:didFinishLaunchingWithOptions: 메시지를 보낸다.

# iosLifeCycle
<img src="/uploads/cee170f4b807d8678f897b8f8d704327/appState.png" width="40%" height="30%" title="iosLifeCycle"></img>

# mainRunLoop
<img src="/uploads/3e9f89a9a186fde650612b926636f638/iosLifeCycle.png" width="40%" height="30%" title="mainRunLoop"></img>

# appState
<img src="/uploads/3585517ea1429dab7eea5afe0f9fa06f/mainRunLoop.png" width="40%" height="30%" title="appState"></img>

# appForeground
<img src="/uploads/89cafb9eee0b38e1afee341aad4d3d19/image.png" width="40%" height="30%" title="appForeground"></img>

# appBackground
<img src="/uploads/9937b99f4e062d570b7188f150d14b8a/image.png" width="40%" height="30%" title="appBackground"></img>

# Summary
<img src="/uploads/635042aa95c8aad4e43b84855a94f85b/_"  title="appBackground"></img>
