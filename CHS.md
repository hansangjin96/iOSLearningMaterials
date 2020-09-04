[이해하기 쉬운 블로그](https://mamu2830.blogspot.com/2019/10/chs-lba.html)

[깔끔하게 잘 정리된 블로그](https://mamu2830.blogspot.com/2019/10/chs-lba.html)

# Cluster
```
섹터 단위로 입출력을 처리할 경우 시간이 오래걸리므로 여러개의 섹터를 묶은 클러스터를 사용
* 섹터 = 하드 디스크의 물리적 최소 단위
```
![image](/uploads/93bf41b030f4747bc89f99bbc5037759/image.png)

# Slack
```
물리적 구조와 논리적 구조의 차이로 발생하는 낭비 공간
1. RAM Slack (Sector Slack)
2. File Slack (Drive Slack)
3. File System Slack
4. Volume Slack
```

## Ram Slack
```
램에 저장 되어있는 데이터가 디스크에 저장될 때 512바이트씩 기록되는 특성때문에 발생하는 공간
램 슬랙을 이용하면 파일의 끝을 알 수 있기 때문에 파일 복구시 유용하게 사용
```

## File Slack
```
클러스터의 사용으로 낭비되는 공간 중 램 슬랙을 제외한 부분
특정 파일이 해당 저장매체에 존재하였는지 규명 가능
 - 파일을 클러스터 단위로 나눈 뒤, 클러스터의 마지막 부분과 파일 슬랙중 일치하는 부분이 있는지 확인
```

## File System Slack
```
파일 시스템 할당 크기와 볼륨 크기 간의 차이로 발생되는 공간
```
![image](/uploads/9a1102970ae9c858dedb564a3eb5f362/image.png)

## Volume Slack
```
전체 볼륨 크기와 할당된 파티션의 크기 차이로 발생되는 공간
```
![image](/uploads/b31f0a4b2909293f5f18de52e02a93ca/image.png)



# CHS 방식 (Cylinder, Head, Sector) 방식
```
디스크의 물리적 구조에 기반한 방식
대용량 디스크를 지원하지 못해 표준에서 제외
```
![image](/uploads/a0b75dd428e17d58a4cbf13235028cf1/image.png)

# LBA방식 (Logical Block Addressing)
```
디스크의 0번 실린더, 0번 헤드, 1번 섹터를 첫 번째(0번) 블록으로 지정
디스크의 마지막 섹터까지 순차적으로 주소를 지정
물리적 구조 정보 불필요
```
![image](/uploads/a66ccc4a45dbc6bcff6169f70b1d739a/image.png)