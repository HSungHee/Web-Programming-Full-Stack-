
# 1. 웹 프로그래밍 기초
========================================

# 1.1 웹의 동작 (HTTP 프로토콜 이해)

## 인터넷 (Internet)

TCP/IP 기반의 네트워크가 전세계적으로 확대되어 하나로 연결된 네트워크들의 네트워크 (네트워크의 결합체)

## HTTP (Hypertext Transfer Protocol)란?

* 팀 버너스리(Tim Berners-Lee)와 그가 속한 팀은 CERN에서 HTML뿐만 아니라 웹 브라우저 및 웹 브라우저 관련 기술과 HTTP를 발명하였습니다.
* 문서화된 최초의 HTTP버전은 HTTP v0.9(1991년)입니다.
* HTTP는 서버와 클라이언트가 인터넷상에서 데이터를 주고받기 위한 프로토콜(protocol)입니다.
* HTTP는 계속 발전하여 HTTP/2까지 버전이 등장한 상태입니다.

### HTTP 작동방식

클라이언트가 먼저 서버에게 요청을하고, 서버는 클라이언트에게 응답을 보냅니다. 

* HTTP는 서버/클라이언트 모델을 따릅니다.
* 장점
  - 불특정 다수를 대상으로 하는 서비스에는 적합하다.
  - 클라이언트와 서버가 계속 연결된 형태가 아니기 때문에 클라이언트와 서버 간의 최대 연결 수보다 훨씬 많은 요청과 응답을 처리할 수 있다.
* 단점
  - 연결을 끊어버리기 때문에, 클라이언트의 이전 상황을 알 수가 없다.
  - 이러한 특징을 무상태(Stateless)라고 말한다.
  - 이러한 특징 때문에 정보를 유지하기 위해서 Cookie와 같은 기술이 등장하게 되었다.

### URL (Uniform Resource Locator)

접근 프로토콜://IP 주소 또는 도메인 이름/문서의 경로/문서이름 (e.g. http://www.sunnyvale.co.kr/docs/index.html)

* 인터넷 상의 자원의 위치
* 특정 웹 서버의 특정 파일에 접근하기 위한 경로 혹은 주소

### HTTP (Hypertext Transfer Protocol)

1. connect (Client -> Server)
2. request (Client -> Server)
3. response (Server -> Client)
4. close (Client -> Server)

* 요청 메서드 : GET, PUT, POST, PUSH, OPTIONS 등의 요청 방식이 온다.
* 요청 URI : 요청하는 자원의 위치를 명시한다.
* HTTP 프로토콜 버전 : 웹 브라우저가 사용하는 프로토콜 버전이다.
첫번째 줄의 요청메소드는 서버에게 요청의 종류를 알려주기 위해서 사용됩니다.

각각의 메소드 이름은 다음과 같은 의미를 가집니다.

참고로 최초의 웹 서버는 GET방식만 지원해줬습니다.

* GET : 정보를 요청하기 위해서 사용한다. (SELECT)
* POST : 정보를 밀어넣기 위해서 사용한다. (INSERT)
* PUT : 정보를 업데이트하기 위해서 사용한다. (UPDATE)
* DELETE : 정보를 삭제하기 위해서 사용한다. (DELETE)
* HEAD : (HTTP)헤더 정보만 요청한다. 해당 자원이 존재하는지 혹은 서버에 문제가 없는지를 확인하기 위해서 사용한다.
* OPTIONS : 웹서버가 지원하는 메서드의 종류를 요청한다.
* TRACE : 클라이언트의 요청을 그대로 반환한다. 예컨데 echo 서비스로 서버 상태를 확인하기 위한 목적으로 주로 사용한다.

## 참고 자료
HTTP, 위키백과 - https://ko.wikipedia.org/wiki/HTTP


# 1.2 웹 Front-End와 웹 Back-End

## 1.2.1 웹 Front-end

### 웹 Front-end?
사용자에게 웹을 통해 다양한 콘텐츠(문서, 동영상, 사진 등)를 제공합니다.

또한, 사용자의 요청(요구사항)에 반응해서 동작합니다.

### 웹 Front-end의 역할

웹콘텐츠를 잘 보여주기 위해 구조를 만들어야 합니다.(신문,책등과 같이) - HTML

적절한 배치와 일관된 디자인 등을 제공해야 합니다.(보기 좋게) - CSS

