# S/W FTL, eMMC, SD, NVMe, UFS

[삼성 블로그](https://news.samsung.com/kr/%EB%AA%A8%EB%B0%94%EC%9D%BC-%EA%B8%B0%EA%B8%B0%EC%9A%A9-%EB%82%B8%EB%93%9C%ED%94%8C%EB%9E%98%EC%8B%9C-%EB%A9%94%EB%AA%A8%EB%A6%AC%EC%9D%98-%EC%A7%84%ED%99%94-emmc%EB%B6%80%ED%84%B0-ufs%EA%B9%8C)

# NVMe
[blog](https://www.samsungsemiconstory.com/11540
````
SSD를 탑재한 서버, PC의 성능 향상과 설계 유연성을 높일 수 있도록 만든 PCIe 인터페이스 기반의 프로토콜.
NVMe는 SSD의 성능을 최대한 활용할 수 있도록 개발되었으며, 
HDD(Hard Disk Drive)에 최적화된 기존의 SATA(Serial Advanced Technology Attachment) 인터페이스보다 6배 이상 빠른 속도를 자랑한다.
따라서 데이터 처리 속도를 크게 줄일 수 있다.
````
![image](/uploads/6da3adf55c2d66dc16def176c2180728/image.png)
![image](/uploads/c7923b44850a99c515393c16ff9a0c20/image.png)
![image](/uploads/6b522d53940038774bcc63dfa62ec579/image.png)

# eMMC
````
데이터 고속 처리를 위해 모바일 기기에 내장하는 메모리 반도체
매모리 카드와 달리 컨트롤러와 낸드플래시 메모리가 패키지로 통합돼 제품에 내장
````

## UFS

```
차세대 플래시 메모리 카드 표준.
UFS는 국제 반도체 표준화 기구 ‘제덱(JEDEC)’의 최신 내장 메모리 규격인 ‘UFS 2.0’ 인터페이스를 적용한 차세대 초고속 플래시 메모리이다.
기존 eMMC(embedded Multi Media Card) 병렬 인터페이스는 한 번에 한 방향으로만 데이터를 전송할 수 있어 동시에 읽고 쓰는 것이 불가능한 반면, 
UFS는 읽고 쓰는 별도의 전용 경로가 있는 LVDS(Low-Voltage Differential Signaling) 직렬 인터페이스가 있어 동시에 읽고 쓰는 쌍뱡향 소통이 가능하다.
또한 UFS는 SSD에서 사용중인 속도 가속 기능인 ‘커맨드 큐(Command Queue)’를 적용했다. 
커맨드 큐는 여러 개의 명령어를 동시에 처리하는 기술로 내장 메모리카드의 성능 극대화를 위해 사용되는 기술이다.
```

![image](/uploads/499b7063061e09351492db65f68829b6/image.png)
![image](/uploads/78353184101d58ccda5a2f3d2df7f818/image.png)
