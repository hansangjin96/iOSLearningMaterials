# File System
```
세미나 
23일 목요일 3시 ~ 5시
Fusion 1
```
# 목차
1. [데이터의 역사](history) 
1. [FTL(Flash Translation Layer)](FTL) 
1. [HOST Bus, Controller, Flash bus = 전송 규격, 제어 규격](bus)
1. [S/W FTL, eMMC, SD, NVMe, UFS](UFS) 
1. [Sector와 Cluster, Slack - CHS 방식/LBA 방식](CHS)
1. [Volume과 Partitioning: format 과 mount, mount point](mount)
1. [MBR, BR/GPT: Primary partition과 Secondary partition, 한계](partition) 
1. [Boot block, Super Block, Inode Table, Data Block](block)
1. [FAT, FAT32, exFAT, NTFS, ext family](FAT) 
1. [ File owner, attribute](FileOwner) 
1. [File Descriptor](Descriptor)
1. [File System vs DB](fdb)

# 파일 시스템
[전체적인 구조](https://m.blog.naver.com/PostView.nhn?blogId=gksgus092&logNo=221080297255&proxyReferer=https:%2F%2Fwww.google.com%2F)

[SSD의 구조 + FTL + 오버 프로비저닝](https://harryp.tistory.com/88)

```
파일 시스템 : 데이터를 효과적으로 관리 하기 위해 사용
구조 : 
데이터 영역 - 사용자가 생성한 파일 기록
메타영역 - 파일 관리를 위한 이름, 위치, 크기등
파일 시스템이 메타정보를 유지관리
```


# 조사해야할 내용
```
1. 데이터 저장의 역사: 자기테이프, 플로피디스크, HDD, SSD, SD Card, CF Card, UFS, CD, DVD —> Data Block으로 보인다., Disk/Disc
2. Layered Architecture: FTL
3. HOST Bus, Controller, Flash bus = 전송 규격, 제어 규격,
4. S/W FTL, eMMC, SD, NVMe, UFS
5. Sector와 Cluster, Slack - CHS 방식/LBA 방식
http://www.ktword.co.kr/abbr_view.php?nav=&m_temp1=4849&id=867
6. Volume과 Partitioning: format 과 mount, mount point
https://ko.wikipedia.org/wiki/%ED%8C%8C%EC%9D%BC%EC%8B%9C%EC%8A%A4%ED%85%9C_%EA%B3%84%EC%B8%B5%EA%B5%AC%EC%A1%B0_%ED%91%9C%EC%A4%80
7. MBR, BR/GPT: Primary partition과 Secondary partition, 한계
8. Boot block, Super Block, Inode Table, Data Block
https://www.youtube.com/watch?v=g53lSn44RNw
https://www.slashroot.in/understanding-file-system-superblock-linux
https://m.blog.naver.com/PostView.nhn?blogId=bitnang&logNo=70186410922&proxyReferer=https:%2F%2Fwww.google.com%2F
9. FAT, FAT32, exFAT, NTFS, ext family
http://blog.naver.com/PostView.nhn?blogId=huntae01&logNo=140010378985&parentCategoryNo=1&categoryNo=&viewDate=&isShowPopularPosts=true&from=search
https://www.remosoftware.com/info/kr/fat-32-exfat-ntfs-difference/
10. File owner, attribute
```

# 참고자료
```
MBR/GPT
https://texit.tistory.com/55
https://tinycorner.tistory.com/66
```

```
Volume과 partition
https://wiki.gentoo.org/wiki/LVM/ko
https://ko.wikipedia.org/wiki/%EB%B3%BC%EB%A5%A8_(%EC%BB%B4%ED%93%A8%ED%8C%85)
http://www.ktword.co.kr/abbr_view.php?m_temp1=4856
http://www.eniac-security.kro.kr/105
```

```
exFAT
https://docs.microsoft.com/en-us/windows/win32/fileio/exfat-specification
```

```
FTL 계층 구조
http://blog.skby.net/ftl-flash-translation-layer/
```