사용자 요청을 잘 반영해야 합니다.(소통하듯이) - Javascript


### * HTML 

원하는 문서의 구조를 프로그래밍 언어로 표현해야 합니다.

HTML이라는 것은 그 구조를 잘 표현해 줍니다.

### * 스타일 - CSS

웹페이지를 꾸미기 위해서는 각각의 HTML 태그(문서의 구조를 표현한 각 조각 단위)를 꾸미기 위한 규칙이 필요합니다

CSS는 이를 표현할 수 있는 프로그래밍 언어입니다.

### * 동작 - JavaScript

HTML,CSS를 이리저리 움직이고 변경할 필요가 있을 거예요.

JavaScript가 그걸 해줍니다.

## 1.2.2 웹 Back-end

### 백 엔드(Back-End)란?

backend는 정보를 처리하고 저장하며, 요청에 따라 정보를 내려주는 역할을 한다. 가령 쇼핑몰이라면, 상품 정보를 가지고 있고, 주문을 받아서 저장하고, 사용자가 관심있어 하는 상품을 골라주는 역할이 back-End의 역할이다

### 백 엔드 개발자가 알아야 할 것들

* 프로그래밍 언어(JAVA,  Python, PHP, Javascript 등)
* 웹의 동작 원리
* 알고리즘(algorithm), 자료구조 등 프로그래밍 기반 지식
* 운영체제, 네트워크 등에 대한 이해
* 프레임워크에 대한 이해(예: Spring)
* DBMS에 대한 이해와 사용방법(예: MySQL, Oracle 등)

## 참고 자료
웹프론트엔드 역할 쉽게 알아보기 - https://html-css-js.com/


# 1.3 Browser의 동작

## Browser

서버에서 전송한 데이터(HTML과 같은)가 클라이언트에 도착해야 할 곳은 'Browser'입니다.

Browser에는 데이터를 해석해주는 파서와 데이터를 화면에 표현해주는 렌더링엔진이 포함되어 있습니다.

이런 작업의 대부분은 브라우저 내부에서 이뤄지기 때문에 반드시 알아야 하는 것은 아닙니다. 하지만 브라우저의 내부를 이해하면 웹 개발을 하면서 맞닥뜨리는 난해한 문제를 해결할 수 있고, 보다 최적화된 웹개발을 할 수 있습니다.

브라우저는 월드와이드웹(WWW)에서 정보를 검색, 표현하고 탐색하기 위한 소프트웨어입니다.

인터넷에서 특정 정보로 이동할 수 있는 주소 입력창이 있고 서버와 HTTP로 정보를 주고 받을 수 있는 네트워크 모듈도 포함하고 있습니다.

그리고 서버에서 받은 문서(HTML, CSS, Javascript)를 해석하고 실행하여 화면에 표현하기 위한 해석기(Parser)들을 가지고 있습니다.

브라우저마다 서로 다른 엔진을 포함하고 있습니다.

## 참고 자료
사파리 브라우저에서 처리되는 webkit렌더링엔진의 처리과정 - https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/

How Browsers Work: Behind the scenes of modern web browsers - https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/


# 1.4 Browser에서의 웹 개발

## HTML 문서구조

뜯어보자 웹사이트!

    1. 먼저 크롬브라우저가 없다면 설치하기
    2. 크롬 브라우저를 열고 크롬 개발자도구 열기
    3. 윈도우 (Ctrl + Shift + I)
       맥(Option + Command + i)
    4. 접속 : http://www.amazon.com


## 알게 된 몇 가지 특징

    * HTML문서는 html이라는 태그로 시작해서 html태그로 끝납니다.
    * head는 무엇을 하는 걸까요? html 문서의 추가적인 설명을 담고있다
    * body는 무엇을 하는 걸까요? 화면에 표현될 <div> 등을 포함
    * HTML은 계층적입니다.
    * HTML은 tag를 사용해서 표현합니다.

```
<tag class="title">안녕하세요</tag>
```

JavaScript와 CSS가 html 안에 여기저기 존재합니다.

```
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>저를소개해요</title>
    <link rel="stylesheet" href="css/style.css">
    <script src="js/start.js"></script>
  </head>
  <body>
    <h1>안녕하세요</h1>
    <div>코드스쿼드 크롱이라고 합니다</div>
    <script src="js/library.js"></script>
    <script src="js/main.js"></script>
  </body>
  <script>
    console.log("javascript code...");
  </script>
</html>
```

