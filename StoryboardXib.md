# Storyboardxib

[참고 블로그] (https://hamait.tistory.com/708)

[참고 블로그] (http://suho.berlin/engineering/ios/ios-storyboard-nibxib-code/)

## Storyboard의 장점

– 퍼포먼스: 최초 뷰컨트롤러 하나만 초기화된 후 나머지는 세구에가 동작할 때 동적으로 객체화 됨.

– 프로토타입: 스토리보드+코드 몇 줄로 빠른 목업 프로토타이핑이 가능.

 

## Storyboard의 단점

– 재사용성: 스토리보드는 의존하는 모든 뷰 컨트롤러들과 함께 복사 혹은 이동해야 함.   스토리보드의 나머지 기능에 의존적이기 때문에 뷰컨트롤러 하나만 뽑아내 재사용하기가 성가심.

– 데이터 흐름: 스토리보드는 뷰컨트롤러들 사이의 흐름을 다루지만 데이터의 흐름은 관여하지 않음.

## NIB의 장점: 재사용성

## NIB의 장점이자 단점: 성능

## Code 장점: 동작방식, 코드만이 방법일 때, 성능, 재사용성, 머지 충돌(Merge Conflicts)

## Code 단점: 프로토타입 제작(Prototyping), 리펙토링

## XIB:

1) Xib files are used with a single UIView.

2)It's very difficult to implement complex auto-layouts in xib.

3)It's utilizes more memory as compared to storyboard and quiet slow.

4) It is compatible from iOS5 and onwards

5) You can do localizations for different languages and countries using different XIBs .

6) It's difficult to use same Xib to support multiple devices.

## Storyboard

1)You can layout all your Scenes like View Controllers, Nav Controllers, TabBar Controllers, etc in a single storyboard.

2)You can use Auto Layout easily that defines mathematical relationships between elements defining their position and sizing.

3)Usually fast and allocates less memory.

4)It's not compatible prior to iOS 5 .

5)"Dynamic" and "Prototype" cells can be used easily.

6)Storyboards best to use for the apps with a small to medium amount of screens.