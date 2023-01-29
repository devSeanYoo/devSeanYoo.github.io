---
title: 스파르타코딩클럽 [엑셀보다 쉬운 SQL] 2주차 개발일지
excerpt: Group by, Order by를 통한 범주화와 정렬
categories: sql
---


## Group by, Order by를 통한 범주화와 정렬

<br>

**Group by A**: A필드 내 동일한 데이터끼리 묶기, 그냥 group by 만 작성하면 무엇을 통계내야 하는지 모르기 때문에 각 데이터 중 대표 하나씩만 보여줌  
예) 같은 이름끼리 묶기 = group by name

<br>

**통계 명령어**  
select A, count(B) from C 후 group by A 를 통해 C 테이블의 A 필드에서 B 개수 찾기  
min은 최소값 찾기  
max는 최대값 찾기  
avg은 평균 찾기, 소수점일시 round(A,1) 하면 A를 반올림해서 소수점 첫째자리까지 보여주기  
sum은 합계

<br>

**정렬 명령어**  
order by A: A필드를 기준으로 오름차순으로 정렬  
order by A desc : A 필드를 기준으로 내림차순으로 정렬  
정렬은 쿼리 작업 다 끝나고 마무리로 실행  
;을 붙이면 퀴리의 끝을 나타냄 (optional)

<br>

**Alias** : 별칭, 쿼리가 길어질 경우 어떤 테이블의 필드를 지칭하는지 나타낼 수 있음  
select * from apple a 로 작성한다면 apple 테이블의 alias는 a
이후에 apple 테이블의 필드를 지칭할 때 a.필드 형식으로 refer 가능
apple as a로 표기해도 됨
