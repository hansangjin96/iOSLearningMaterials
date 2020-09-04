# NSOperation

[참고 블로그 - 컨텐츠 목록 다운로드 예제(테이블 뷰, 네트워크, NSOperation)](http://minsone.github.io/mac/ios/how-to-using-nsoperation-and-nsoperationqueue)

[참고 2 제드](https://zeddios.tistory.com/510)

[blog 3](http://theeye.pe.kr/archives/2470)


## 백그라운드로 작업을 수행하는 방법 

```
1) NSTread

2) GCD - dispatch queue (C API)

3) NSOperation - NSOperationQueue (obj-C API)

NSOperation은 NSOperationQueue로, GCD는 dispatch queue를 통해서 각각의 작업들을 관리
```

## 작업 취소

NSOperation의 Cancel을 통해 작업을 취소할 수 있도록 제어가 가능

## KVO

isCancelled, isFinished등 작업의 상태가 변경되었는지를 알 수 있음

## 작업의 재사용

NSOperation의 자식 클래스를 만들어서 원하는 형태로 작업이 가능하며 작업이 끝나더라도 재사용할 수 있음

## 작업 우선순위

각 작업은 우선순위가 있으며 작업들간의 우선순위를 매깁니다. 우선순위가 높은 작업이 우선순위가 낮은 작업보다 먼저 수행이 됩니다.

## 작업 간의 의존성

작업이 수행한 후 다른 작업이 수행할 수 있도록 작업 계층을 만들 수 있음

- NSBlockOperation : 하나 이상의 블록 객체를 동시에 실행하는데 사용하는 클래스

- NSOperation : 커스텀 Operation객체를 정의하기 위한 base class

