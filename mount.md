# Volume과 Partitioning: format 과 mount, mount point

# 볼륨(Volume)
```
디스크 상의 논리적인 분할 단위
연속된 섹터의 집합
파티션보다 더 유동적이고 논리적인 개념임
```

![image](/uploads/0ecb4d22f8b1fc6acddeed03b739c707/image.png)

# 파티션(Partition)

[blog](https://blog.naver.com/bitnang/70183582975)

```
저장매체의 저장공간을 논리적으로 분리한 것
* Boot Record 영역 : 각 파티션의 크기, 위치, 운영체제 등의 정보
```

## Master Boot Record
```
분할된 각 파티션의 BR을 관리하는 영역
```

![image](/uploads/2e9dfb53546263fd058062c0a0670690/image.png)
![image](/uploads/91d09cdb2728a07a525d75ce56f50f35/image.png)

## Boot Code
````
컴퓨터가 부팅될 때 수행되는 코드
부팅 가능 파티션을 찾아 파티션의 Boot Sector를 호출하는 역할
````

## Partition Table 영역
```
16바이트씩 4개의 파티션 정보가 저장
* 부트 플래그(Bootable Flag) : 해당 파티션이 부팅 가능한지 나타냄
```

## 확장 파티션 (Extended Partition)
````
파티션을 4개까지 밖에 분할 못하기 때문에 4번째 파티션 테이블이 또 다른  MBR을 가르키도록 하는 구조
````
![image](/uploads/8c27db9c7d27b9cf77a17eac06606d28/image.png)

[format mount](https://kimhyun2017.tistory.com/21)

# 마운드(mount)
![image](/uploads/a76a15a83d721747ba4cb46753fb6d04/image.png)