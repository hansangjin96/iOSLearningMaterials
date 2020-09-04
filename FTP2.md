```
Data type, File Structure, Data transfer mode
Login vs Anonymous FTP
FTPS, SFTP, FTP over SSH, TFTP, Simple File Transfer Protocol
```

# Data type
```
ASCII (TYPE A) : 텍스트에 사용됩니다.
이미지 (유형 I, 일반적으로 이진 모드 라고 함 ) : 송신 시스템은 각 파일을 바이트 단위 로 전송 하고 수신자는 바이트 스트림 을 수신 할 때이를 저장 합니다. 
EBCDIC (TYPE E) : EBCDIC 문자 세트를 사용하는 호스트 간의 일반 텍스트에 사용됩니다.
로컬 (TYPE L n ) : 8 비트 바이트를 사용하지 않는 시스템 간의 파일 전송 (예 : DEC PDP-10 과 같은 36 비트 시스템 )을 지원하도록 설계되었습니다 . 
```

# File Structure(RFC959의 3.1.1 섹션에 정의)
```
파일 구성은 STRU 명령을 사용하여 지정됩니다.

F 또는 FILE 구조 (스트림 지향) 파일은 임의의 바이트, 문자 또는 단어 시퀀스로 간주
R 또는 RECORD 구조 (레코드 지향). 파일은 고정 또는 가변 길이 일 수있는 레코드로 분할 된 것으로 간주
P 또는 PAGE 구조 (페이지 지향). 파일은 데이터 또는 메타 데이터를 포함 할 수있는 페이지로 나뉨

대부분의 최신 FTP 클라이언트 및 서버는 STRU F 만 지원
```

# Data Transfer Mode
```
스트림 모드 (MODE S) : 데이터가 연속 스트림으로 전송되므로 FTP가 처리하지 않아도됩니다.
블록 모드 (MODE B) : 스트림 지향 (STRU F) 텍스트 파일을 전송하는 데 사용될 수도 있지만 주로 레코드 지향 파일 (STRU R)을 전송하기 위해 설계되었습니다. 
압축 모드 (MODE C) : 실행 길이 인코딩을 사용하여 데이터 압축으로 MODE B를 확장 합니다.
```

# Login
```
FTP 로그인은 일반 사용자 이름과 비밀번호 체계를 사용하여 액세스 권한을 부여
USER 명령을 사용하여 서버로 전송되고 암호는 PASS 명령을 사용하여 전송
```

# Anonymous FTP
```
호스트는 익명 FTP 액세스를 제공 할 수 있습니다. 

```

[FTPS, SFTP, FTP over SSH, TFTP, Simple File Transfer Protocol](FTP3)