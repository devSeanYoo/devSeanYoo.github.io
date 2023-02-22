---
title : Visual Studio Code 기초
excerpt : 기초 설정 및 기본 명령어, 사용 extensions 정리
categories : coding
---

## 기초 설정
- 하단의 상태바가 보라색이면 아무 프로젝트도 열리지 않은 상태
  - 파란색이 되어야 프로젝트가 열려있는 상태  
-  Activity Bar (메인 메뉴) > Side Bar (각 메뉴의 창)
- User settings.json에서 indent당 공백 개수 설정 가능 
  - 공백 4가 디폴트, 한번 indent할 때마다 공백 4개 들여쓰기
- tab 또는 enter로 해당 명령어 자동완성 및 실행
- 코드블럭이라면 드래그하지 않아도 명령어 실행 가능 (ex. 잘라내기 또는 복사)
- Manage 메뉴에서 setting sync on 하면 깃허브나 MS계정을 통해 기기 연동
- 설정에서 word wrap : 창의 크기에 따른 코드 자동 줄바꿈 설정

<br>

## 기본 명령어
- ctrl + shift + p = 모든 명령 표시  
- ctrl + / : 해당 라인 전체 주석처리  
- c + tab : 주석 태그 바로 생성  
- ctrl + p : 파일 검색  
- ctrl + , : 설정  
- ctrl + d : 커서가 놓인 단어와 같은 단어를 모두 하이라이트하고 일괄 수정 가능  
- alt + 클릭 : 클릭한 모든 곳에 커서를 넣어서 동시에 일괄 입력 가능  
- alt + shift + i : 드래그된 줄들의 끝에 커서를 넣어서 동시에 일괄 입력 가능  
- alt + 방향키 : 커서가 있는 줄/드래그된 줄들을 위아래로 이동 (잘라내기+붙이기 불필요)  
- alt + shift + 방향키 : 커서가 있는 줄/드래그된 줄들을 위아래에 복붙  
- ctrl + home, end : 파일의 시작과 끝으로 이동  
- ctrl + L : 커서가 있는 줄 선택  
- ctrl + 좌우방향키 :  빠른 커서이동  
- ctrl + 위아래 방향키 : 스크롤바 이동

<br>

## 사용 Extensions 정리
- Korean Language Pack for VS Code 로 한글 패키지 설치  
- Code Spell Checker로 오타 검수  
- Live Server로 VS Code에서 수정하는 사항을 로컬서버를 통해 실시간으로 확인  
- Markdown All In One, Markdown Shortcuts로 블로그 작성 편하게 만듦  
- 파이썬 수업 때 설치한 파이썬 관련, 쥬피터 관련 확장 프로그램들

<br>

출처 :  
*Visual Studio Code 기본 사용법, 생활코딩, 2021.08.25*, <https://www.youtube.com/watch?v=K8qVH8V0VvY>  
*5 Essential VSCode Shortcuts To Code Faster, 노마드코더, 2019.11.11*, <https://www.youtube.com/watch?v=Wn7j5dfbJF4>  
*Visual Studio Code Keyboard Shortcuts for Windows*, <https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf>