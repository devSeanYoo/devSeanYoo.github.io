---
title : 엑셀로 최신 뉴스 스크랩하는 법
excerpt : RSS를 통한 네이버, 구글 뉴스 스크랩
categories : excel
---

## 스프레드시트로 뉴스 스크래핑
1. 구글 스프레드시트를 켠다.
2. A1셀에 다음 코드를 붙여넣는다.  
=importfeed("http://news.google.com/news?hl=ko&gl=kr&ie=UTF-8&output=rss&q=펭귄","",true,30)  
=importfeed("http://newssearch.naver.com/search.naver?where=rss&query=펭귄","items",true,100)  
    > importfeed("뉴스의 rss를 얻는 주소", "쿼리", 헤더표시여부, 표시할 기사 개수)  
    > 펭귄을 다른 단어로 바꾸면 된다  
    > 복사했을 때 Formula parse error가 뜬다면 따옴표를 지웠다가 다시 적기

> 2023-02-19자로 네이버뉴스에서 rss를 제대로 긁어오지 못하는 듯 하다.

> 위 코드는 빅데이터를 다루는 학교 수업에서 배운 내용이다. 나중에 특정 단어를 기준으로 최신 뉴스 모아보거나, 연관 단어 분석할 때 사용할 수 있다.