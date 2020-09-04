[Thread Safe](https://m.blog.naver.com/PostView.nhn?blogId=complusblog&logNo=220985528418&proxyReferer=https:%2F%2Fwww.google.com%2F)

# Thread Safe

멀티 쓰레드 환경에서 코드에 쓰레드가 동시 접근하여 의도치 않은 결과를 도출
```
1) MUTEX를 이용한 동기화 방법

pthread_mutex_lock(&mutx);
... Critical Section
pthread_mutex_unlock(&mutx);
 ```

```
2) SEMAPHORES를 이용한 동기화 방법

A Thread

state = sem_init(&bin_sem,0,0);
while(number != 0)
wait...
데이터 처리
sem_post(&bin_sem)

B Thread

sem_wait(&bin_sem);
데이터 처리
```

통상적으로 Mutual Exclusion(상호배제) 방식을 이용한 Critical Section 처리가 자주 사용되는 편이다.

# Thread-safe를 지키기 위한 방법

```
1. Re-entrancy
어떤 함수가 한 스레드에 의해 호출되어 실행 중일 때, 다른 스레드가 그 함수를 호출하더라도 그 결과가 각각에게 올바로 주어져야 한다.

2. Thread-local storage
공유 자원의 사용을 최대한 줄여 각각의 스레드에서만 접근 가능한 저장소들을 사용함으로써 동시 접근을 막는다.
이 방식은 동기화 방법과 관련되어 있고, 또한 공유상태를 피할 수 없을 때 사용하는 방식이다.

3. Mutual exclusion
공유 자원을 꼭 사용해야 할 경우 해당 자원의 접근을 세마포어 등의 락으로 통제한다.

4. Atomic operations
공유 자원에 접근할 때 원자 연산을 이용하거나 '원자적'으로 정의된 접근 방법을 사용함으로써 상호 배제를 구현할 수 있다.
```