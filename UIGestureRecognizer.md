# Ui Gesture Recognizer

# Pinch

![image](/uploads/333cea2fdf8840053e85ab9455699b0e/image.png)

내용을 확대 또는 축소

Pinch Gesture Recognizer는 화면은 터치하는 두 손가락 사이의 거리 변화를 보고(report)

손가락 사이의 거리가 변경될 때마다 액션메소드가 호출

# Rotation

![image](/uploads/f9371298a5a2670e8c7ae57822fa3dbf/image.png)

화면에서 두 손가락의 상대적인 회전을 측정하고 , 해당 동작을 사용하여 컨텐츠를 회전

Gesture Recognizer는 회전값을 라디안 단위로 보고

# Swipe

화면에서 수평 또는 수직 swipe동작을 감지하고, 이를 사용하여 컨텐츠를 탐색(navigation)

action은 Gesture가 성공적으로 끝난 후에만 호출

Swipe는 분리되어 있기 때문에, flicks 또는 빨리감기 동작에만 사용해야합니다

# Pan

패닝(드래그)하는 Gesture를 찾으며, UIgestureRecognizer의 구체적 하위클래스

1. 먼저 translation메소드를 통해 이 Pan Gesture로 인해 변환되는 좌표 값을 얻어와야합니다. 

2. 그리고 우리의 이미지View에 이 translation을 적용해줘야합니다.