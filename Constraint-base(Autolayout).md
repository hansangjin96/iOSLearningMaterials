# Constraint base(autolayout)

[블로그](https://jinshine.github.io/2018/06/07/iOS/%EC%98%A4%ED%86%A0%EB%A0%88%EC%9D%B4%EC%95%84%EC%9B%83(AutoLayout)%EA%B3%BC%20Layout%20%EA%B0%9C%EB%85%90/)

[블로그2](https://zeddios.tistory.com/380)

# 1. Frame 기반의 프로그래밍 방식(Frame-Based Layout)
- 가장 유연하며 빠른 성능
- 모든 뷰에 대해 개별적인 설정과 관리가 필요.
- 설계 및 디버그나 유지관리에 많은 노력이 필요하다는 단점이 있습니다.

# 2. Autoresizing masks
- Frame기반의 프로그래밍을 좀 더 수월하게 만들어줄 Autoresizing mask를 도입했지만 Autoresizing mask조차 요즘같은 트랜디한 UI를 구현하기 힘들어서 이를 극복하기 이해 Auto Layout이 도입되었습니다.

# 3. Auto Layout

Auto Layout이란 기존의 Frame-Based Layout과 다른 View들 간의 관계를 이용하여 View의 위치와 크기를 자동으로 결정하는 Layout System입니다.

- 제약 조건을 이용해 유저 인터페이스 정의
- 뷰간의 관계 설정을 통한 크기와 위치 계산
- 내/외부 변경 사항에 동적으로 반응
- Frame 기반에 비해 느린 포퍼먼스

## Auto Layout tools
-  Stack : 선택한 객체들을 하나의 스택 뷰로 변환
- Align : 정렬에 관한 제약사항 설정
- Pin : 객체 간 상대적 거리 및 크기에 관한 제약사항 설정
- Resolve Issues : 오토 레이아웃 관련 문제 해결

## Auto Layout Attributes
- Leading : 상대 뷰와의 왼쪽 면과의 간격
- Trailing : 상대 뷰와의 오른쪽 면과의 간격
- Top : 상대 뷰와의 위쪽 면과의 간격
- Bottom : 상대 뷰와의 아래쪽 면과의 간격