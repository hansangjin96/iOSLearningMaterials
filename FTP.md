```
history
기본 동작 - control connection, data connection, active mode vs passive mode, NAT traversal
Data type, File Structure, Data transfer mode
Login vs Anonymous FTP
FTPS, SFTP, FTP over SSH, TFTP, Simple File Transfer Protocol
```

# History
![image](/uploads/6022996d624b49203c04dd5ad8bee050/image.png)


# FTP (File Transfer Protocol)
```
인터넷을 통해 한 컴퓨터에서 다른 컴퓨터로 파일을 교환하기 위한 표준 프로토콜
IEFT RFC 959번에 정의되어 있음
프로토콜 TCP20,21번 포트를 사용
간단한 명령어를 통하여 FTP를 사용
Control Port를 통해 Telnet Session을 협상

TCP를 사용하여 네트워크의 FTP 서버와 클라이언트 시스템간에 파일을 업로드 및 다운로드하는 데 사용되는 프로토콜
응용 프로그램 계층에서 작동
서버에서 클라이언트 시스템으로 파일을 다운로드 할 수있을뿐 아니라 클라이언트 컴퓨터에서 서버로 파일을 업로드 할 수 있습니다. 
따라서 FTP는 양방향 시스템으로 간주됩니다.
```

![image](/uploads/6eda1957256db504e5f0589692590b83/image.png)


# 제어연결(Control Connection)
```
클라이언트에서 서버로의 명령과 서버의 응답을 위한 연결
21번 포트 사용
명령 또는 응답의 형태로 제어정보 전송
FTP세션동안 계속 연결상태 유지
```

# 데이터 연결(Data Connection)
```
파일이 전송될 때 생성되는 데이터 연결
20번 포트 사용
각 파일 전송때마다 설정되면 전송이 완료되면 폐쇄
```

# FTP 접속 방식
![image](/uploads/1196ede9e04f4cf90e6a4c263cb5a9b0/image.png)

![image](/uploads/e91645bc11a7742d0f8ed3e8103a6fe0/image.png)


# NAT and traversal
```
FTP에서 PORT명령을 보낸 뒤에 서버가 클라이언트로 다시 연결할 때 방화벽에 문제가 생길 수 있음
NAT의 경우 공용 IP주소가 아니라 내부 호스트 IP주소를 사용함

해결법
1) PASV명령을 사용하여 연결 -> 현대 FTP 클라이언트에서 주로 사용
2)  응용 프로그램 레벨 게이트웨이 를 사용하여 PORT 명령의 값을 변경
```


[Data type, File Structure, Data transfer mode](FTP2)