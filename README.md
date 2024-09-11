<p align="center" style="font-size: 40px; font-weight: bold;">
  <strong>테스팅 연습 기록</strong>
</p>  

테스팅 공부를 하고 기록을 남기기 위한 레퍼지토리 개설
---
공부 교재 : 부트 캠프 QA편 (남효진 지음)
---
교재 목차 

1장. 소프트웨어 테스팅 개요

2장. 기능, 비기능 테스팅 방법

3장. 소프트웨어 테스트 프로세스

4장. 실전 소프트웨어 테스팅
---
**2024/09/03 공부 기록** 
---
1장. 소프트웨어 테스팅 개요
---
1.1 테스팅의 정의와 활동
테스팅이란??  
기능적 측면에서 제품 또는 서비스가 고객의 요구사항을 충족하는지 확인하고 동작, 성능, 안정성등 제품의 내외부 요인에서 발생하는 결함이 없는지 확인하는 활동이며,
관리적 측면에서는 품질 보증 활동으로 쌓아온 품질 데이터를 활용하여 리스크를 판단하고 문제를 예방하는 활동을 말한다.

테스터는 제품 설계 단계부터 출시 이후까지 제품에 영향을 미치는 모든 요소를 발견, 제어, 차단, 예방하는 활동을 한다.

테스트 조직의 테스트 활동 범위 

테스특 계획 및 전략 -> 테스트 분석과 설계 -> 테스트 실행 -> 테스트 인시던트 보고 -> 테스트 종료 -> 회고

1.2 테스트 레벨
---
소프트웨어 테스팅 활동은 소프트웨어 생명주기 전반에 걸쳐 테스트 레벨과 테스트 종류로 구분해 수행한다.

단위 테스트

단위 테스트(코드 데스트)는 모듈이나 클래스, 메서드 등 가장 작은 단위의 소프트웨어를 대상으로 요구 사항대로 작동되는지 확인하는 테스트이다.
단위 테스트는 소스 코드를 중심으로 개발자가 테스트를 수행하고, 별도의 테스트 케이스 없이 개발 설계서, 컴포넌트 명세서와 같은 개발 산출물로 테스트를 수행한다.
흔히 테스트 주도 개발(TDD)과 개발자 테스트로 지칭한 테스트들을 말한다.
단위 테스트의 특징은 코드를 작성한 개발자 또는 개발 팀이 테스트를 수행해서 발견하는 결함을 디버깅 기간을 두지 않고 즉시 수정하며 결함에 대한 기록을 남기지 않는다.
단위 테스트를 잘 사용하면 제품의 모듈별 품질이 향상되어 안정성을 확보하고 전반적 테스팅 시간을 절감하고 비용을 줄일 수 있다. 

통합 테스트 
각 모듈에 대한 개발이 완료되면 통합을 진행하며, 이떄 발생할 수 있는 모듈 간 상호작용하는 동작을 확인하는 테스트이다.
(ex: 스마트폰 애플리케이션 실행시 api 호출하여 고객의 요청에 대한 응답을 내려 줄떄 애플리케이션으로부터 api를 호출하여 응답을 내려 주는 동작이 정상적으로 작동하는지 확인)

시스템 테스트
통합이 완료된 완벽한 소프트웨어 제품을 하드웨어와 결합한 뒤 시스템 기능과 하드웨어 통합 간 인터페이스 전체를 확인하는 테스트를 말한다.
시스템 테스트의 목적은 기능적 요구사항과 비기능적 요구사항을 모두 포함하기 때문에 유저가 사용할 환경이나 그와 유사한 환경에서 테스트를 수행한다.
일반적으로 인수 테스트가 출시 여부를 결정하기 위한 최종 테스트라고 인식하고 있지만, 시스템 테스트가 그 역할을 대신하는 경우가 있다.

인수 테스트
인수테스트는 실제 시스템을 사용하게 될 최종 유저(고객)가 제품이 요구 사항을 충족하는지 확인하고 이에 대한 평가를 얻기 위한 테스트이다.
인수테스트는 알파 또는 베타 테스팅이라는 이름으로 실제 유저가 테스트를 수행하기도 하고, 직접 참여가 어려울 경우 테스트 조직이나 제품 관련자가 유저 입장에서 제품 완성도를 확인하는 테스트를 수행한다.

1.3 테스트 종류 
---
기능 테스트
기능 테스트는 기획서 또는 고객 요구 사항 명세서, 개발 설계서와 같은 문서를 기반으로 도출된 테스트 케이스를 사용하여 시스템의 기능과 특징, 시스템 간 상호작용을 확인하는 테스트이다.
기능 테스트의 종류에는 단위 테스트, 스모크 테스트, 통합 테스트, 시스템 테스트, 인수 테스트, 리그레션 테스트 등이 포함된다. 

