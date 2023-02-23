---
title : HTML 기본
excerpt : 패스트캠퍼스 코딩 레벨원 - MBTI 테스트 만들며 배우는 왕초보 코딩
categories : coding
---

<br>

## HTML : Hyper Text Markup Language  
- 웹의 구조를 담당  
  - 얼굴을 만들 때 필요한 구조는 눈, 코, 입, 귀

- index.html 파일 사용  
  - 다른 html파일 만들기 전에 기본적으로 있어야 함  
  - ! + tab하면 기본 설정이 뜸  

<br>

## HTML의 기본 형식
- 기본적으로 태그는 열고 닫혀야함  
  - <태그 속성 = "값">내용</태그>
    ```html
    <h1 class = "title">Hello World!</h1>
    ```

- 빈 태그 : 열리고 닫히지 않고 시작 태그만 존재
  - <태그>
  - <태그 속성="값"/> 끝에 /를 붙여서 빈태그가 종료되었다는 것을 표시
    ```html
    <img src="이미지 파일"/>
    ```

<br>

- Block Elements : 레이아웃을 만들기 위한 요소  
  - 크기를 지정할 수 있음, 크기 미지정 시 가로너비는 최대, 세로너비는 최소 지향  
    - div, h1, h2, p, ul, header, etc  

- Inline Elements : 글자를 만들기 위한 요소  
  - 크기 지정이 불가능함, 가로너비 & 세로너비 최소 지향
    - span, a, etc

<br>

## HTML의 구체적 구성요소
```html
<!DOCTYPE html> 
<html lang="ko">   <!-- 사이트의 메인 언어 설정 -->
<head> <!-- html의 정보 표현 -->
  <meta charset="UTF-8">   <!-- 기본 문자인코딩 -->
  <meta http-equiv="X-UA-Compatible" content="IE=edge"> <!-- MS의 IE와 edge 관련 명령어, 없어도 무방 -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
  <!-- viewport는 모바일을 뜻함, 모바일에서 사이트가 어떻게 출력될지 설정, 
  1.0이면 확대축소가 되어있지 않음, 모바일에서 볼 필요가 없다면 제거 가능 -->
  <title>Document</title>
  <link rel="stylesheet" href="./main.css"> 
  <!-- link를 적고 tab을 누르면 자동완성, href에 link할 파일 기입, css파일을 html에 연결 -->
  <script defer src="./main.js"></script> <!-- js파일을 html에 연결 -->
</head>
<body>  <!-- html의 구조 표현 -->
  <a href="/about.html"> <!-- anchor 다른 페이지로 이동하는 버튼 -->
    About?!
  </a> <!-- 사이트에서 About?!이라고 적힌 버튼을 누르면  about.html파일로 이동 -->
  <div> <!-- li 요소의 조상 요소 -->
    <ul class="fruits"> <!-- li 요소의 부모 요소 -->
      <li>Apple</li> <!-- li는 태그, 이 줄 전체가 한 요소, ul 요소의 자식 요소, div 요소의 후손 요소 -->
    </ul>
  </div>
  <div>
    <h1>Hello1</h1> <!-- heading 제목 -->
    <h2>Hello2</h2>
    <h3>Hello3</h3>
    <h4>Hello4</h4>
    <h5>Hello5</h5>
    <h6>Hello6</h6>
  </div>
  <div class="이름"> <!-- 요소에 별명 짓기, CSS에서 refer하는 명칭이 됨 = 선택자 -->
    <ul> <!-- unordered list 순서가 없는 목록 -->
      <li>Apple</li> <!-- list item 목록의 항목 -->
      <li>Banana</li>
    </ul>
  </div>
  <div>
    <img src="source 경로" alt="이미지 이름">
    <span>이 안의 글자 서식 설정</span>
  </div>
</body>
</html>
```

<br>