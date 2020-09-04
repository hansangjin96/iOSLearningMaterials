# H.264/H.265
1. Naming
1. History
1. Applications
1. Design
1. Implementations
1. License

# H.264

# Description
```
2003년에 발표된 동영상 표준 규격. 기존 MPEG-4 Part 2보다 발전된 비디오 코딩이라 AVC(Advanced Video Coding)로도 통용된다.
```

# Efficiency
```
화질 향상 겸 H.263의 두 배의 압축률을 가지는 것으로 목표로 개발되었고, 실제로 두 배에 가까운 효율을 구현한다.
```

# Feature
```
방송 규격 : 블루레이에 기본 코덱으로 채택되면서 H.264가 사용되기 시작되었다.

개발 당시 컴퓨터 사양이 부족했기 때문에 보급속도가 느렸다.
```


# H.265
```
2013년 4월에 발표된 MPEG-H Part.2 규격으로 기존보다 압축 효율이 높아서 HEVC(High Efficiency Video Coding)라고도 한다.

복잡도가 H.264에 비해 5배 정도 늘어나고 압축률이 H.264 대비 최대 50%까지. 동일 화질(PSNR)로 따지면 대략 30%를 웃도는 정도의 압축률을 보인다. 


압축률이 올라가는 만큼 알고리즘도 복잡해져서 CPU의 연산 성능만으로는 인코딩-디코딩이 매우 힘들다.

본래 4K 10bit 이상 HDR을 목표로 한 코덱이므로 1080p FHD 이하 해상도와 8bit에서는 상대적으로 효율이 낮다.

위 두 가지 단점 때문에 2019년 기준으로도 보급률이 낮다.

라이센스 비용을 비싸게 받음 

-> 그래서 구글은 유튜브를 중심으로 VP9을 푸시하고 있고, 넷플릭스와 함께 AV1을 발전시킴


2017년 9월부터 애플의 운영체제에 전격적으로 도입된다. 
모바일 운영체제 iOS 11 및 최신 macOS에서 HEVC 코덱 지원을 시작한다. 
-> 4k 60fps압축, 편집 가능


H.265를 사용한 이미지 포맷으로 BPG, HEIF가 있다.
```

# H.266
```
Versatile Video Coding (VVC)

MPEG와 VCEG가 함께 구성된 팀인 JVET(JointVideoExpertTeam)에서 만든 차세대 비디오 코덱으로, H.265(HEVC)의 후속작이다. 
한때 FVC(Future Video Coding)라고도 알려졌다.

VR 시장의 발달 -> 16K 수준의 초고해상도 영상처리용으로도 개발되고 있다. 

디스플레이 기술의 발달로 HDR 시장이 확대됨에 따라 이에 대응하기 위해 10비트 색심도는 물론이고 16비트 색심도를 지원하며 1000니트, 4000니트, 10000니트의 밝기 표현을 지원

트랜스코딩 알고리즘이 복잡해짐에 따라 인코딩 복잡성은 H.265 대비 최대 10배, 디코딩 복잡성은 최대 2배 증가할 것으로 예상

```
[https://en.wikipedia.org/wiki/Advanced_Video_Coding](https://en.wikipedia.org/wiki/Advanced_Video_Coding)

[VP9/VP10](video3)