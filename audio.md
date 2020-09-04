# PCM(Pulse Code Modulation)
## history
## implementation
````
압축되지 않은 디지털 오디오에 아날로그 신호를 0과 1의 디지털 신호로 변환하는 방법
소리 등의 연속되는 값을 기록하기 위해 쓰이며, 전자악기 중 일부의 음원을 표현하는 방식

WAV 파일도 기본적으로 PCM 데이터를 저장

회로 구조가 복잡한 문제가 있었지만 집적회로 기술의 발달로 해결
'ADPCM' 등 전송에 더 유리하도록 많은 개량

지금은 APT-X나 무손실 포맷을 쓴다고 한다.

아날로그와 달리 디지털에선 처리 가능한 범위를 넘어가는 부분은 양자화가 불가능하기 때문에 파형의 피크 부분이 한도를 넘겨버려서 잘려 없어지는 클리핑 현상이 발생
````

## Sampling
```
음성과 같은 아날로그 신호를 디지털화하기 위해 일정한 간격으로 샘플링을 하여야 한다. 이것을 PAM(펄스진폭변조)라고 한다.
```
![image](/uploads/de73e2bcb57cab6dbe54f94e1a0c4fc0/image.png)

## Quantization
```
PAM 펄스 진폭의 크기를 디지털 양으로 변화하는 것이다.
```
![image](/uploads/11efc23061aad82bcc30dc0dba5305d0/image.png)

## Encoding
```
양자화된 PCM 신호(2진 비트열)를 실제 전송을 위한 디지털 신호로 변화하는 것이다.
```
![image](/uploads/2e8489e2c42e69f4419b222bd01e0ae5/image.png)

[https://en.wikipedia.org/wiki/Pulse-code_modulation](https://en.wikipedia.org/wiki/Pulse-code_modulation)

[wave format](audio2)