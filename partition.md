# MBR, BR/GPT: Primary partition과 Secondary partition, 한계


![image](/uploads/d4143ebd19908ac3f988695c1fb607c7/image.png)

컴퓨터에 전원이 공급되면 메인보드에 내장된 펌웨어(BIOS - basic input output system firmware interface)가 실행됨

MBR의 기술적 제한을 해결하기 위한 것이 GPT

GPT는 BIOS가 부팅 불가, EFI,UEFI가 가능

## UEFI의 장점
```
   - GPT(GUID Partion Table)를 사용한 대용량 디스크(2TB 이상)에서 부팅이 가능하게 한다.
   - CPU에 독립적인 아키텍처이다.
   - CPU에 독립적인 드라이버이다. 
   - 운영체제를 설치하기 전에 네트워크 사용을 포함하여 유연한 기능을 제공한다.
   - 모듈화 디자인이다.
   - Backward and forward compatibility
```

## 파티션의 종류
```
리눅스는 Primary , Extended, Logical 파티션으로 나뉘는데,
주 파티션은 4개까지 생성이 가능
4개 이상이 필요할 경우 확장파티션을 생성해야한다.
확장 파티션을 다시 논리 파티션으로 나눠서 12개까지 생성 가능
```

# GPT

```
BIOS가 아닌 EFI 펌웨어를 사용하는 디스크 형식
MBR과 마찬가지로 디스크 정보를 담는 영역
LBA 방식 사용
128개의 파티션을 만들 수 있음
최대 8ZB
LBA0에 Protective MBR을 가짐
CRC를 이용해 파티션 테이블을 보호
중요 데이터는 볼륨의 끝에 복제본을 저장하는 방식으로 장애에 복구 가능
```

## GPT 구조

![image](/uploads/86a1b001e0ee4a167d33f03d3f50382a/image.png)


