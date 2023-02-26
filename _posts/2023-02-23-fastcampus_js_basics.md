---
title : JS 기본
excerpt : 패스트캠퍼스 코딩 레벨원 - MBTI 테스트 만들며 배우는 왕초보 코딩
categories : coding
---

<br>

## Javascript : 컨텐츠를 바꾸고 움직이는 등 페이지의 동적 처리 담당
- 얼굴에서 눈, 코, 입, 귀가 움직임

- 낙타표기법 camelCase 사용
  - 첫번째 단어의 첫 글자는 소문자, 두번째 단어의 첫 글자부터는 대문자
  - 변수를 작성해야 하지만 띄어쓰기를 하면 안됨, 그래서 가독성을 위해 붙여쓰되 읽기 편하게 만든 것
  - goEatChicken, workAndLife

<br>

## JS 연산자
```javascript
console.log(1+2) // 3, 사칙연산 +, -, *, / 
const 변수1 = 85 // '='는 변수에 값을 할당하는 연산자
```

<br>

## JS에서 다루는 데이터의 종류
```javascript
const stringData = 'Hello World' // 문자 데이터

const numberData = 1234 // 숫자 데이터

const booleanData = true // 참, 거짓 데이터

let numberData1 = 123
numberData1 = null // Null 데이터, 변수에서 값을 제거할 때 사용

const objectData = {
  key1: 'value1',
  key2: 'value2',
  key3: 'value3'
} // 객체 데이터, value1을 key1에 보관하는 형식, 위의 다양한 데이터를 한번에 보관하는 방식
console.log(objectData.key3) // key3에 대한 값을 출력, value3, 마침표를 통해 표기하는 것을 점표기법이라고 지칭
console.log(objectData['key2']) // 점표기법 대신 대괄호 사용 가능

const arrayData = [9, 8, 7, 6] // 배열 데이터, 데이터를 나열해서 보관 가능
console.log(arrayData[2]) // 인덱스 넘버가 2인 값 출력, zero-based numbering으로 0부터 셈
```

<br>

## 변수 설정하는 법
```javascript
const 변수2 = '값2' // 값을 다시 할당할 수 없는 변수 생성, 재할당 시 에러 발생, let보다 권장되는 방법

let 변수3 = '값3' 
변수3 = '값3.5' // 값을 다시 할당할 수 있는 변수, 변수3이 값3에서 값3.5로 변경, 재할당이 필요할 때만 사용

// 예약어 : 특별한 의미를 가지고 있어서 변수나 함수의 이름으로 사용할 수 없는 단어
// let, const, function, if, new, import
```

<br>

## JS 함수 기초
```javascript
function hello() {
  const message = 'Hello World!'
  console.log(message)
}
hello()
hello()
hello()
// 명령을 묶어서 간편하게 반복 사용 가능
// 만약 함수를 사용하지 않고 3번 반복한다면 변수 3개(message1, message2, message3)에 값을 넣고 각 변수들을 모두 실행해야 함

function hello(name) {
  const message = 'Hello '+ name + '!'
  console.log(message)
}
hello('A')
hello('B')
hello('C')
// 함수에 입력되는 값인 인수(A)를 매개변수(name)에 넣어 출력값을 변경

function hello(name) {
  const message = 'Hello '+ name + '!'
  console.log(message)
  return // 함수를 종료, 이 뒤에 있는 내용은 출력되지 않음
  console.log('이 부분은 실행되지 않아요!')
}
hello('D')
hello('E')
// function 내에 if를 넣어 특정 조건 달성 시 함수 종료하게 만들 수 있음
```

<br>

## JS로 HTML 제어하기
```javascript
const itemEls = document.querySelectorAll('.item') 
// html 파일에서 .item 클래스를 가진 css 선택자를 모두 찾아서 itemEls 변수에 할당, 총 3개 있을 예정
//즉 HTML 요소를 찾아 변수에 저장

const btnEl = document.querySelector('.btn') 
// html 파일에서 .btn 클래스를 가진 css 선택자를 찾아서 btnEls 변수에 할당, 총 1개 있을 예정

const colors = ['blue', 'orange', 'tomato']

btnEl.addEventListener('click', function () { 
  // function () = 익명 함수, 지정된 함수의 이름이 없음
  itemEls.forEach(function (itemEl, index) { 
    // for Each itemEls마다 index 넘버 추가, 찾은 HTML 요소의 개수만큼 함수를 반복해서 run function
    console.log(index, itemEl) // itemEl와 각 index 출력
    itemEl.style.backgroundColor = colors[index] 
    // 각 itemEl의 index와 같은 colors 변수의 배경색을 itemEl에 적용, HTML 요소에 CSS 지정
  })
  btnEl.innerHTML = '<span>클릭했어요!</span>' 
  // 버튼을 클릭한 후 HTML 문구를 변경, span으로 감싸서 css가 적용되게 만듦, HTML 요소의 내용으로 문자를 추가
}) // btnEls 변수에 click 액션을 하면 function으로 정의한 이벤트가 발생, HTML 요소를 '클릭'하면 함수를 실행
```

**위 함수의 최종 결과**  
<img width="364" alt="123" src="https://user-images.githubusercontent.com/112374186/221399755-3e39cb98-1a73-4112-97c1-4ce12c93d074.png">

<br>

## 위 JS 실행에 사용한 HTML
```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <link rel="stylesheet" href="./main.css">
  <script defer src="./main.js"></script>
</head>
<body>
  <div class="container">
    <div class="item">1
    </div>
    <div class="item">2
    </div>
    <div class="item">3
    </div>
  </div>
  <div class="btn">클릭하세요</div>
</body>
</html>
```

<br>

## 위 JS 실행에 사용한 CSS
```css
.btn {
   width: 150px;
   height: 40px;
   background-color: rosybrown;
   border-radius: 10px;
   color: white;
   display: flex;
   justify-content: center;
   align-items: center;
   cursor: pointer; /* 마우스 커서가 올라갔을 때 화살표에서 손가락으로 변경 */
   transition: 0.2s;
}

.btn:hover {
   background-color: blue;
}

.btn span {
   font-size: 22px;
   font-weight: 700;
}
```

<br>