비기능 테스트
비기능 테스트는 시스템의 성능, 유용성, 안정성, 확장성 등 비기능적인 측면에서 시스템의 동작을 확인하는 테스트이다.
비기능 테스트의 종류에는 네트워크 테스트, 호환성 테스트, 어뷰징 테스트, API 테스트, 데이터 테스트 등이 포함된다.

스모크 테스트
스모크 테스트는 테스트 조직에 의해 정식 테스트 절차를 시작하기 앞서 테스트가 가능한 상태인지 확인하기 위한 목적으로 신속하게 주요 기능과 그에 연관된 상호작용을 확인하는 테스트이다.

리그레션 테스트
리그레션 테스트는 이미 테스트된 시스템을 반복해서 확인하는 것으로 격함 수정 이후 변경된 결과가 이전에 제대로 작동하던 기능들과 문제를 발생시키지 않는지, 사이드 이펙트로 새롭게 발생한 결함은 없는지, 수정했던 결함이 재발생하지 않는지 확인하는 테스트이다.
리그레션 테스트는 모든 테스트 단계에서 수행할 수 있지만 실무에서는 가급적 발견한 결함을 대부분 수정하고 시스템이 안정되는 단계에서 기능 상태를 최종으로 확인하기 위한 용도로 사용한다.

마이그레이션 테스트
마이그레이션 테스트는 서버 버전이 업데이트되거나 서버 또는 디바이스로 교체되거나, 데이터베이스를 통합허거나 폐기할 떄 데이터를 한 위치에서 다른 위치로 이동하는 것을 말한다.
마이그레이션 테스트는  데이터 마이그레이션 후 분실되거나 변경되는 데이터, 기능상 작동되지 않는 문제, 새롭게 발생하는 결함은 없는지 확인하고 시스템 안정성을 보장하기 위해 수행한다.

---
**2024/09/04 공부기록
---
---
1.4 소프트웨어 품질 관리자의 명칭과 역할
---

테스터

유저의 입장과 개발자의 입장에서 명세서를 바탕으로 테스트 케이스를 설계하고 테스트를 실행하는 역할을 수행한다. 

테스트 리더 

QA 조직과 테스트 조직이 서로 독립적일 떄 테스터들을 관리하고 테스트 활동 계획 및 수행 상황을 체크하고 보고하는 역할을 한다. 

QA

QC와 QM의 역할을 포함한다.
QA는 제품 또는 서비스가 필요한 수준 이상의 품질을 달성했는지 평가한다(QC). 또한 품질 요구 사항을 충족한다는 확신을 제공하고 이를 보장하기 위해 품질 관련 프로세스 및 절차를 정의하고 개선한다(QA).  

소프트웨어 테스트 엔지니어

소프트웨어 테스트 엔지니어 또는 SDET(Softwarre Development Engineer in Test)는 품질 보증 관련 조직 내 테스트와 관련된
개발 활동을 수행하는 전문가 조직이다.

소프트웨어 아티펙트

소프트웨어 개발 과정에서 생성되는 다양한 부산물들이며, 예를 들어, 소프트웨어 모듈, 요구 사항 문서, 애플리케이션 등이 있다.

프레임워크

품질 목적 달성을 위해 단위 테스트에 필요한 것을 개발자가 고민할 필요 없이 일관된 코드 구성 규칙을 제공하여 프로그래밍 작업을 보다 쉽게 수행할 수 있도록
만들어 놓은 틀이다.

---
**2024/09/05 공부기록
---

1장 핵심 요약

테스팅이란??

제품 설계 단계부터 출시 이후까지 제품의 품질에 영향을 미치는 모든 요소를 발견하고 제어, 예방 , 차단하는 활동이다.

테스팅 활동이란??

테스팅 활동은 테스트 레벨과 테스트 종류로 구분된다.  테스트 레벨은 개발 생명주기에 따라 단위 통합, 시스템, 인수 테스트로 구분할 수 있고,
테스트 종류는 테스트 목적에 따라 기능, 비기능, 리그레션 테스트로 구분한다.

테스터의 역할이란?

테스팅 수행 포지션에는 테스터, QA, 테스트 엔지니어로 역할이 구분되며, 테스터는 테스트 케이스를 설계하고 테스트를 실행하는 역할, QA는 제품의 품질 달성을 평가하고 품질을 보장하기 위한 프로세스를 정의하고 개선하며,
테스트 엔지니어는 테스트와 관련된 자동화, 화이트박스 테스팅 같은 프로그램을 개발하는 역할을 수행한다.

