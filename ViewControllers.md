# Viewcontrollers

[developer.apple](https://developer.apple.com/library/archive/featuredarticles/ViewControllerPGforiPhoneOS/index.html)

### 모든 앱은 1개 이상의 뷰콘을 가지고 있고, 대부분 여러개를 가짐

### 뷰 콘트롤러는 1개의 루트 뷰를 가지고 그 아래에 여러개의 서브 뷰를 가짐

## View Management

![image](/uploads/06b78604655cc469a1215124fd029556/image.png)

### Content view controllers manage a discrete piece of your app’s content and are the main type of view controller that you create.

### Container view controllers collect information from other view controllers (known as child view controllers) and present it in a way that facilitates navigation or presents the content of those view controllers differently.

### 컨텐트 뷰는 모든 뷰를 자기가 관리하지만, 컨테이너 뷰는 자기 자신과 루트 뷰만 관리함

## Data Marshaling

![image](/uploads/717f7a87b4a4a68b97f12ff2a6d6c2cd/image.png)

### 컨텐트 뷰콘은 데이터와 뷰 사이를 매니지 하며 clean seperation of responsibility를 유지해야함

### UIDocument 객체가 데이터를 관리하는 방법 중 하나

## User Interactions

### 터치 이벤트 핸들링을 뷰콘이 직접 처리하지 않고 delegate 를 통해 처리

## Resource Management

### didReceiveMemoryWarning 메소드 가 더이상 필요하지 않은 객체의 참조를 지움

## Adaptivity

![image](/uploads/0590df06fb074c93f30213ea8ebc718c/image.png)

### 여러가지 디바이스에 맞게 어댑트 할 수 있어야함

### 따라서 오토 레이아웃과 UIKit를 써서 화면 전환을 처리함