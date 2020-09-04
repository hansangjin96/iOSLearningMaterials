# Wave Format

## Description
```
WAVeform audio format : 마이크로소프트 윈도우에서 표준적으로 사용되는 PCM 데이터 파일

데이터를 "청크"에 저장하기 위한 RIFF 비트스트림 형식 방법의 응용 프로그램(RIFF : 태그가 있는 파일 형식)
일반적으로 압축되지 않은 오디오 형식에서 사용됨
```

![image](/uploads/e86468e77d1d00f0c5a67804260518e4/image.png)

![image](/uploads/16bf5e7432d4599c476764c43d1a530f/image.png)

## Features
```
FLAC 형식이 무손실 압축 포맷이라면, 이쪽은 "무손실 무압축" 포맷이다.

이미지 파일로 치자면 BMP나 TIFF, 또는 DSLR 등에서 지원하는 RAW 파일과 비슷하다고 할 수 있다. 
이 때문에 보통 WAV 파일의 용량은 FLAC의 2배 이상이다. 

mp3 확장자는 편집 후 재압축하면 음질이 손상될 우려가 있고, 손실형 압축을 해버리면 편집에 문제가 생길 수 있기 때문에 
wav 확장자를 쓰는 것이 프로그래머나 편집자에게는 훨씬 좋다.
```

## Metadata
```
INFO 청크의 메타 데이터 로 태그를 지정
```

## Popularity
```
압축되지 않은 WAV 파일은 크기가 크므로 인터넷을 통한 WAV 파일 공유 는 흔하지 않습니다.

1 세대 아카이브 파일 을 유지하는 데 적합하고 , 디스크 공간이 제한되지 않는 시스템에서 사용하거나, 
압축 및 압축 해제에 시간이 소요되는 오디오 편집과 같은 응용 프로그램에서 사용하기에 적합
```

## Limitations
```
부호없는 32 비트 정수 를 사용하기 때문에 4GiB 미만의 파일로 제한
```

## Audio CDs
```
오디오 CD는 WAV 파일 포맷이 아닌 Red Book Audio를 사용함
공통점 : 압축되지 않은 PCM으로 인코딩됨
```

[https://en.wikipedia.org/wiki/WAV](https://en.wikipedia.org/wiki/WAV)

[MP3](audio3)