테스트 조직이란?

목적 제품 특성 요구 등에 따라 독립적 조직, 비즈니스 그룹내 독립적 그룹, 개발 그룹내 테스트 파트로 구성된다.

테스트 전문가의 요구와 지질

테스트 전문가가 되려면 기본적으로 소프트웨어 공학에 대한 이해, 테스팅 전문 지식, 테스팅 지원 도구에 대한 기술과 경헙이 필요하다.
또한 문제 해결 능력, 협업 능력 등이 있어야 한다. 

---
2024/09/06 공부기록
---

---
2장 테스트 설계 기법
---

2-1 전략적 접근 방법으로 테스트 기법 활용하기

테스트 설계 기법은 소프트웨어를 분석하고 이것을 바탕으로 테스트 케이스를 도출하는 것이다.
어떤 기법을 사용해서 테스트 케이스를 작성할 것인가 하는 테스트 작성 방법론으로서 접근이 아니라 테스트 수행을 위한 전략적 접근 방법으로 테스트 설계 기법 활용을 목적으로 접근해야 한다.

테스트 전략

테스트 전략은 목표 달성을 위해 테스트 컨텍스트를 설정하고 시스템의 리스크, 테스트 대상 객체, 담당자, 요구 사항 등 다양한 측면에서 테스트 수행을 위한 
전체 설계를 구상하고 계획을 수립하여 필요한 활동을 정의하는 것이다.

테스트 컨텍스트

상황에 따라 테스트를 실행, 판단, 결정해야 하는 부분

테스트 전략 수립 과정

착수 -> 계획 -> 분석/설계 -> 구현/실행 -> 완료/리포팅 

테스트 절차별 계획 수립 단계 

요구 사항 또는 기획 의도 분석: 테스트 대상의 설계 목적과 중심 가치를 분석하여 주요 기능 선별, 리스크 분석하여 제거 전략 계획

테스트 목표 수립: 명확하고 구체적이고 달성 가능한 목표를 계획해야 한다.  예를 들어 테스트 커버리지 수행률, 성공률 100% 달성 등

테스트 일정 관리: 테스트 시작부터 완료까지 소요되는 시간을 추정하여 일정을 계획하되 테스트 기간 내 개발자의 디버깅 소요 시간까지 고려한다.

테스트 범위 및 우선 순위 선정: 시스템 구성 요소, 프로젝트 요구 사항, 예산, 일정, 우선순위, 투입 인원 역량을 고려하여 테스트 범위를 선정한다. 

테스트 종류 선택: 테스트 범위와 투입된 인원의 역량에 따라 테스트 대상에 맞는 적절한 테스트 종류를 선택한 후 어느 단계에 어떤 테스트를 누가 진행할지 전략을 계획한다.(기능 테스트, 성능 테스트, api 테스트 등)

테스트 수행 방법 및 절차 선정: 프로젝트에 적용된 소프트웨어 개발 생명주기 방법론(폭포수, 애자일 등)에 따라 단계별 테스트 진행 방법 및 절차를 계획하고 투입 인력의 보유 지식과 역량 수준에 따라 테스트 범위를 분배한다.
통합 테스트는 수행 차수별로 분류하여 1차수에는 전체 기능 테스트, 2차수는 이슈 수정 확인 및 추가 개발 건테스트, 3차수에는 리그레션 테스트로 단계적으로 테스트를 수행할 수 있도록 절차를 계획함

테스트 지원 도구 선정 및 테스트 환경 요구 사항 확인: 버그 관리 시스템, 자동화등 기술 검증에 필요한 지원 도구, 데이터 관리 시스템 등 테스트 범위에 맞는 테스트 도구를 선정하고 테스트 방법과 요구 사항에 맞게 테스트를 수행하기 위한 환경을 준비한다.

투입 리소스 선정 및 관리: 시스템 복잡도, 프로젝트 관련자 요구 사항, 테스트 수행 방법에 따라 적합한 인원으로 테스트 담당자를 선정한다. 인원이 선별되면 각 인원별로 수행 역할과 책임을 구분하여 중복된 업무가 발생하지 않도록 계쵝하고 인원별 테스트 진행 과정 및
실행 세부 정보를 추적할 수 있도록 기록 및 관리 방안을 계획한다.

테스트 품질 기준 수립: 테스트 시작 조건, 완료 조건을 계획한다. 

