# Grand Central Dispatch

[blog1](https://duwjdtn11.tistory.com/558)

[blog2](https://zeddios.tistory.com/516)

[example](https://meetup.toast.com/posts/88)

# Disapatch Queue

이전에는 개발자가 직접 쓰레드를 생성하고 관리했지만, GCD를 이용하면 OS가 자동으로 관리

## serial dispatch queue : 등록된 작업을 한번에 하나씩 처리
## concurrent dispatch queue : 여러 작업을 동시에 처리

![image](/uploads/c34fbddb37235e481a5e70fcbc485d6d/image.png)

![image](/uploads/3cccc36eaa4b44e84400937b798d12dc/image.png)

## main queue : 메인 스레드에서는 serial queue 사용, 모든 UI 처리는 메인 스레드에서 처리
## global queue :  편의상 사용할 수 있게 만들어 놓은 Concurrent queue, 처리 우선순위를 위한 quality of service 제공

(Qos를 지정함으로서 중요도를 표시하고, 이로 인해 앱이 responsive해지고 에너지 효율이 좋아짐!)

![image](/uploads/4258c8655c05ce0857efa26f39753a34/image.png)


## sync / async

![image](/uploads/ee0ec2c0d22e499751fef329df6cf674/image.png)

![image](/uploads/cf5b1d223757efa33049a0a974b34045/image.png)

## QOS(quality of service)

NSOperation, NSOperationQueue, NSThread 객체, dispatch queues 및 pthread (POSIX 스레드)로 수행할 작업을 분류할 수 있습니다.

작업을 위해 QoS를 할당하면, 해당 중요도(importance)를 표시하고, 시스템이 해당 QoS의 priority를 지정하여 적절하게 스케쥴링

![image](/uploads/600f9cd48d4801bcf5ecfd95e26abcd1/image.png)

