# FTL(Flash Translation Layer)

[blog](http://blog.skby.net/ftl-flash-translation-layer/)

[blog-kakao](https://tech.kakao.com/2016/07/15/coding-for-ssd-part-3/)

```
플래시 메모리와 파일 시스템 사이에서 플래시 메모리를 디스크처럼 사용할 수 있게 해주는 Mapping 기술

Hard Disk에는 물리적인 섹터가 있지만, SSD에는 page와 block밖에 없음
하지만 FAT,NTFS같은 파일시스템과 그 위에서 작동하는 운영체제는 섹터를 기반으로 동작함
따라서 FTL이 물리적 구조를 논리적 구조로 바꿔줌으로써 SSD의 물리적 한계를 극복
```
![image](/uploads/1544b261d177e79775b47a287bb9d894/image.png)


## FTL 필요성

1. 플래시 메모리 섹터들의 최대 지우기 횟수 결점 보완
2. DISK I/O를 플래시 메모리에서 동작할 수 있도록 지원
3. NAND 플래시 한계 : 쓰기보다 지우기가 느린 특성

![image](/uploads/f886428ab8b768d79d30e1daf6d6722a/image.png)
![image](/uploads/cc0cb13759d48a9a10b9546d7d6ea131/image.png)


## 구조

```
1. STL(Sector Translation Layer): Address Mapping, Garbage Collection, Wear leveling 등을 담당한다.
   - Address Mapping(주소매핑): 파일시스템으로부터의 논리적 주소를 NAND Flash Memory의 물리적 주소로 연결시켜준다. 
    이는 Flash Memory의 특성상 특정 페이지의 데이터를 수정하고자 할 때, 
    새로운 데이터를 다른 빈 페이지에 기록하고 이전 데이터는 무효화(invalidation)시키고 새로운 데이터의 주소 매핑정보를 유지하기 위함이다.
   - Garbage Collection(가비지 컬렉션): 무효화된 페이지를 많이 포함하는 블록을 선택하여 유효한 페이지들을 다른 블록에 복사한 후에 해당 블록을 삭제하여 재사용 할 수 
     있도록 해주는 기법이다. 
     이러한 동작은 페이지 복사를 위해 Read 및 Program동작을 수행하여야 하고 블록을 삭제하기 위해 Erase동작을 수행하여야 하므로 비용이 많이 든다.

2. BML(Bad-block Management Layer): NAND Flash Memory는 공장 출하시의 초기불량(initial bad block)과 사용 중 불량이 발생하는 블록(run-time bad block)을 스펙에서 허용하고 있다. 
이러한 불량을 관리하고 Error 처리 등을 BML이 담당한다.

3. LLD(Low Level Driver):  NAND Flash를 사용하기 위한 Driver로 Flash interface를 상위 계층에 제공한다.
```

## FTL 핵심 기술

```
1) Wear Leveling
 - 블록당 writter 횟수를 모니터 하여 균등하게 분배
 - 특정 블록에만 write되는것을 방지하여 수명연장
```
![image](/uploads/7696dad802dada00d6db75cb0f4c0666/image.png)


```
2) Garbage Collection
 - 블록을 실제로 샂게하지 않고, 표기 후 적절한 시점에서 일괄 삭제처리
```
![image](/uploads/60f28ebb841a199e05215599a76448c6/image.png)

```
3) Over Provisioning
 - wear leveling, GC를 작업하기 위한 여유공간
```
![image](/uploads/f7a07f5ebc97119ff8768c3b5dead41a/image.png)

## FTL Mapping 방식

![image](/uploads/a79c820465b720f66ea57e7e136dd900/image.png)

![image](/uploads/756060c5caaab2f839196d79f49b0495/image.png)



# NAND Flash Memory

```
읽기 속도가 느린 대신 쓰기 속도가 빠르고 NOR에 비해 싼 메모리(SDD)
```
