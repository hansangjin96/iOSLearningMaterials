목차
```
1. Mark Up Language? 목적?
2. History & Versions
3. Key words
- Processor & Application
- Markup & content
- Tag
- Element
- Attribute
- Detecting Character Code 
- Comments
4. Well-formed, Schema, Validation, DTD
5. DOM, SAX
6. Binary XML
```

[참고블로그](http://tcpschool.com/xml/intro)

[참고 사이트](http://wiki.hash.kr/index.php/XML#.ED.99.9C.EC.9A.A9)

# Mark Up Language
```
'마크'또는 '태그'로 둘러싸인 언어
문서의 골격에 해당하는 부분을 작성

메타 데이터(meta data)란 데이터를 설명하는 데이터를 의미한다.
마크업 언어는 메타 언어중에서도 구분을 명료히 하는 언어다. 
마크업 언어는 위치 범위가 명확하다는 장점 때문에 메타 데이터를 표현할 때 아주 좋다
```

# Mark Down Language
```
마크업언어의 일종으로 읽기도 쓰기도 쉽다
```

# 마크업 언어 종류
![image](/uploads/8c94456170c8b7eb332106725248203a/image.png)

# HTML
```
하이퍼텍스트 마크업 언어(HyperText Markup Language)

HTML은 제목, 단락, 목록 등과 같은 본문을 위한 구조적 의미를 나타내는 것뿐만 아니라 
링크, 인용과 그 밖의 항목으로 구조적 문서를 만들 수 있는 방법을 제공한다. 
```
![image](/uploads/6774fd914d4398fa042d469c78d81aa1/image.png)

# XML이란
```
eXtensible Markup Language
HTML 과 비슷한 마크업 언어, 사람과 기계가 읽기 편한 구조

HTML -> 데이터를 보여주는 목적
XML -> 데이터를 저장하고 전달하는 목적
```

# History & Versions
```
XML은 SGML의 애플리케이션 프로파일이다.

동적 정보 표시를 위한 SGML의 다재다능함은 인터넷의 성장 이전인 1980년대 말에 초기 디지털 미디어 출판사들에 의해 인지되었다. 
1990년대 중순, 일부 SGML 실천자들은 당시 새로운 월드 와이드 웹을 경험하였고 웹이 성장할수록 마주칠 가능성이 있던 문제 중 일부를 SGML이 해결해줄 것이라 믿었다. 
댄 커널리는 1995년 당시 직원으로 있었을 때 SGML을 W3C의 활동 목록에 추가하였다. 
작업은 1996년 중순 썬 마이크로시스템즈의 엔지니어 존 보삭이 선언문을 만들고 협업자들을 모집하였을 때 시작되었다. 
보삭은 SGML과 웹에 모두 경험이 있는 사람들의 작은 공동체와 잘 어울렸다.

주요 디자인 결정은 1996년 7월과 11월 사이 도달했으며, 당시 XML 사양의 최초 워킹 드래프트가 출판되었다. 
추가 디자인 작업이 1997년에 계속되었으며 XML 1.0은 1998년 2월 10일 W3C 권고안이 되었다.
```
![image](/uploads/8d89d47b5e78c26e3ed52d397685aada/image.png)

![image](/uploads/3c5e6dfae738196c51298504b8380d15/image.png)

# XML 특징
```
1. 다른 목적의 마크업 언어를 만드는 데 사용되는 다목적 마크업 언어입니다.
2. 다른 시스템끼리 다양한 종류의 데이터를 손쉽게 교환할 수 있도록 해줍니다.
3. 새로운 태그를 만들어 추가해도 계속해서 동작하므로, 확장성이 좋습니다.
4. 데이터를 보여주지 않고, 데이터를 전달하고 저장하는 것만을 목적으로 합니다.
5. 텍스트 데이터 형식의 언어로 모든 XML 문서는 유니코드 문자로만 이루어집니다.
```

#  XML 선언(Declaration)
```
<?xml version="버전" encoding="문자 코드"?>

버전에 사용되는 XML버전을 기입, 주로 "1.0" 지정
문자코드는 UTF-8 or EUC-KR
```

# XML 구조
```
부모(parent) 요소는 여러 개의 자식(child) 요소를 가질 수 있습니다.
하지만 자식(child) 요소는 단 하나의 부모(parent) 요소만을 가집니다.

형제(sibling) 요소는 같은 트리 레벨(tree level)에 존재하는 요소를 가리킵니다.
```
![image](/uploads/806e0f822beb97cc309766b3afe2ceda/image.png)
![image](/uploads/34b99259183315e8fd5f02e72f8b64bb/image.png)]

# processor and application
```
프로세서는 마크업을 분석하고 구조화된 정보를 애플리케이션에 넘긴다. 
이 명세는 XML 프로세서가 무엇을 해야 하고 하지 말아야 하는지 제시하지만, 애플리케이션에 대해서는 다루지 않는다. 
이 프로세서(명세가 부르기를)는 흔히 XML parser라 불린다.
```

# markup and content
```
XML 문서를 구성하는 문자들은 마크업과 내용으로 나뉘는데, 그 구분은 간단한 문법 규칙으로 이루어진다. 
일반적으로 마크업을 구성하는 문자열은 문자 <로 시작하여 문자 >로 끝나거나, 문자 &로 시작하여 문자 ;로 끝나며, 마크업이 아닌 문자열은 내용이다. 
그러나, CDATA 절에서, 구분자 CDATA와 는 마크업으로 분류되고,그들 사이의 텍스트는 내용으로 구분된다. 
추가로, 가장 바깥 엘리먼트의 앞과 뒤의 공백(whitespace)은 마크업으로 분류된다.
```
![image](/uploads/a85133227298c7a45304bd9f94346e36/image.png)

# XML Tag
```
<로 시작하여 >로 끝나는 마크업 구조. 태그는 세 가지 종류가 있다.

시작 태그(start-tag); 예: <section>
끝 태그(end-tag); 예: </section>
빈 엘리먼트(empty-element) 태그; 예: <line-break />
```

# XML elements
```
문서의 논리 요소로서, 시작 태그로 시작하여 짝이 되는 끝 태그로 끝나거나, 빈 엘리먼트 태그만으로 이루어진다. 
시작 태그와 끝 태그 사이의 문자들은(있다면) 엘리먼트의 내용이고, 마크업을 포함할 수 있다. 
이 마크업은 자식 엘리먼트(child elements)라 부르는 다른 엘리먼트들을 포함할 수도 있다.
```
![image](/uploads/b17860de22c942881cc0b5b979106d2b/image.png)

# XML Attribute
```
XML 속성은 XML 요소에 대한 추가적인 정보를 제공해주며, 해당 요소의 특징을 정의합니다.

```
![image](/uploads/069d002cde1df7ba7e69b9e0a3762a37/image.png)
![image](/uploads/b394afd0888f8c6d7a6ca5703af8b2e6/image.png)

# Comments
```
주석은 XML 코드의 어느 부분에라도 작성할 수 있으며, 이러한 주석문은 XML 파서가 처리하지 않습니다.

XML의 주석은 <!--로 시작하여 -->로 끝납니다.
주석의 시작 태그(<!--)에는 느낌표(!)가 있지만 종료 태그(-->)에는 느낌표가 없습니다.
```

# Well-Formed
```
문법에 맞는(well-formed) XML 문서란 XML 문서로서 가져야 하는 최소한의 필수 요건을 충족한 XML 문서를 의미합니다.
따라서 이 문서는 XML의 모든 구문을 허용하지만, DTD(document type definition)나 스키마를 사용하지는 않습니다.

조건
1. 루트(root) 요소를 하나만 가져야 합니다.
2. 모든 XML 요소는 종료 태그를 가져야 합니다.
3. 시작 태그와 종료 태그에 사용된 태그 이름이 대소문자까지 완벽하게 일치해야 합니다.
4. 모든 XML 요소의 여닫는 순서가 반드시 정확하게 지켜져야 합니다.
5. 모든 속성의 속성값이 따옴표로 둘러싸여 있어야 합니다.
```

# Validation
```
유효한(valid) XML 문서는 문법에 맞는(well-formed) XML 문서를 좀 더 엄격하게 검증한 문서입니다.
따라서 유효한(valid) XML 문서는 모두 문법에 맞는(well-formed) XML 문서입니다.
거기에 추가하여 DTD(document type definition)를 가지고 있으며, 그에 따라 제대로 검증된 문서를 의미합니다.

XML에서 사용하는 DTD에는 다음과 같이 두 가지 종류가 있습니다.

1. DTD : 일반적인 문서 타입 정의(document type definition)
2. XML 스키마(XSD)
```

# DTD
```
문서 타입 정의(DTD)는 XML 문서의 구조 및 해당 문서에서 사용할 수 있는 적법한 요소와 속성을 정의합니다.

DTD는 엔티티를 정의할 수 있으며, 빠른 개발을 위한 내부 DTD를 사용할 수 있습니다.
DTD는 예전부터 사용해 온 구식 방법이지만, 특유의 장점을 바탕으로 아직도 널리 사용되고 있습니다.
```

# DTD 사용 목적
```
DTD를 사용하여 새로운 XML 문서의 구조를 정의함으로써 새로운 문서 타입을 만들 수 있습니다.
이렇게 생성된 DTD는 새로운 문서 타입을 이용한 데이터의 교환에서 표준으로써 활용됩니다.
또한, 응용 프로그램은 DTD의 정의에 따라 XML 문서의 구문 및 구조에 대한 유효성을 검사할 수 있습니다.
```
![image](/uploads/cdb1772331d0d184a56d968376d030fb/image.png)

![image](/uploads/9b609328bd31945947f2ff0ebf0d4292/image.png)

# Schema
```
XML 스키마의 특징

XML로 작성되었다.
XML 네임스페이스와 데이터 타입을 지원한다.
확장성을 가졌다.
```
![image](/uploads/174f42cea830198ab4c7917a2d889d1f/image.png)

![image](/uploads/3b8fc9b3990e896aec887a426e895546/image.png)
![image](/uploads/4e12c55f4963ab674cca76f21a7f96ed/image.png)
![image](/uploads/250a8832d5a5c90da02f4b74ca9f942b/image.png)

# DOM
```
DOM(Document Object Model)은 XML이나 HTML 문서에 접근하기 위한 API로 W3C 표준 권고안입니다.
DOM은 문서 내의 모든 요소를 정의하고, 해당 요소에 접근하는 방법까지 정의합니다.

DOM방식은 메모리에 모두 로드 후 파싱

1. 처음 XML문서를 메모리에 모두 로드한 후 값을 읽는다.
2. XML문서가 메모리에 모두 로드되어있기 때문에 노드의 검색, 수정, 구조변경등이 빠르고 용이하다.
3. 직관적이고 SAX보다 파싱하기 단순하다.




XML 문서가 전부 메모리로 올라가 객체 모델로 만들어진다. 
W3C의 공식 표준이며, W3C가 표준화한 API들의 기반이다. 
문서가 통째로 메모리에 올라가 조직화하기 때문에 문서 요소를 임의로 접근하고 사용하기에 용이하다. 
그러나 이는 반대로 단점이 되기도 하는데, 논리 구조를 통째로 메모리에 올려놓고 연산하기 때문에 
XML 데이터의 양이 많으면 메모리 부족으로 인해 고생하게 된다.
```
![image](/uploads/00f6a65a4fcde92d4090e24afbbb55bd/image.png)

# SAX
```
SAX는 순차적으로 읽어가며 파싱하는 것
SAX 방식은 XML 문서를 하나의 긴 문자열로 간주한다.

1. XML문서를 순차적으로 읽어들이면서 노드가 열리고 닫히는 과정에서 이벤트가 발생한다.
2. XML문서를 메모리에 전부 로딩하고 파싱하는것이 아니라서 메모리 사용량이 적고 단순히 읽기만 할 때 속도가 빠름.
3. 발생한 이벤트를 핸들링하여 변수에 저장,활용하는 것이기 때문에 복잡하고, 노드 수정이 어렵다.
4. DOM보다 어렵다.




XML 문서를 애플리케이션에서 사용하기 위한 API. DOM과 비교해 저수준의 인터페이스를 가지고 있으며 처리해야 할 파일이 클 때 적합하다. 
XML의 구조에 따라 이벤트가 발생하며, 프로그래머는 이 이벤트를 처리하는 이벤트 핸들러를 작성하여 필요한 데이터를 추출할 수 있다. 
이러한 이유로 데이터 내용을 조직하는 기능은 DOM만 못하다. 
XML 문서를 통으로 메모리상에 논리 구조를 유지하면서 올리고 작업할 수 없기 때문이다. 
그러나 이러한 이벤트 기반 처리 방식은 역시 읽어서 처리해야 하는 XML 데이터가 매우 클 때 장점으로 발휘한다. 
일단 어떻게든 다른 대용량 비휘발성 저장공간(데이터베이스, NoSQL 등)에 입력하는 데 SAX를 쓰고, 데이터 조작은 해당 저장공간에서 하면 되기 때문이다.
```
![image](/uploads/1fbb5cb0af4399cfc9ddfd79d1214a8e/image.png)

# Binary XML
```
요약
이진 XML 스펙은 Extensible Dynamic Binary XML DB2 클라이언트 / 서버 이진 XML 형식 (XDBX)을 설명합니다.

내용
이진 XML 형식은 XML 값의 외부 표현으로, 클라이언트와 데이터 서버 간의 XML 데이터 교환에 사용할 수 있습니다. 
이진 표현은 효율적인 XML 구문 분석을 제공하므로 XML 데이터 교환에 대한 성능이 향상 될 수 있습니다. 

이진 XML 형식을 사용하면 일반적으로 XML 문서의 상세도가 줄어들어 구문 분석 비용이 줄어들지 만 일반 텍스트 편집기 및 타사 도구를 사용하여 문서를보고 편집 할 수 없습니다. 
```

[인터넷 프로토콜](restapi)