테스트 상태 수집 및 보고 전략: 프로젝트의 현재 상태를 점검하고 관리할 수 있도록 테스트 진행 과정을 기록하고 보고하는 전략을 수립한다. 진행 과정 중 수시로 상태를 점검하여 발생하고 있거나 발생할 것이 예상되는 문제점을 파악하고 즉각하고 대응할 수 있도록 미리 보고 
전략과 대응 인력을 계획한다. 

테스트 기법 선택

테스트 케이스를 설계할 때 테스트 기법을 사용해야 하는 이유는 적은 케이스로 보다 많은 결함을 찾을 수 있고, 일정 수준의 테스트 보장성을 확보할 수 있다.

ISO/IEC 25010:2011

소프트웨어 품질 요구 사항 및 제품의 품질을 평가하기 위한 모델

기능성, 신뢰성, 사용성, 효율성, 유지 보수성, 이식성 


---
2024/09/09 공부기록
---


2.2 명세 기반 기법

시스템에서 제공하는 기능 및 메뉴에 대한 명세를 기반으로 테스트 케이스를 설계하는 기법이다.
개발 초기 테스트 케이스를 설계하는 과정에서 개발자가 발견하기 어려운 결함을 찾기 위해 사용하는 기법이다.

명세

구현하고자 하는 소프트웨어를 체계적으로 표현한 자료로, 요구 사항 분석서, 기획서, 설계서, 상태 다이어그램등이 해당된다.


동등 분할 

시스템 입력의 결과로 나타나는 결괏값이 동일한 경우 하나의 그룹으로 간주. 한 그룹 내 입력값은 어떤 값을 선택해도 항상 같은 결과를 기대할 수 있다는 전제로 함
입출력값 영역을 수학적 등가 집합으로 만든 뒤 대푯값 하나를 선택하여 테스트 케이스를 만드는 기법이다.
예를 들어 a클래스에 해당되는 입력값이 1~100이고 결괏값이 N으로 동일하다면 모든 값으로 테스트 케이스를 만들지 않고 대푯값만 선택하여 테스트 케이스를 만드는 것이다.
클래스 수가 많다면 클래스 당 입력 대푯값 하나와 클래스별 출력값을 확인했다는 것이 보장되어 테스트 커버리지를 달성한다.
이렇기 때문에 동등 분할은 모든 경우의 수에서 테스트 케이스 수를 줄일 수 있지만, 항상 같은 결과를 기대하는 것을 가정하여 테스트가 실행되고 테스트 강도가 약해서 입출력값은 방대한데 일정이나 투입 인원이 부족할 경우 샘플링 테스팅의 일환으로 사용되거나 한다.

동등 분할 기법 테스트 케이스 작성 단계

1. 입출력값을 수학적 등가 집합(클래스)의 형태로 묶기

2. 테스트 컨디션 도출하기

3. 테스트 케이스 도출하기 

테스트 일정과 투입 인력이 충분할 경우 강한 동등 분할 테스팅으로 모든 경우의 수를 테스트 할 수 있도록 설계해야 한다. 
반대로 테스트 일정과 투입 인력이 부족할 경우 약한 동등 분할 테스팅으로 등가 집합에서 하나의 대표값만 선택해서 테스트 케이스를 설계하는 형태로 활용한다.
또한 테스트할 데이터 양이 몇 천건에 해당하는 경우 약한 동등 분할 테스팅을 선택하여 등가 집합에서 하나의 대푯값에 대한 테스트를 수행하도록 설계한다.

테스트 케이스의 구성 요소와 작성 범위

TC ID: 테스트 케이스 구별 번호

카테고리: 테스트를 수행하기 위한 메뉴 위치

사전 조건: 테스트가 수행되기 위한 전제 조건

수행 절차: 주체적인 테스트 수행 단계

기대 결과: 테스트 실행 결과가 의도한 대로 동작했는지 판단하는 근거

우선순위: 시간적 제약이 있을 경우 테스트 대상을 선별하기 위한 기준

확인 결과: 수행 결과에 대한 최종 상태(PASS/FAIL/BLOCK/NI)

비고: 테스트 케이스의 의도 등 관련 내용 코멘트 

테스트 케이스 작성 범위

1. 요구 사항에 명시되어 있으나 구현 x

요구사항을 기반으로 테스트 케이스 설계, 실행

2. 요구 사항대로 구현되었으나 때에 따라 정상 동작하지 않은 경우

요구 사항을 기반으로 테스트 케이스 설계 실행

3. 요구 사항에 없으나 구현된 경우

비공식 테스트 추가 실행, 요구 사항 변경 또는 해당 부분 제거

