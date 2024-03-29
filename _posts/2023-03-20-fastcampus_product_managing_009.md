---
title : O2O 산업 및 직방 서비스 분석
excerpt : \[패스트캠퍼스] 한 번에 끝내는 서비스 기획의 모든 것 초격차 패키지 Online
categories : pm
---

## 기획자로서 고려해야 할 질문
- 어떻게 문제를 해결할까?
- 어떤 임팩트를 전달할까?

<br>

## O2O 산업
- 온라인에서 오프라인으로 seamless하게 사용자 경험이 연결되게 하는 산업
- O2O의 근간은 온디맨드 서비스
  - 기존의 오프라인의 수요를 언제든지 온라인으로 충족시키고, 오프라인으로 서비스를 제공하는 방식
- 그러나 오프라인 서비스와 온라인 서비스에 간극이 존재
  > ex. 직방에 올릴 집 사진을 찍을 때 과도하게 왜곡해서 집이 넓은 것처럼 보이게 찍기
- 그래서 OMO Online Merge with Offline
  - 온라인과 오프라인에 사용자 경험이 동일하게 제공 
  - 어떻게 이를 실현할지가 중요
- 온라인 환경의 서비스와 오프라인 환경의 서비스를 둘다 이해해야 함

<br>

## 직방 서비스 분석 
> 강의자료 참고

- 앱 내에 있는 다양한 서비스의 메인화면과 하위 서비스 분석
> - 아파트 서비스
>   - 매매/전월세 메인
>     - 거주민 리뷰 서비스
>     - 우리집 내놓기 서비스
>     - 직방 시세 서비스, 3D 단지 투어
>     - 아파트 중개 라이브  
>   - 신축 분양 메인
>     - 신축분양 목록과 광고  
> - 앱 푸쉬 서비스

- 서비스의 비전과 전략 조사

- 수익구조 조사
  > ex. 원룸/투룸/아파트 분양 광고, 중개 수수료, 스마트홈 커머스

- 서비스 CJM 작성
  > ex. 매물 등록 > 매물을 광고에 적용 > 매물 탐색 > 중개사 연락 > 고객 응대 > 방문 및 계약
  - 각 단계마다 이탈율 계산

- 관련 이해당사자 운영구조 작성
  > ex. 집주인, 부동산 중개인, 사용자, IoT사업, 아파트 관리업체

<br>

## 직방 서비스의 문제점
- **기존 문제를 해결하여 사용자 손실을 최소화 :** VoC, 서비스 지표 모니터링, 사용자 이탈 최소화를 위해 개선할 문제
  > ex. 매물 탐색하는 과정에서 매물 비교하기가 어렵다
- **더 좋은 가치를 제공하고 잠재 문제를 해결하여 사용자 유입을 최대화 :** 프로덕트 비전, 비즈니스 목적, 구성원의 의지, 사용자 유입 최대화를 위해 개선할 문제
  > ex. 중개 매물의 한계로 중개 수수료 수익 극대화 어려움

- 문제를 발견한 후 이 문제가 왜 존재하는지, 왜 아직 해결되지 못했는지 추론하기
  > 현직자들이 몰라서 냅둔 것이 아니다  
  > ex. 법적 규제, 사내 인프라 구축 미흡, 등

- 기존 데이터를 바탕으로 문제 정의, 그 문제를 해결하는 가설은 어떤 것인가, 그 가설을 증명하기

<br>

## 개선 방식
- 개선안을 제안하고 동료들을 설득해야 함
  - 모두가 문제에 대한 공감과 컨텍스트를 이해한 다음에 업무가 시작해야 함
  - 어떤 개선안을 채택할지, 어떤 방식으로 개선할지 자기 혼자 생각하고 개선안을 결론지어 통보하지 말고, 유관 부서와 데이터로 정의된 문제에 대한 회의를 진행해야 함  
    > ex. 이탈율을 해소하기 위해 UI를 바꿔주세요 (x)  
    이 부분에서 이탈율이 n%인데 이걸 어떻게 해소할 수 있을까요? (o)
​
1. 타 사 서비스 벤치마킹  
정의한 문제 해결에 가까운 서비스를 선정해서 비교

2. 개선안 수립  
사용자 스토리를 정의하여 어떤 요구사항이 필요한지 정리
누구는 무엇을 위해 무엇을 하고 싶다

3. 개선안 디벨롭  
유관부서와 대략적인 일정 협의

4. 세부 기획
   1. 서비스 정책 : 프로세스를 진행하기 전에 의사결정이 필요한 사항들을 정리
   2. 서비스 프로세스 : 유저 스토리를 구현 기능 단위로 나눠 프로세스 정리
   3. 상세 스펙과 화면 설계 : 개선 방안을 어떻게 서비스에 구현할 것인지 UI와 스토리보드 설계
   4. 서비스 운영 메뉴얼 : 사용자 가이드 운영 메뉴얼 작성

<br>

5. 분업 및 스토리 포인트 관리  
스토리 포인트 : 각 업무당 소요 시간

6. 프로세스 트래킹  
정기 미팅 블록을 통해 이슈 공유, 만약 이슈가 없다면 바로 해산

7. 사용자 행동 추적 코드를 심어서 데이터 수집  
GA, Amplitude

8. 성과 측정
GA 데이터, Amplitude 데이터, SQL로 DB 접속  
성과의 이유를 바탕으로 좋은 성과요소는 Keep, 나쁜 성과 요소는 Fix

<br>