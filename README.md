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