4. 요구 사항에 없으나 구현된 부분이 정상 동작하지 않은 경우

비공식 테스트 추가 실행


경곗값 분석

동등 분할 후 각 범위의 경계에 해당되는 입력값에서 발생하는 결함의 검출 가능성을 높이기 위해 경곗값을 포함하여 테스트 케이스를 설계하는 기법

경곗값 분석 기법 테스트 케이스 작성 

테스트 케이스 도출

분류한 등가 집합에서 경계에 해당되는 값을 선택하고 테스트 컨디션으로 도출한 값을 포함하여 테스트 케이스 도출

약한 동등 분할 테스팅으로 등가 집합에서 하나의 대푯값만 선택해서 테스트 하기에 테스트 강도가 약하다고 판단될 경우 동등 분할 기법 + 경곗값 분석 기법을 함께 활용하여 테스트 강도 및 범위를 확보하고 품질을 보장하는 형태로 활용

특히 시간, 초기화 조건이 있는 이벤트 또는 콘텐츠의 경우 경곗값에서 이슈가 많이 발생하므로 이런 조건이 있는경우 반드시 경곗값 분석 기법을 적용하여 테스트 케이스 설계를 한다.


결정 테이블 테스팅

발생 조건에 따른 결과를 테이블 형태로 나열한 것이다.

시스템의 동작을 유발시키는 조건과 처리의 가능한 조합을 모두 고려하고 조합에 대한 예상 결과를 포함하여 테스트 케이스를 설계하는 기법이다.

명세서 또는 시스템 설계 자체를 테스트하는 데 주로 적용한다.

이 기법을 전체 시스템에 적용할 경우 너무 많은 경우의 수가 도출될 수 있으므로 중요한 코어 시스템에서만 사용하는 것을 권장한다.

발견할 수 있는 결함으로 명세가 잘못된 경우 명세의 불완점함과 모호함을 발견할 수 있고 입력 조건과 출력에서 액션 누락, 잘못된 액션의 원인을 발견할 수 있다.

개발 구현이 잘못된 경우 복잡한 로직 처리 실수, 시스템 동작 누락, 잘못된 동작 수행을 발견할 수 있다.


결정 테이블 테스팅 기법 테스트 케이스 작성 예시

1. 조건의 조합 생성

