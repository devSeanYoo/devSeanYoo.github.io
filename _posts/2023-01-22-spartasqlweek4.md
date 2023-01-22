---
title : 스파르타코딩클럽 [엑셀보다 쉬운 SQL] 4주차 개발일지
excerpt : Subquery 이용
categories : SQL
---

<br>

**Subquery** : 쿼리 안에 쿼리를 삽입하는 형태  
select 절, from 절, where 절 등 다양한 곳에 삽입 가능  
코딩하듯이 줄을 잘 맞춰줘야 이해하기 편함

<br>

**where 절 서브쿼리** : 서브쿼리로 where절의 조건 설립  
where 필드명 in (서브쿼리)
```sql
select *  // 전체 필드를 보고 싶음 (3)
from users u  // users 테이블에서 (1)
where user_id in (  // 유저 아이디가 다음과 같은 유저들 (2)
	select user_id  // 유저아이디를 보고 싶은 서브쿼리 (2.3)
	from orders o  // orders 테이블에서 (2.1)
	where payment_method = 'kakaopay'  // 결제방식이 카카오페이인 (2.2)
)
```

<br>

**select 절 서브쿼리** : 보여줄 필드를 새로 추가  
select 필드명, 필드명, (서브쿼리) from 테이블명  
```sql
select c.checkin_id, // checkins 테이블의 체크인 아이디 (2)
	   c.user_id , // checkins 테이블의 유저 아이디 (3)
	   c.likes ,  // checkins 테이블의 좋아요 개수 (4)
	   (
		select avg(likes) // 그 유저의 좋아요 평균을 (7)
		from checkins // checkins 테이블에서 (5)
		where user_id = c.user_id // 유저아이디가 (3)에서 불러온 유저아이디와 같다면 (6)
		) as avg_likes // avg_likes 별칭으로 보고싶다 (8)
from checkins c (1)
```

<br>

**from 절 서브쿼리** : 서브쿼리로 만들어진 테이블을 이용  
select 필드명 from 테이블명 inner join (서브쿼리) on  
```sql
select pu.user_id , pu.point, a.avg_likes // 이것들을 보여줘라 (7)
from point_users pu // 이 테이블과 (5)
inner join ( // 합친 다음에 (6)
	select user_id , round(avg(likes),1) as avg_likes // 유저 아이디와 좋아요 평균 개수 필드를 보여주는 테이블을 (3)
	from checkins c // checkins 테이블에서 (1)
	group by user_id // 유저 아이디별로 묶었을 때 (2)
	) a on pu.user_id = a.user_id // 유저아이디를 기준으로 (4)
```

<br>

select절에서 바로 만들어진 별칭은 그 절에서 사용 불가능  
서브쿼리 내의 select 절에서 만들어진 별칭은 전체 쿼리 select 절에서 사용 가능

with table1 as (서브쿼리), table2 as (서브쿼리)  
서브쿼리 전체를 쿼리 안에 넣을 필요 없이 table1을 통해 refer 가능  
제일 윗단에 적어야 함

<br>

문자열 쪼개기 
```sql 
substring_index(필드명, '문자', 1) // 필드에서 '문자'를 기준으로 앞에 있는 부분만 추출  
substring_index(필드명, '문자', -1) // 뒤에 있는 부분만 추출
```

문자열 일부 쪼개기  
```sql
substring(필드명, 시작포인트 인덱스넘버, a) // 필드에서 시작포인트가 인덱스 넘버인 글자부터 옆으로 a 칸까지 추출
```

원하는 값 필드에 출력 : 테이블로 만들어 서브쿼리로 사용 가능  
```sql
select // 보여달라 (5)
	(case when 조건 then 결과A // 이 조건에 포함되면 결과A를 (2)
	else  결과B // 아니라면 결과B를 (3)
	end) // 조건 종료 (4)
from 테이블 //테이블에서 (1)
```