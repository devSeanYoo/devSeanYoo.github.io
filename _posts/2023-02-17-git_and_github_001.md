---
title : 깃의 역할과 용어, 깃헙 용어
excerpt : 유튜브 생활코딩 참고
categories : github
---

## 깃의 역할
**버전관리**  
- 각 버전에 대한 수정내용, 수정날짜, 등 정보 기록 용이  
    > 블로그 만들 때 작업하다가 에러가 뜨면 깃헙 데스크탑에서 히스토리를 뒤져봄  
    > 언제, 어떤 코드를 넣었기에 에러가 발생하는지 찾기 쉬움

- commit : 새로운 버전 생성  
  
기록을 따로 정리하지 않아도 히스토리에 쌓여있다는 것이  엄청난 메리트

<br>

**백업**  
- 개인 컴퓨터에만 보관된 파일은 유실 가능성이 존재 > 그래서 백업해야함  
- 백업 데이터는 따로 개인 서버에 보관하거나, 원격 저장소 (클라우드 서비스)를 이용  
- publish : 원격 저장소에 처음 보관
- push : 로컬의 버전을 원격 저장소로 밀어넣어서 보관
- pull : 원격 저장소에서 당겨서 로컬로 가져옴

<br>

**협업**  
- push, pull을 여러 명이서 진행하면 곧 협업  
- 깃이 중간에서 서로의 수정내용에 대한 교통정리를 함  
    > ex. 같은 내용을 2명이 수정해서 push했다면 어떻게 될까?

- branch : 각 사용자가 작업하는 가지  
    > 기능 추가 등 수정할 때 main branch에 바로 작업하지 않고 feature branch를 새로 만들어서 진행
- pull request로 자신의  branch 검토 요청
- 이후 main/master branch로 merge

<br>

깃 자체는 깃헙데스크탑보다 많은 기능이 있지만 지금 당장은 버전관리 및 백업 용도로만 사용 예정이라 깃 명령어는 필요 없음, 나중에 협업에 용이한 부분은 추가로 공부하기

## 깃헙 용어
repository : 저장소  
public : 오픈소스 프로젝트  
private : 초대된 사람들만 이용 가능  
fork : 내 저장소로 복제  

깃헙에 대한 기능은 블로그 만들면서 맨땅에 헤딩하며 이미 배운 내용들 위주

<br>

출처 :  
*Git1, 생활코딩, 2018.09.10*, <https://www.youtube.com/playlist?list=PLuHgQVnccGMCNJESahrVV-uYGMNYK_vMf>  
*Github.com - Pull request, 생활코딩, 2020.10.21*, <https://www.youtube.com/playlist?list=PLuHgQVnccGMBXv1OKe3Hn3Jq6F735-uWm>  
*Github.com, 생활코딩, 2020.08.03*, <https://www.youtube.com/playlist?list=PLuHgQVnccGMDWjb0TWItMCfDWDs8Y3Oo7>

<br>
