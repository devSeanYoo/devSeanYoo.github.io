---
title : 스파르타코딩클럽 [엑셀보다 쉬운 SQL] 3주차 개발일지
excerpt : 쿼리 순서 = from > join > where > group by > select > order by
categories : SQL
---

## Join, Union을 통해 테이블 연결하기

데이터를 테이블 별로 나눠서 보관하는 이유는 각 목적에 맞는 데이터들만 모아두는 것이 간편하기 때문

<br>

**Join** : 두 테이블의 공통된 정보(key값)을 기준으로 두 테이블의 데이터를 연결해서 한 테이블처럼 보기
(엑셀의 vlookup과 유사)

**left join**
```sql
select * from A a // A테이블을 a라고 별칭을 설정
left join B b // A테이블의 오른쪽에 B테이블을 연결, B테이블의 별칭은 b
on a.C = b.C // A테이블의 C필드와 B테이블의 C필드가 같은 데이터, 이 둘을 기준으로 연결
```

만약 데이터가 없다면 공란 null로 표시 (A에 B 데이터를 붙여서 추가적으로 보여주는 개념, A와 B의 순서가 중요함)  
NULL의 여부에 따른 데이터를 구하고 싶다면 left join 사용  
> 예) 활동시간이 null인 사용자 이름 구하기  
> - 활동시간 테이블과 사용자 테이블로 나뉘어져 있을 것  
> - 사용자 테이블에 활동시간 테이블을 left join  
> 만약 반대로 붙이면 활동시간 없는 사용자는 보이지 않음  
> - 합쳐서 활동을 아직 하지 않은 사용자 구함  
 = 등록만 한 사용자

<br>

**inner join**  
inner join은 null이 아닌 데이터들만 표시 (A와 B의 교집합만 보여주는 개념, 순서 상관 없음)  
inner join을 제일 자주 사용함

Outer Join은 거의 사용하지 않음

<br>

join 후 필드명을 지칭할 시 어느 테이블의 필드인지 모호하기에 에러 발생 (모호하지 않다면 즉, 같은 이름의 필드가 1개밖에 없다면 별칭이 없어도 됨)  
<span style='color: red'>**join 후에는 필드명 앞에 테이블의 별칭이 무조건 붙어야함**</span>

<br>

group by와 order by에 콤마를 통해 여러 필드를 한번에 조건을 걸 수 있음  
group by A, B : A로 먼저 묶고 그 안에서 B로 묶음  
order by A, B : A로 먼저 정렬하고 그 안에서 B를 정렬

inner join을 두번 사용해서 테이블 3개를 연달아 붙일 수 있음

count는 null공란을 건너뛰고 데이터가 들어있는 항목의 개수만 셈  
count한 값을 수식에 넣고 싶다면 count() 전체를 넣어줘야 함 (count() as의 별칭을 대신 넣을 수 없음, <span style='color: skyblue'>근데 그럼 별칭을 만드는 이유가 없는데..??</span>)

**Union** : 같은 필드를 갖고 있는 두 개의 테이블을 연달아 세로로 보려고 할 때 사용  

```sql
(A)
union all
(B) // A와 B테이블을 세로로 합친다
 ```
union내에서는 order by가 적용이 되지 않음 = 합쳐진 테이블이 정렬되어있지 않음

**쿼리 순서 = from > join > where > group by > select > order by**