JavaScript 코드는 body 태그 닫히기 전에 위치하는 것이 렌더링을 방해하지 않아도 좋고, css코드는 head 안에 위치해서 렌더링 처리 시에 브라우저가 더 빨리 참고할 수 있게 하는 것이 좋습니다.

## 참고 자료
웹에서 html, css, javascript를 쉽게 테스트할 수 있는 웹사이트 - http://jsbin.com/?html,output


# 1.5 웹서버

웹 브라우저를 실행한 후 주소 입력창에 URL 주소를 입력하면, 그 URL주소에 해당하는 결과물이 화면에 보입니다.

우리가 현실에서 주소를 보고 집을 찾아가는 것처럼, 웹 브라우저는 URL 주소에 해당하는 웹서버(Web Server)에 연결하고, 해당 주소에서 볼 수 있는 내용을 읽어 들여 보여주게 됩니다.

## 웹 서버란?

* 웹 서버는 소프트웨어(Software)를 보통 말하지만, 웹 서버 소프트웨어가 동작하는 컴퓨터를 말합니다.
* 웹 서버의 가장 중요한 기능은 클라이언트(Client)가 요청하는 HTML 문서나 각종 리소스(Resource)를 전달하는 것입니다.
* 웹 브라우저나 웹 크롤러가 요청하는 리소스는 컴퓨터에 저장된 정적(static)인 데이터이거나 동적인 결과가 될 수 있습니다.
 
## 웹 크롤러

네이버나 구글 같은 검색 사이트에서 다른 웹사이트 정보를 읽어나갈 때 사용하는 소프트웨어

## 웹 서버 소프트웨어의 종류

* 가장 많이 사용하는 웹 서버는 Apache, Nginx, Microsoft IIS
* Apache웹 서버는 Apache Software Foundation에서 개발한 웹서버로 오픈소스 소프트웨어(Open-sourceSoftware)이며, 거의 대부분 운영체제에서 설치 및 사용을 할 수 있습니다.
* Nginx는 차세대 웹서버로 불리며 더 적은 자원으로 더 빠르게 데이터를 서비스하는 것을 목적으로 만들어진 서버이며   Apache웹 서버와 마찬가지로 오픈소스 소프트웨어입니다.

## 참고 자료
웹서버, 위키백과 - https://ko.wikipedia.org/wiki/%EC%9B%B9_%EC%84%9C%EB%B2%84

Apache HTTP Server Project - https://httpd.apache.org/

nginx - https://nginx.org/en/


# 1.6 WAS (Web Application Server)

## 클라이언트/서버 구조

클라이언트(Client)는 서비스(Service)를 제공하는 서버(Server)에게 정보를 요청하여 응답 받은 결과를 사용합니다.

## DBMS (DataBase Management System)

다수의 사용자가 데이터베이스 내의 데이터에 접근할 수 있도록 해주는 소프트웨어입니다.

## 미들웨어 (MiddleWare)

클라이언트 쪽에 비즈니스 로직이 많을 경우, 클라이언트 관리(배포 등)로 인해 비용이 많이 발생하는 문제가 있습니다.

비즈니스 로직을 클라이언트와 DBMS사이의 미들웨어 서버에서 동작하도록 함으로써 클라이언트는 입력과 출력만 담당하도록 합니다.

## WAS (Web Application Server)
WAS는 일종의 미들웨어로 웹 클라이언트(보통 웹 브라우저)의 요청 중 웹 애플리케이션이 동작하도록 지원하는 목적을 가집니다.

### WAS가 가지는 3가지 기본 기능
    1. 프로그램 실행 환경과 데이터베이스 접속 기능 제공
    2. 여러 개의 트랜잭션(논리적인 작업단위) 관리
    3. 업무를 처리하는 비즈니스 로직을 수행

### 웹 서버 vs WAS
    * WAS도 보통 자체적으로 웹 서버 기능을 내장하고 있습니다.
    * 현재는 WAS가 가지고 있는 웹 서버도 정적인 콘텐츠를 처리하는 데 있어서 성능상 큰 차이가 없습니다.
    * 규모가 커질수록 웹 서버와 WAS를 분리합니다. 그 목적은 장애 극복 기능(failover)인 경우가 많다. 
    * 자원 이용의 효율성 및 장애 극복, 배포 및 유지보수의 편의성을 위해 웹서버와 WAS를 대체로 분리합니다.


