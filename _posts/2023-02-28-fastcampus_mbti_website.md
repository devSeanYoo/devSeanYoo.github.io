---
title : MBTI 웹사이트 실습 필기
excerpt : 패스트캠퍼스 코딩 레벨원 - MBTI 테스트 만들며 배우는 왕초보 코딩
categories : coding
---

<br>

## 웹사이트 만드는 순서
1. html의 구조를 먼저 구상  
   - div, h1, h1, img등 어떤 요소들이 들어갈지 생각하기
2. html 구조를 바탕으로 각 요소들의 css를 꾸미기
3. html 구조와 반응할 js 할당

<br>

## 기타 팁
- js 배열 데이터 내에 객체 데이터를 여러 개 넣고 index에 따라 필요한 데이터를 뽑을 수 있음  
  - 배열이름.index=해당 객체데이터

- js의 export : 해당 변수를 파일 밖으로 내보내기 = 또 다른 js파일에서 사용 가능하게 만들어줌

- 폴더의 최상위 경로에 ico파일이 있다면 사이트의 파비콘으로 인식됨, 아니면 직접 head에 넣기
  ```html
  <link rel="icon" href="favicon.png"> <!-- 파비콘 추가 -->
  ```

- 브라우저에 따라 기본 css가 있어서 다르게 출력됨 : 이를 리셋하고 새로 만들어야 브라우저와 무관하게 원하는 css 적용 가능
  ```html
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reset-css@5.0.1/reset.min.css" /> <!-- css 리셋 -->
  ```

- 웹 폰트 적용, css에 font-family도 맞춰서 기입
  ```html
  <link rel="stylesheet" as="style" crossorigin href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.6/dist/web/variable/pretendardvariable-dynamic-subset.css" />
  ```

```css
display: block; /* 이미지는 원래 글자 요소인데 이걸로 블록요소로 변환 가능 */
```

- js에 파일을 import했을 경우 해당 js를 사용하는 html에 script할 때 
  ```html
  <script type="module" defer src 추가 필요
  ```

```javascript
location.href = '/results.html?mbti=' + mbti // 물음표를 통해 전달하고 싶은 데이터를 만드는 것을 쿼리스트링이라 부름
```

<br>

## 최종 실습 자료 링크
**<https://github.com/devSeanYoo/mbti_website>**

<br>