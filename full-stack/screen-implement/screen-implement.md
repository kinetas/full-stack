# 화면 구현
서버server(물리) : 제공하다 / service(논리)제공하는 주체  
클라이언트client : 요청하는 주체  
- Web Browser(80) <--> web service(html)
네트워크Network : 서버와 클라이언트를 연결  
IP : 네트워크 환경 상 주소  
포트별 서비스 제공  

## 웹서비스 구현

---

### HTML

Hyper Text Markup Language  
Hyper Text는 여러 텍스트 페이지들을 링크같은 것들을 통해 이동할 수 있는 것  
Markup &lt;h1&gt; 같은 것들  
프로토콜 : 통신을 위한 프로그램(http)  
Request : 요청  
Response : 수신  

구조를 만들 때 사용  
#### Markup Language
시작태그와 종료태그가 필요  
<태그명> </태그명>  
으로해야함  
<태그명 속성=값> 으로도 할 수 있음  
태그는 부모태그와 자식태그가 있음  
practice.html 주석참고  

---

#### Basic

<!DOCTYPE html>     :   이 문서가 HTML5 문서임을 선언    
        <html lang="ko">    :   HTML문서의 시작을 나타내며  lang 속성을 이용하여 문서의 기본언어가 한국어임을 명시
        <head>              :   문서의 메타데이터와 제목등을 포함하는 머리말
        <meta charset="UTF-8"> : 문서의 문자 인코딩을 UTF-8 으로 설정
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        : 반응형 웹 디자인을 위한 뷰포트 설정
        : width=device-width : 뷰포트의 너비를 디바이스의 너비만큼 설정   
        : initial-scale=1.0 : 페이지가 처음 로드될때 기본 확대/축소 수준을 지정 
        <title>Document</title>                    
        <body>              :   문서의 본문, 브라우저에 ViewPort(웹페이지를 사용자가 보는영역)에 표시되는 내용 
        
---

### CSS
스타일링  

---

### JavaScript
동적 처리(브라우저의 기능 사용)-객체지향문법  
