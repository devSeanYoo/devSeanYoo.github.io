---
title:  "스파르타코딩클럽 [엑셀보다 쉬운 SQL] 1주차 개발일지"
excerpt: select, where 등 조건 걸어서 데이터 보기
categories: SQL
---

## select, where 등 조건 걸어서 데이터 보기

Table : 데이터가 담긴 시트 <br>
Field : 시트 내 특정 항목 <br>

show tables : 무슨 테이블이 있는지 알아보기 (좌측 네비게이터에서도 확인 가능) <br>
select A,B,C(* = 모든 필드) from D(테이블) <br>
where A = B: A 필드에서 B라는 조건에 해당하는 데이터만 추출 <br>
and, or로 다중조건 설정 <br>

'=' = 같다 <br>
'!=' = 같지 않다 <br>
문자열은 ''로 감싸기, 숫자열은 감싸지 않기 <br>
날짜는 문자열 <br>

where A between B and C : A 필드에서 B와 C 사이의 데이터만 <br>
where A in (B,C) : A 필드에서 B와 C에 해당하는 데이터만 <br>
where A like '%B' : A 필드에서 B로 끝나는 데이터만 <br>
  a%t : a로 시작하고 t로 끝나는 요소 <br>
 
limit n : n개의 데이터만 볼 때 <br>
distinct(필드명) : 필드 내에서 중복제거하고 보기 <br>
count(필드명) : 필드의 전체 데이터 개수 확인 <br>

에러가 발생한다면 에러 메시지를 읽고 해석해서 스스로 해결하려고 하라 <br>
(예전 노마드코더 유튜브 영상에서 개발 실력 늘리는 방법 중 한가지) <br>
cf) SQL은 파이썬에 비해 에러 메시지가 친절하지 않은 느낌이 듦 <br>
