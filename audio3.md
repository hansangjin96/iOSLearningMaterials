# MP3
1. History
1. Design
1. Licensing, ownership, and legislation
1. Alternative technologies

# History
```
1993 : MPEG-1
->MPEG-2와 MPEG-2.5로 확장

1997 : MPEG3 등장!
-> 비교적 적은 용량에 CD와 가까운 음질로 들을 수 있어서 엄청 인기!
```

# Feature
```
독일의 프라운호퍼社가 주도적으로 개발한 오디오 코덱

"손실 압축 포맷"
-> 따라서 WAV로 복원해도 손실된 부분 복구 불가

압축 효율성은 그 이후에 나온  WMA, Vorbis, AAC, Opus 등에 비해 떨어진다.

320Kbps이상의 음역대는 일반인은 구분하지 못하기 때문에 FLAC과 큰 차이가 없음
-> FLAC은 음원의 신뢰성 확보 측면
```

# Design

## File Structure
![image](/uploads/92132be56b7da4c41d060b8ceacdbdd2/image.png)


## Encoding & Decoding
```
파트 1은 오디오 신호를 프레임이라고하는 작은 조각으로 나누고 수정 된 이산 코사인 변환 (MDCT) 필터가 출력에서 ​​수행됩니다. 
파트 2는 샘플을 1024 포인트 FFT ( 고속 푸리에 변환 )로 전달한 다음 심리 음향 모델이 적용되고 출력에서 ​​다른 MDCT 필터가 수행됩니다. 
3 부에서는 비트 전송률 및 사운드 마스킹 요구 사항 을 충족하기 위해 자체적으로 조정되는 노이즈 할당이라고하는 각 샘플을 정량화하고 인코딩 합니다. 
파트 4 는 헤더 , 오류 검사 의 4 개 파트로 구성된 오디오 프레임이라고하는 비트 스트림 형식을 지정합니다.
```

## Quality
```
비트레이트가 높을수록 MP3 데이터 스트림이 커지고 원본 녹음에 가까워짐
비트레이트가 너무 낮으면 Compression effect가 생김
```

# Derived Codec
```
MP3HD(무손실) : HD 지원 기기에 파일을 넣고 재생하면 무손실, 일반 기기에 넣고 재생하면 손실 320kbps로 재생되는 대단한 호환성

MP3PRO(고효율) :  MP3에 SBR 대역을 추가한 코덱

MP3 Surround(다중채널):  최대 5.1채널을 지원
```

# Alternative technologies
```
AAC(Advanced Audio Coding )가 MP3의 후속으로 가장 널리 사용됨
```

# Licensing, ownership, and legislation
```
기본 MP3 디코딩 및 인코딩 기술은 유럽 연합에서 특허가 없으며 모든 특허는 늦어도 2012 년에 만료되었습니다. 
```

[https://en.wikipedia.org/wiki/MP3](https://en.wikipedia.org/wiki/MP3)

[ogg](audio4)