2. 결정 테이블로 전환하기

   (분류한 데이터의 조합을 결정 테이블로 전환(결정 테이블의 입력 조건과 동작은 참(True)과 거짓(False)로 표현)

3. 테스트 케이스 도출하기

  생성한 결정 테이블의 내용을 가능한 모든 동작을 유발시키는 조건의 조합으로 테스트 케이스를 도출
   

상태 전이 테스팅

명세를 구성하는 모델이 상태 다이어그램이면 소프트웨어가 이에 맞게 구현되어 있는지 확인하기 위해 상태 전이 테스팅 기법을 사용한다.
수행 절차가 연속된 시나리오를 가질 수 있도록 작성

테스트 케이스 도출

전형적 상태의 순서를 커버하는 방식

특정한 상태 전이 순서를 실행하는 방식

모든 상태를 커버하는 방식(유효 케이스)

불가능한 상태 전이를 테스트하는 방식(비유효 케이스)

모든 상태 전이를 커버하는 방식

발견 가능한 결함

멩세가 잘못된 경우 상태 누락, 전이, 이벤트 누락, 가드를 전이 대신 표기한 경우, 가드의 중복 또는 불일치를 발견할 수 있다. 
개발 구현이 잘못된 경우 상태 누락 또는 훼손, 잘못된 이벤트 또는 이벤트 누락, 작동 오류를 발견할  수 있다.

전이, 이벤트, 가드

전이: 한 가지 상태에서 다른 상태로 변경하는 것

이벤트: 상태의 전이를 발생시키는 요인


테스트 프로시저

시스템이 수행해야 하는 동작의 단계 테스트 실행 순서를 순차적으로 나열한 것

테스트 일정과 투입 인력이 충분할 경우: 유효, 비유효 케이스의 모든 상태를 커버하는 방식과 특정한 상태 전이 순서를 실행하는 방식을 활용하여 테스트할 수 있도록 설계

테스트 일정과 투입 인력이 부족할 경우: 적은 케이스로 많은 결함을 찾을 수 있도록 유효 케이스에 대한 모든 상태를 커버하는 방식으로 테스트 케이스를 설계


유즈 케이스 테스팅

유저와 시스템 사이 상호작용을 유저의 시각에서 표현한 시나리오, 비즈니스 시나리오 또는 프로세스 흐름을 기반으로 테스트 케이스를 설계하는 기법

유즈 케이스는 시스템을 실제로 사용하는 행위의 절차(흐름)로 기술되기 때문에 흐름상 예상하지 못했던 정보나 존재할 수 있는 결함을 발견 할 수 있고 인수 테스트나 통합 테스트 단계에서 각각의 컴포넌트 사이의 상호작용으로 발생하는 결함을 발견하는데 유용하다.

유즈 케이스 기반 테스트 케이스 도출 방법

단위 레벨 시나리오 테스트 케이스: 각 유저가 사용하는 기능 또는 시스템이 가진 기능에 초점을 맞춰 케이스를 작성, 유저 또는 시스템과 유즈 케이스 간 상호작용을 테스트할 떄 사용하거난 개별적인 유즈 케이스에 대한 단위 테스트를 수행할 떄 사용

시스템 레벨 시나리오 테스트 케이스: 유즈 케이스와 시스템 사이의 상호작용을 수행 순서에 초점을 맞춰 시나리오로 도출하는 방법이다. 

유즈 케이스 테스트 케이스를 작성할 때 요구 사항이나 공식 문서를 너무 많이 벗어나지 않도록 하고 시나리오를 이해하기 쉽게 체계적이고 정확하게 작성하는 것이 테스트 케이스의 완성도를 보장할 수 있다.


유즈 케이스 테스팅 기법 테스트 케이스 작성 예시

1. 조건의 입출력값 및 결괏값 분류

2. 테스트 케이스 도출하기

---
2024/09/10 공부기록
---


조합 테스팅

입력값을 조합해서 최대 커버리즈를 가지는 최소 개수의 테스트 케이스를 설계하는 기법이다.
테스트할 입력값의 양에 따라 입력값의 모든 조합을 테스트하는 올 컴비네션즈 테스팅, 2개의 입력값 조합을 테스트하는 페어와이즈 테스팅, 입력값을 최소 1번 이상 테스트하는 이치 초이스 테스팅으로 분류한다.
이 조합 테스팅은 의도적으로 테스트 케이스의 수를 줄여서 테스트하는 기법으로 리스크 수준은 높지만 입력값의 누락 없이 잘 조합한 최소한의 테스트 케이스로도 일정 수준의 품질을 보장할 수 있다.
조합 테스팅 기법으로 테스트 케이스를 작성할 떄 동등 분할, 경곗값 분석, 결정 테이블과 같은 다른 테스팅 기법을 이용해 테스트 데이터(입력값)를 선정하는 것이 유용하다.
조합 요소에 해당하는 대표적인 요소로는 시스템의 기능, 유저, 옵션, 조건, 처리가 해당한다. 

조합 테스팅 기법 테스트 케이스 작성 예시

1. 조건의 입력값 선정

2. 테스트 케이스 도출


2.3 구조 기반 기법

구조 기반 기법은 화이트박스 테스트로 코드, 개발 설계, 소프트웨어 구현 정보 등 구조를 보여 주는 정보를 기반으로 소프트웨어나 시스템의 내부 구조를 고려하여 테스트 케이스를 설계하는 방법이다. 
구조 기반 기법은 구문, 결정 등 코드 자체를 테스트하는 컴포넌트 레벨 구조와 한 모듈에서 다른 모듈을 호출하는 관계를 테스트하는 통합 레벨 구조 그리고 메뉴와 비즈니스 프로세스 구조를 테스트하는 시스템 레벨 구조로 구성된다.

화이트박스 테스트 블랙박스 테스트 

화이트박스 테스트 : 소프트웨어의 내부 설계 구조, 코드, 소프트웨어의 동작을 테스트하는 기법, 테스터가 소스 코드에 직접 접근하여 코드 수준에서 소프트웨어의 정확성을 검증한다.



블랙박스 테스트: 사전 지식 없이 내부 구조를 블랙박스로 보고 명세서와 입출력을 분석하여 선정한 테스트 케이스를 이용하여 시스템의 결함을 발견하는 테스트이다. 


---
2024/09/11 공부기록
---

테스트의 강도가 낮다는 것  -> 테스트된 범위와 수준이 낮아 품질에 대한 보장성이 떨어지고 약한 것
리스크가 높고 주요한 시스템일수록 테스트 강도가 높은 다중 조건 또는 조건 결정 커버리지로 테스트 범위를 달성하여 보장성을 높이고, 리스크가 낮은 소프트웨어는 테스트 강도가 낮은 커버리지를 적용

구문 커버리지
프로그램 내 모든 명령문(문장)을 1번 이상 수행하는 것, 커버리지가 가장 낮고 제어 흐름도의 모든 문장을 통과하는 한 개의 테스트 케이스가 필요하다.
결정 커버리지가 100% 달성된 경우 구문 커버리지도 100% 달성되는 것이 보장되기 때문에 최소 단위의 테스트를 해야 할 경우 구문 커버리지까지 달성이 보장되는 결정 커버리지로 테스트를 수행하는 것이 좋다. 

결정 커버리지
프로그램 내 각 분기들을 1번 이상 수행하여 구현된 코드가 예상대로 작동되는지 확인한다. 
제어 흐름도의 모든 분기들을 최소 1번씩은 통과하는 2개의 테스트 케이스가 필요하다.
결정 커버리지는 모든 분기를 한 번씩은 통과하도록 설계하기 때문에 결정 커버리지를 100% 달성할 경우 구문 커버리지도 함께 달성된다.
결정 커버리지는 테스트 커버리지가 낮아서 코어 시스템이 아닌, 문제가 발생할 때 영향도나 리스크가 낮은 시스템이나 소프트웨어를 테스트할 때 사용한다. 
일정과 투입 인력이 부족한 특수한 상황에서 적은 케이스로 많은 결함을 찾을 수 있고 주요 경로에 대한 커버리지 달성을 목표로 할때 활용할 수 있다.


조건 커버리지
프로그램 내 분기의 결과와 관계없이 개별 조건들이 참이 되는 경우와 거짓이 되는 경우를 모두 수행해서 코드가 예상대로 작동되는지 확인(분기의 결과가 같거나 달라도 무관)
개별 조건들이 참과 거짓이 되는 경우를 모두 수행하기 때문에 결정 커버리지를 포함한다고 생각할 수 있지만 분기의 결과가 참과 거짓의 모든 값을 갖는 것은 아니기 때문에 결정 커버리지를 포함하지 않음
따라서 결정 커버리지보다 조건 커버리지의 테스트 강도가 더 높다

조건 결정 커버리지
프로그램 내 분기 결과와 개별 조건들이 참과 거짓이 한 번씩 통과되도록 수행하여 구현된 코드가 예상대로 작동되는지 확인한다. 조건 커버맂와 결정 커버리지를 모두 포함한다.

변경 조건 결정 커버리지
각 개별 조건식이 다른 조건식에 무관하게 분기의 결과에 영향을 주는 경우에만 커버리지에 포함된다.
프로그램 내 모든 분기의 결과와 개별 조건의 모든 결과가 참, 거짓이 적어도 한 번씩 통과되도록 수행한다. 
결정 커버리지와 조건 결정 커버리지보다 테스트 강도가 높다. 
실무에서 일정과 인력이 부족할 경우 조건식 조합 수는 줄이지만 개별 조건식, 분기 결과가 참, 거짓이 한 번씩은 통과하여 모든 결괏값을 확인하는 커버리지를 달성하고자 할 때 활용한다. 

다중 조건 커버리지
프로그램 내 분기의 모든 조합과 개별 조건식의 모든 조합을 1번 이상 수행한다.
분기내에서 발생할 수 있는 모든 결함을 발견할 수 있고 가능한 모든 조합을 고려한 테스트로 100% 커버리지를 보장한다. 
이는 테스트 커버리지가 매우 높아서 코어 시스템이나 문제가 발생할 때 영향도나 리스크가 높은 시스템이나 소프트웨어를 테스트할 때 사용하는 것이 유용하다.
또 테스트 일정과 투입 인력이 충분할 경우, 가능한 모든 조건식의 조합을 커버할 수 있도록 테스트를 설계한다. 


2.4 경험 기반 기법
테스트 담당자의 유사 시스템 또는 프로그램에 대한 기술적 경험, 지식, 보유 능력에 기반하여 테스트 케이스를 설계하는 방법이다.
명세나 구조 기반으로 찾아낼 수 없는 범위의 테스트 케이스와 결함을 도출할 수 있다. 
테스트 담당자의 보유 지식과 경험에 의존적이기 때문에 테스트 케이스와 테스트 수행 결과의 효과성에 큰 차이가 발생할 수 있다는 단점이 있다.

오류 추정 기법(에드훅 테스팅)
테스트 담당자의 직관과 경험에 의하여 특정한 형태의 결함이 발생할 것을 예측해서 결함을 드러내도록 설계하는 테스트 기법이다.
공식 기법으로 발견할 수 없는 결함, 예측 불가능한 결함을 발생시키기는 조건과 데이터, 발생 가능한 오류를 모두 나열해서 이를 공격할 수 있도록 테스트 케이스를 설계한다.
오류 추정 기법은 기본적으로 공식적인 기법을 적용한 후에 이를 보강하는 용도로 사용하는 것이 효과적이다. 
다른 공식 기법이나 탐색적 테스팅 기법과 달기 테스트 케이스 설계 기법이 정해져 있지 않다.
오류 추정 기법의 목표인 테스트 케이스 작성 시간 최소화는 유지하면서 테스트 투입 인원에 따른 품질의 불확실성을 제거하고 일정 수준의 품질을 유지할 수 있도록 조직 단위의 공통화된 테스트 방법을 기록하고 관리한다.
기록된 데이터와 자료는 다음에 출시할 제품의 리스크를 예측하고 위험을 방지하는 데 유용하게 사용할 수 있다.

탐색적 테스팅
테스트를 실행하는 중에 테스트 대상을 분석하여 테스트를 설계하고 계획하며 실행 과정을 기록하고 결과를 평가하는 일련의 과정을 동시에 진행하는 테스트 기법이다. 
정해진 시간(1~2시간 내 수행)동안 업무를 수행하며 테스트 목표에 포함된 테스트 차터를 활용하여 테스트 결과물을 도출한다. 
테스트 차터는 테스트 대상, 범위, 목적, 수행 절차, 수행 임무, 결과 보고를 정의한 테스트 참조문서로 리스크를 분석한 기반으로 작성한다. 
테스트 대상과 방법, 발견한 이슈는 구성원에게 공유하고 해결 방법과 대응책을 마련하기까지 끊임없이 소통과 대화를 진행한다.
테스트의 마지막에는 검토 가능한 테스트 결과를 도출하고 테스트 수행중 발견한 새로운 아이디어를 기록하여 수행한 테스팅에 대한 피드백을 얻는다. 


체크리스트 
테스트에 대한 내용(테스트 절차, 범위, 주요 기능 등), 시스템 성능 평가, 기능 동작 점검 기준, 경험, 노하우 등 내용을 정리하고 나열한 목록으로 테스트를 할 때마다 누락 없이 재사용하는 것을 목적으로 작성한다.
체크리스트와 테스트 케이스의 주요한 차이점은 공식 기법을 활용하여 작성한 테스트 케이스는 기법이 주는 테스트 효과가 보장된다는 것이고 체크리스트는 이 보장성이 없다. 
공식적인 기법 외 경험 기반 테스트 기법을 주로 활용하는 이유는 공식적인 기법으로 작성한 테스트 케이스로만 테스트를 실행할 경우 해당 케이스에 한정된 결함만 발견할 것이고 수행 주체와 상관없이 동일한 결함만 발견되기 때문이다.
하지만 결함은 하나의 케이스에만 한정되어 발생하지 않으므로, 경험 기반 테스팅으로 테스트 케이스를 벗어나 발견한 결함의 주변을 탐색하여 숨은 결함들을 발견할 수 있다. 


---
3강 소프트웨어 테스트
---

3.1 API 테스트

API 시스템에 대한 엔드포인트(서버에서 리소스에 접근할 수 있도록 해주는 URL) 테스팅 활동이며 API가 예상되로 작동하고 사용할 준비가 되어 있는지 안정성, 성능, 보안 측면에서 기대치를 충족하는지 확인하는 비기능 테스트이다.
API 테스트는 프런트엔드나 클라이언트가 구축되기 전 백엔드 시스템의 내부 설계 및 통합이 완료된 후 API 엔드포인트에 대한 테스트를 수행하는 것이다. 
UI 구현을 완료한 후 애플리케이션이나 웹의 실제 유저가 사용하는 화면에서 블랙박스 테스트를 수행할 수 있지만 그러려면 서버, 데이터베이스, 클라이언트와 같은 모든 시스템과 애플리케이션 개발이 완성된 상태여야 한다. 
개발이 완료된 단계에서 엔드 투 엔드 테스트가 시작된다면 개발 초기에 해소할 수 있는 이슈에 대한 대응은 늦어질 수밖에 없다. 
API는 애플리케이션과 운영체제를 연결하여 두 소프트웨어의 구성 요소가 서로 통신할 수 있게 하는 메커니즘이다. 
API는 클라이언트에 요청을 받고 서버와의 인터페이스로 요청에 대한 응답 값을 클라이언트에 전달한다. 즉 API는 클라이언트와 애플리케이션이 서로 통신할 수 있게 연결해주는 매개체로 볼 수 있다. 

API의 종류와 유형
API는 구조에 따라 



