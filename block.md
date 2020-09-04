# Boot block, Super Block, Inode Table, Data Block 

[유닉스, 리눅스 파일 시스템 구조](https://m.blog.naver.com/gksgus092/221080447647)

![image](/uploads/e8c982fe545698274c5692c3d3f74a2a/image.png)

# Boot block
```
운영체제를 주기억장치에 올리는 역할을 하는 프로그램이 들어있는 영역으로, 윈도우 부트레코드와 유사함
```

# Super block
```
File System에 관한 전체적인 정보를 저장하는 Block
여러개가 있는 이유는 한 개의 슈퍼블록이 사라져서 못 쓰게 될 때 fsck 를 이용하여 복구 가능

파일시스템 Size, 매직넘버, 마운트 횟수, 블록그룹번호, 블록 크기, 첫 번째 inode 등
```

# Inode List 
````
inode 를 모아놓은 곳인데 한 블록에 여러개의 inode 를 저장하고 있다.
````

# inode (index inode) 
```
아이노드는 파일의 이름을 제외한 해당 파일의 모든 정보를 갖고 있다.
```

# Data block
````
실제로 데이터가 저장되는 블록
````

# Directory Block
```
파일 이름과 inode 번호를 저장한다.
```

# Indirection block
````
inode에 Data Block의 위치 정보를 저장할 공간이 부족할 때, 이 위치정보를 저장하기 위한
공간을 동적으로 할당하는데, 이 공간이 indirection block(간접블럭)
````
