# 서버의 이해
#web Mar 20, 2023 2:06 PM
## 1. IP와 도메인은 무엇일까?
IP는 네트워크에 접속되어 있는 컴퓨터의 주소가 숫자로 표현된 것이다. 도메인은 직관적으로 알기 어려운 IP를 문자열로 바꾼 형태를 말한다.

## 2. 클라이언트와 서버는 무엇일까요?
클라이언트는 ‘고객, 의뢰인’으로 흔히 옮겨지듯 무언가를 제공받는 입장을 나타내는데, 웹의 경우에는 컴퓨터가 여기에 해당할 것이다. 웹페이지가 그 내용이 될 것이다. 초창기에는 텍스트가 그 중심이었지만, 점점 웹에서 제공받는 내용은 각종 미디어 자료를 비롯한 다양한 형식으로 확장되었다.
어떤 것을 제공해주는 주체를 서버라고 부른다. 인터넷의 경우 클라이언트가 요청한 내용을 확인하고 그에 대응하는 정보를 전송하여 제공한다. 요청 내용의 적합성에 따라 ‘404 Not Found’와 같은 오류를 반환하기도 하고, HTTP 프로토콜을 통해 다양한 형식의 정보를 전달한다.

## 3. 정적 웹사이트와 동적 웹사이트의 차이점은 무엇일까요? Django는 무엇을 위한 도구인가요?
하이퍼텍스트로만 구성된, 이를테면 HTML과 CSS만으로 구성된 웹페이지는 대부분 정적 웹페이지로 볼 수 있을 것이다. 서버에 구축되어 있는 정보를 소비만 할 수 있는 것이 아니라, 이용자가 정보를 제공하거나 인증을 주고받는 상호작용이 가능한 서비스는 동적 웹사이트에서 구현될 수 있다.
django는 파이썬으로 짜놓은 프로그램을 이용한 웹서비스를 손쉽게 구축할 수 있도록 구성된 프레임워크이다. 서버 구축이나 보안 등의 문제를 간편하게 해결하고 내용에 집중할 수 있도록 도움을 준다.

## 4. HTTP는 무엇이고 요청과 응답 메시지 구성은 어떻게 되나요?
HTTP는 클라이언트와 서버가 통신할 수 있도록 만들어진 프로토콜(약속)이다. HTTP/1.1(1997), HTTP/2(2015), HTTP/3(2022)가 현재 표준으로 사용되고 있다.
* 클라이언트 요청 메시지 예시
```
GET / HTTP/1.1
Host: www.example.com
User-Agent: Mozilla/5.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: en-GB,en;q=0.5
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
* 서버 응답 메시지 예시
```
HTTP/1.1 200 OK
Date: Mon, 23 May 2005 22:38:34 GMT
Content-Type: text/html; charset=UTF-8
Content-Length: 155
Last-Modified: Wed, 08 Jan 2003 23:11:55 GMT
Server: Apache/1.3.3.7 (Unix) (Red-Hat/Linux)
ETag: "3f80f-1b6-3e1cb03b"
Accept-Ranges: bytes
Connection: close

<html>
  <head>
    <title>An Example Page</title>
  </head>
  <body>
    <p>Hello World, this is a very simple HTML document.</p>
  </body>
</html>
```

## 5. 프레임워크는 무엇일까요?
웹서비스와 관련된 프레임워크를 많이 보게 되는데, 프레임워크는 순수한 프로그래밍 언어로 짜인 프로그램을 웹 상에서 구현할 수 있도록 웹서비스에 필요한 많은 요소들을 미리 준비해놓은 틀이라고 할 수 있다. 서비스 제공자는 이 미리 만들어진 틀에 자신의 프로그램을 배치하고 각종 설정값을 조정해서 원하는 서비스를 구축하게 된다.

