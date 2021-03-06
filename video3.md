# VP9/VP10

1. History
1. Features
1. Technology
1. Adoption
1. Patent Claims
1. Successor: from VP10 to AV1

# vp9

# 개요
```
2012년 구글이 개발한 오픈소스 비디오 코덱으로, VP8을 계승하였다.
```

# 장점
```
64x64 매크로 블럭을 지원하여 압축률이 높아졌다.

모션 예상 알고리즘의 개선을 통해 CG 영상(게임 영상, 애니메이션 등)의 화질 개선이 큰 편이다.

오픈 소스이며, 특허 관련 로열티가 없는 무료 코덱이다.
```

# 단점
```
H.265와 화질이 비슷하거나 조금 떨어짐 but 265보다 인코딩 시간이 오래걸림

그래픽 카드와 브라우저가 함께 하드웨어 가속을 지원하지 않으면 소프트웨어 디코딩을 해야 하므로 저사양에서 문제를 일으키는 것

->  VP9 지원 환경이 차차 정착되면 자연스레 해결될 것이다. 
구글의 유튜브 이외에도 넷플릭스, 아마존닷컴 등의 웹 사이트들이 VP9 코덱을 채택하기 시작하면서 VP9 코덱도 또한 하드웨어 디코딩을 지원하는 기기들이 늘어났다.
```

# 사양
![image](/uploads/7ad1d505d327ed900d132f17e3bfc0ae/image.png)

# 발전
```
 2015년 9월 1일부터 무료 코덱을 개발하고 있는 구글, 모질라, 시스코 외에 마이크로소프트, 아마존, 인텔, 넷플렉스가 
H.265의 특허권을 가지고 있는 MPEG LA에 대항하기 위해 The Alliance for Open Media라는 이름으로 연합을 맺었다. 
홈페이지 그리고 이 단체에서 개발하는 코덱인 AV1에다가 VP10을 통합시키기로 결정했다. 기존 VP10의 기능들은 모두 통합된다.
```

# AV1

# 개요
```
AOMedia Video 1

오픈 미디어 연합(Alliance for Open Media)이 개발하여 2018년 3월 28일에 발표되어 6월 25일에 세부 스펙이 공개된 오픈소스 기반의 비디오 코덱.
```

# 효율
```
VP9 및 H.265 대비 약 30%의 데이터 레이트 절감이라는 목표는 달성했다.

그러나, 19년 초 표준 인코더 기준, 인코딩 시간이 VP9 보다 16배 길고 개인이 적당한 인코더 구해서 
써먹기에는 호환성 이전에 버그가 문제가 되는 등, 안정화와 최적화가 숙제로 남아있다. 
```
https://namu.wiki/w/%ED%8C%8C%EC%9D%BC:1616b28cc562fcbc1.png

```
2020년 아직 AV1이 대중화 하지 않는 시기에 H.266이 등장하였다. 
H.265 대비 데이터 레이트는 50% 절감 하면서도 인코딩은 10배 디코딩은 2배의 시간이 필요해서 AV1 대비 데이터 절감과 인/디코딩 면에서 우월하다. 
하지만 해당 코덱은 라이센스 비용이 유료로서 공개 코덱이자 라이센스 비용이 없는 AV1이 대중화 할만한 시간은 남아 있다.
```

# level
![image](/uploads/33af237f0e1997851e06cc19f615ddbb/image.png)


[https://en.wikipedia.org/wiki/VP9](https://en.wikipedia.org/wiki/VP9)

[MP4 vs AVI](video4)