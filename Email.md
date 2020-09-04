# Email Protocols
```
MUA, MSA, MTA, MDA
Email Address, Email message format
SMTP, POP3, IMAP,  MAPI
```
![image](/uploads/9e62d3d901bf30225d7b9c872a0f03e0/image.png)


# MUA(Mail User Agent)
```
 - 사용자가 메일 송/수신을 위해 사용하는 클라이언트 프로그램
 - 메일을 작성하거나 메일함에 도착한 메일을 보여주는 기능을 수행한다.
 - 예. 아웃룩 익스프레스 등

Mail User Agent의 약자로 사용자가 E-mail을 읽고 답장하고 삭제할 수 있는 프로그램들을 말한다. 우리가 흔히 사용하는 Outlook Express(아웃룩)등의 클라이언트 프로그램을 일컫는다.
```

# SMTP
```
Simple Mail Transfer Protocol의 약자로 TCP/IP에서 E-mail을 전달시켜 주는 프로토콜을 말한다. 기본으로 TCP 25 포트를 사용한다.
PC에서 메일서버로 메일을 보낼때, 메일서버끼리 메일을 주고 받을때 사용된다.
일반적으로 POP3/IMAP과 같이 서버 사서함에 메시지를 저장하고 주기적으로 다운로드 할 수 있는 두가지 프로토콜 중 하나와 함께 사용한다.
```

# MSA(Mail Submission Agent)
```
MUA에서 메일을 수신하고 오류를 확인한 후 SMTP를 사용하여 동일한 서버에서 호스팅되는 MTA로 전송하는 서버 프로그램입니다.
```

# MTA(Mail Transport Agent)
```
 - (송신 시) 사용자로부터 메일을 전달받아서 외부로 전달해주는 프로그램
 - (수신 시)  외부로부터 MTA가 메일을 수신하면, 적절한 MDA에게 메일을 전달한다.
 - 예. sendmail, qmail 등

Mail Transport Agent의 약자로 MUA에서 작성되고 전송된 E-mail을 처리하는 우체국이라 할 수 있다. 우리가 배우고자 하는 메일서버가 바로  MTA에 해당한다.
그림에서 메일서버1, 메일서버2를 가리킨다.
```

# MDA(Mail Delivery Agent)
```
 - 사용자의 메일함으로 메일을 저장해주는 프로그램
 - 외부로부터 수신한 메일을 MTA가 MDA에게 전달해주면, MDA는 해당 사용자의 메일함에다가 저장한다.
 - 예. procmail 등

Mail Delivery Agent의 약자로 MUA에 의해서 전송된 E-mail을 MTA로부터 넘겨받아 다시 수신자가 MUA를 통해서 받기 전까지 
E-mail을 저장해 주거나 MUA로 전송해 주는 역할을 한다. 
그림에서 보여지진 않지만 daum.net 과 paran.com의 메일서버들은 계정사용자들에 대한 MDA를 가지고 있어 사용자들이 MUA를 이용해서
 메일을 받아가지 않는다면 이를 보관해둔다.

MDA로 사용되는 것이POP3, IMAP이다.
```

# MRA
```
 - 원격 서버에 있는 우편함으로부터 사용자의 MUA로 메시지를 가져오는 프로그램
```
![image](/uploads/113da2f2631d2f7faa98f48ee0920b12/image.png)

![image](/uploads/0f12dcae526b18be82dffd1d00bda21e/image.png)

![image](/uploads/4d6a726da6067f89bd5f9aba35e47a68/image.png)

![image](/uploads/4bfe54a8e239e98c3a0ae1422110a2c4/image.png)



# POP3
```
우리가 보통 알고 있는 받는 메일서버를 말한다. 
MTA에서 MDA로 전송된 E-mail을 수신하기 위한 데몬이 POP3나 IMAP 데몬이기 때문에 이런 이름이 붙었다.
최종적으로 MUA가 E-mail을 수신하기 전까지 E-mail의 내용을 가지고 있기 때문에 받는 메일서버라고 한다.

POP3 (Post Office Protocol 3)

이메일을 받아오는 표준프로토콜이다.

POP3는 인터넷 서버에서 이메일을 수신받을수 있는 client/server Protocol이다.

비동기화 방식, 주기적으로 서버의 메일박스를 체크하여 메일을 다운로드한다.

POP3는 서버에서 메일을 받아오는 즉시 삭제되도록 만들어졌지만 대부분의 MUA에서는 이를 방지하기위해 서버에 저장이되도록 설정을 할수 있다.

Store-and-forward

Port:110, 995(encryption)
```


# IMAP(Internet Message Access Protocol)
```
이메일을 받아오는 표준 프로토콜

IMAP은 인터넷 서버와 동기화되어 이메일을 열람할수 있다.  
이메일 전체에 대해 동기화 하는것이아니라 메일의 제목을 동기화 하여  사용자가 선택적으로 메일을 다운로드할 수 있다.

또한 서버측 편지함의 메시지의 다양한 상태플래그(읽음, 읽지 않음)을 표시할수도 있으며 사용자로부터 확실한 제거요청이 있기전 까지는 서버측 편지함에 저장된다.

Remote-fileserver

Port:143, 993(encryption)
```


# MAPI( Messaging Application Programming Interface )
```
Exchange 메일 서버와 Outlook에서 사용됨
IMAP과 거의 비슷하지만 더 많은 기능 제공

모든 데이터서버 및 데스트탑에 동일하게 저장되어 데이터 유실의 위험이 없음
```



![image](/uploads/4b6e5a6032b596f6c2ffffb2a78be831/image.png)

![image](/uploads/349e3349d583aa1ad9952a6251bb0311/image.png)


# Email Address
```
전자 메일 주소의 일반적인 형식은 local-part @ domain 이며 구체적인 예는 jsmith@example.com 입니다. 
```
![image](/uploads/7047e5418b9aae0526552f7ec8e55613/image.png)
![image](/uploads/614ce445aa20cdbdb47a5b0f4df8507d/image.png)
![image](/uploads/ce3c9e48a0a96971bdd9364b47472937/image.png)


#  Mail Message Format
```
메세지는 헤더,빈줄,바디로 구성 됨

```

![image](/uploads/b85502f59de425cec853b3a5ac2cca50/image.png)
