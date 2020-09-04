# Container and Codec

1. History
1. Compression
1. Media Codecs

![image](/uploads/3052ab04de82fea971efe8d012f26d42/image.png)

# Container
```
무언가를 담는 포장지 같은 개념
```
![image](/uploads/b942dd1cc75648a371a73210460654c7/image.png)

# Codec
```
COder and DECoder

음성 또는 영상의 신호를 디지털 신호로 변환하는 코더와 그 반대로 변환시켜 주는 디코더를 통틀어 부르는 말.
=> 영상 신호를 디지털 신호로 변환하는 것을 코딩(인코딩), 디지털 신호를 영상으로 변환하는 것을 디코딩이라고 한다.

고용량의 미디어 파일 크기를 획기적으로 줄일 수 있게 하여, 파일 저장과 스트리밍을 수월하게 했으며, 역으로 보다 고화질의 영상을 즐길 수 있게 하였다.
```

# Details
```
"통합코덱"은 코덱을 하나하나 설치하는 것이 귀찮은 사람들을 위한 코덱 모음집이다.

"내장코덱"은 몇몇 동영상 플레이어가 자주 쓰는 코덱을 안에 포함하고 재생시켜주는 방식

"FFmpeg"는 현재 쓸만한 코덱의 통합코덱이며, 상위 미디어 플레이어의 내장코덱 그 자체이며, 사실상 표준코덱이다.
```

# History
```
초창기 코덱의 춘추전국시대에는 다양한 코덱이 존재했다. 그 중 MPEG-1 Audio Layer 3 (MP3)가 현재까지 이어져 내려오고 있다.

MPEG-2 Part.2 시대. DVD로 정리되며, 코덱의 대세가 일단락 되었다. WMV가 유명하다.

MPEG-4 Part.2 시대. 인터넷(스트리밍)에서 급격한 발전이 있었으나, MS의 독점적 행태(ASF, MS MPEG4)에 반기를 들면서 DivX, DiviX의 독점에 반기를 들면서 Xvid(DivX를 뒤집었다)가 등장한다. 

그러거나 말거나 어둠의 세계에서는 "대 P2P 시대"가 열린다(...)

MPEG-4 Part.10/H.264(AVC) 시대. MPEG(미디어)그룹과 ITU(통신)그룹의 연합하여 코덱을 발전시켰다. 

그래서 같은 코덱인데 이름이 두개다(...) 아이폰, Blu-ray Disc 이후부터 사람들에게 친숙해졌다. 이어서 MPEG-H Part.2(H.265 HEVC, HEIC, UHD)가 나온다.
```

# Encoding Options
```
```
![image](/uploads/d1701a11cc175a884ab9b9f50e592a7d/image.png)

# Audio Codec
```
```
![image](/uploads/d73cb6a4f58ed500b2f9844930d9c689/image.png)

# Video Codec
```
```
![image](/uploads/eeee1aba2ee900983fb7146acef5634c/image.png)





[https://en.wikipedia.org/wiki/Codec](https://en.wikipedia.org/wiki/Codec)

[H.264/H.265](video2)