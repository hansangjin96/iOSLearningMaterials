# 아날로그에서 디지털로 변환

# Sampling
```
표본화. 아날로그 함수를 디지털화하기 위해 정해진 주기로 값을 수집하는 것을 말한다. PCM 등 디지털 기록 체계의 최우선 사항이다. 

나이퀴스트-섀넌의 정리 : 샘플링을 할때 원음이 가지는 최대 주파수의 2배 이상으로 촘촘히 하면 손실이 발생하지 않는다
```
![image](/uploads/eaef83baf0663eb10697af2e6bb5bd9a/image.png)

# Quatization
```
아날로그 신호의 크기는 uncountable이지만 디지털 신호의 크기는 countable이다.
따라서 아날로그를 디지털로 바꾸려면 양자화를 진행해야함

샘플링된 신호의 크기를 가장 가까운 허용된 값으로 근사시킴

손실이 발생하는 비가역적 과정
```
![image](/uploads/4707f773a1891d892292eb058af47a7e/image.png)
