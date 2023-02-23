---
title : CSS 기본
excerpt : 패스트캠퍼스 코딩 레벨원 - MBTI 테스트 만들며 배우는 왕초보 코딩
categories : coding
---

<br>

## CSS : Cascading Style Sheets
- 컨텐츠를 꾸며주는 시각적인 표현 담당 (정적)
  - 얼굴에 눈, 코, 입, 귀를 적절하게 배치
  
- main.css을 기본 파일로 사용

<br>

## 개발자도구 사용
- 개발자도구 F12를 이용해서 각 코드가 어디에 적용되었는지 하이라이트되어 알 수 있음  
- 개발자도구를 통해 실시간으로 CSS를 작성하며 변경사항을 확인할 수 있고 그 후 실제 CSS파일에 복붙할 수도 있음

<br>

## CSS의 구체적 구성요소
- 선택자는 refer하는 명칭
  - 선택자 {속성:값; 속성:값;}  
  ```css
  h1{color: red; font-size: 30px;}
   ```
- .이름 + tab : 해당 이름의 css 선택자를 html 파일에 생성 가능
  ```html
  .name + tab
  <div name=""></div>
  ```

```css
/* 선택자 이용 */
li{ 
   color : red;
   font-size: 20px;
} /* 태그 선택자 : html 태그 이름을 선택 */

.orange{ 
   color: blue;
   font-size: 40px;
} /* 클래스 선택자 : html class 속성을 선택, 태그와 무관, 태그 선택자보다 우선 */

div .orange {
   color: red;
} /* 하위(후손) 선택자 : html의 하위 요소 선택, div 띄어쓰기 class해야함, 
ex. div 요소의 후손 중 orange 클래스를 가진 요소 */

.apple:hover {
   color: purple;
} /* 가상 클래스 hover : html 요소에 마우스 커서가 올라가 있는 동안만 선택, 
ex. li 태그에 hover할 때 보라색으로 표시*/

.strawberry:active {
   color: skyblue;
} /* 가상 클래스 active : html 요소에 마우스를 클릭하고 있는 동안만 선택 */


/* CSS 속성 정리 */
/* Box Models : html 요소의 형태를 만듦*/
.container { /* container 클래스 꾸미기 */
   background-color: orange;
   height: 400px;
   padding-top: 30px;
   padding-left: 30px; /* 요소의 내부에 여백 생성, 추가된 여백만큼 크기가 늘어남 */
   width: 700px;
   border: 4px solid black;
} 

.item { /* item 클래스 꾸미기 */
   background-color: royalblue;
   width: 130px; /* 미지정시 부모 요소인 container 클래스의 크기가 최대값 */
   height: 100px;
   min-width: 50px; /* 최소 가로 너비 */
   max-width: 150px; /* 최대 가로 너비 */
   margin-bottom: 30px; /* 요소의 외부에 여백 생성 */
   padding-top: 30px; /* 내부에 여백이 생성되어 item의 총 height가 130px이 됨 */
   border: 4px solid yellow; /* 선의 굵기, 종류, 색상 정의 */
   border-radius: 10px; /* 모서리 둥글게 만들기 */
   box-shadow: 10px 10px 10px rgba(0,0,0,0.5); /* 그림자 생성 : x축 이동, y축 이동, blur 효과 정도, 색상(r,g,b,투명도) */
}

/* Fonts, Texts : html 요소의 글자를 꾸밈 */
.anthem {
   font-size: 50px; /* 16px이 기본 */
    font-weight: 700; /* 글자 굵기, 400이 기본 */
    font-family: sans-serif; /* 글꼴,sans-serif이 기본 */
    line-height: 1.3; /* 1이 기본 */
    text-align: center; /* 글자 정렬 */
    color: greenyellow;
    text-decoration: underline; /* 글자 추가로 꾸미기 */
    word-break: keep-all; /* 띄어쓰기를 기준으로 줄바꿈 */
}

/* Backgrounds : html 요소의 배경 색상이나 이미지 추가 */
.container {
   background-image: url("https://picsum.photos/200/300");
   background-size: 100px; /* 배경 이미지 사이즈 */
   background-repeat: no-repeat; /* 사진이 반복되지 않고 한번만 나오게 설정 */
   background-position: center center; /* container 클래스 안에서 이미지가 어디에 위치할지 지정 */
}

/* Positions : html 요소의 위치를 지정 */

/* Flexible boxes, Flex : html 요소들을 수평 혹은 수직으로 정렬 */
.container {
   display: flex; /* 수직을 수평으로 정렬, 부모요소에 추가하면 자식요소가 수평으로 정렬 */
   justify-content: center; /* item 요소들이 좌우 기준으로 중앙 정렬, start/center/end 중 설정 */
   align-items: end; /* item 요소들이 상하 기준으로 중앙 정렬, start/center/end 중 설정 */
   gap: 30px; /* 수평인 item 사이에 gap을 만듦 */
}

.container .item {
   display: flex;
   justify-content: center;
   align-items: center; /* padding-top이 설정되어 있어서 글자가 밑으로 밀려서 보임 */
   color: white;
   font-size: 30px;
}

/* Transitions : html 요소의 이전과 이후 상태를 애니메이션으로 처리해서 자연스럽게 움직임 */
.container .item{
   transition: 1s; /* item이 hover로 인해 변환될때 1초 지연 */
}

.container .item:hover{
   transform: 
   rotate(45deg);
   background-color: pink;
   border-radius: 50%;
}

/* Transforms : html 요소에 회전, 비율, 기울이기, 등 효과 추가 */
.container .item {
   transform: 
   translateX(50px) 
   translateY(50px) 
   rotate(90deg) 
   scale(2); 
   /* 오른쪽으로 50px 이동, 아래쪽으로 50px 이동, 90도 회전, 2배크기로 만들기, 이들을 모두 변환함수라고 칭함 */
}

/* Flotations : html 요소를 글자 위에 띄움 */

/* Animations : html 요소에 애니메이션 추가, transitions 보다 복잡하게 이용 가능 */

/* Grid : html 요소들의 레이아웃을 손쉽게 지정 */

/* Columns : html 요소의 문장을 마치 신문처럼 여러 단으로 배치 */

/* Filters : html 요소에 흐리게, 무채색화, 등 그래픽 효과 추가 */

/* 화면 크기에 맞게 CSS 변환 = 반응형으로 만들기 */
@media (max-width: 500px) { /* 미디어 쿼리 (미디어 규칙) */
   .container {
      height: 200px;
      border: 10px solid red;
      background-color: orange;
   } /* 화면의 너비가 500px 이하면 이렇게 변환*/
} 
```
<br>

## 위 CSS파일과 함께 사용된 HTML파일
```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <link rel="stylesheet" href="./main.css"> 
</head>
<body>  
  <div>
    <ul>
      <li class="apple">사과</li>
      <li class="strawberry"> 딸기</li>
      <li class="orange">오렌지</li>
    </ul>
  </div>
  <div class="container">
    <div class="item">1</div>
    <div class="item">2</div>
  </div>
  <div class="anthem">
    동해물과 백두산이 마르고 닳도록 하느님이 보우하사 우리나라 만세 무궁화 삼천리 화려 강산 대한 사람 대한으로 길이 보전하세
  </div>
</body>
</html>
```

<br>