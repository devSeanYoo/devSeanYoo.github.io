---
title:  "(첫글) 깃헙 블로그 구축하기"
excerpt: "계정 생성부터 사이트 등록까지"
categories: GithubBlog
---

## 계정 생성부터 사이트 등록까지

**출처 : _깃헙(GitHub) 블로그 10분안에 완성하기_, 테디노트 TeddyNote, 2021.01.13, Retrieved from <https://www.youtube.com/watch?v=ACzFIAOsfpM>**

**깃헙 블로그 초기 구축**

1. 깃헙 계정을 만든 후 <https://github.com/topics/jekyll-theme> 에서 블로그 테마 선택 후 내 계정으로 fork <br>
    Fork 시에 다른 세부 사항은 건들지 않아도 됨

2. fork 후 setting에서 repository name 수정 필요 <br>
    이름은 자신의 깃헙아이디.github.io 로 수정 (이 블로그의 경우 devSeanYoo.github.io)

3. config.yml 파일에서 url 항목의 주석(# 이후 문장) 삭제 후 url을 repository name과 같이 수정 후 commit <br>
    config 파일에서 블로그 설정 조정 가능 

4. 설정한 url로 30초~2분 정도 후에 접속하면 블로그 사이트로 이동

**블로그 포스팅 방법**

1. _post 폴더 생성

2. 폴더에서 add file

3. 블로그 포스트 파일 이름은 연도4자리-월-일-제목.md 순으로 작성 <br>
    ex. 2023-01-01-first.md <br>
    제목은 마음대로 작성 가능

4. 마크다운 형식 사용 <br>
    매 포스트마다 layout: single, title: 제목 작성
    
5. 링크는 <url> 형식으로 작성하면 됨, <>로 감싸지 않을 시 링크가 걸리지 않음

영상에서는 Typora 툴을 이용해 마크다운 문법으로 쉽게 글을 작성할 수 있다고 하지만 2023년 1월 1일 현재는 유료다. 그래서 다른 무료 마크다운 편집툴을 찾아보는 중이다.  

> 2023-01-02자로 그냥 VS Code에 마크다운 익스텐션 설치해서 쓰는 중... 그럭저럭 쓸 만하다.

참고 자료 : 
_편안한 Jekyll 사용을 위한 마크다운(markdown) 문법_, 테디노트, 2018.04.06, Retrieved from <https://teddylee777.github.io/jekyll/Jekyll-%EC%82%AC%EC%9A%A9%EC%9D%84-%EC%9C%84%ED%95%9C-markdown-%EB%AC%B8%EB%B2%95> <br>
_Minimal Mistakes Jekyll theme Configuration_, Retrieved from <https://mmistakes.github.io/minimal-mistakes/docs/configuration/> <br>
_Jekyll Posts_, Retrieved from <https://jekyllrb.com/docs/posts/>

