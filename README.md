# Fooding · All-in-One Restaurant Platform

> Fooding은 예약, 웨이팅, POS, 리워드, B2B 파트너 마켓까지 외식업 운영의 전 과정을 하나의 플랫폼으로 통합합니다.

## Contents
- [Fooding · All-in-One Restaurant Platform](#fooding--all-in-one-restaurant-platform)
  - [Contents](#contents)
  - [Overview](#overview)
  - [Live Links \& Downloads](#live-links--downloads)
    - [Public Sites](#public-sites)
    - [App Downloads](#app-downloads)
  - [Product Modules](#product-modules)
  - [Core Capabilities](#core-capabilities)
  - [Tech \& Architecture](#tech--architecture)
  - [Business Model](#business-model)
  - [Progress Highlights](#progress-highlights)
    - [Roadmap Snapshot](#roadmap-snapshot)
  - [Metrics \& Impact](#metrics--impact)
  - [Team](#team)
  - [Repository Layout](#repository-layout)

## Overview
- **Vision**: 외식업 디지털 전환을 선도하는 No.1 플랫폼. 사장님과 손님 모두에게 단일 경험을 제공합니다.
- **Problem Statements**
  - 사장님은 예약, POS, 웨이팅, 마케팅, 식자재 구매를 서로 다른 서비스로 관리해야 하고, 높은 수수료와 데이터 분산 문제가 있습니다.
  - 손님은 신뢰할 수 있는 리뷰, 편리한 예약·웨이팅, 통합 리워드가 부족합니다.
- **Solution**
  - 통합 앱과 POS, CEO 도구로 매장 운영 전 과정을 자동화.
  - Fooding Partner 마켓으로 식자재/설비를 도매가에 공급.
  - Fooding User 앱으로 탐색부터 방문, 리뷰, 리워드까지 일관된 사용자 여정 제공.

## Live Links & Downloads
### Public Sites
- **Fooding User**: [https://fooding.im/](https://fooding.im/)
- **Fooding CEO Web**: [http://ceo.fooding.im/](http://ceo.fooding.im/)

### App Downloads

| Product | Android | iOS | Windows | Mac |
| --- | --- | --- | --- | --- |
| Fooding POS | _TBD_ | _TBD_ | _TBD_ | _TBD_ |
| Fooding 매장관리 앱 | _TBD_ | _TBD_ | _TBD_ | _TBD_ |

## Product Modules
> 모듈별 폴더(`projects/fooding/product-modules/<module>/`)에 README와 이미지/다이어그램(`assets/`)을 함께 보관합니다.
| Module | Target | 핵심 기능 |
| --- | --- | --- |
| **Fooding User** | 고객 | 지역 기반 검색, 상세 정보, 예약/웨이팅, 인증 리뷰, 통합 포인트 |
| **Fooding POS** | 매장 | 테이블/QR 주문, 주방 관리, 예약·웨이팅 현황, 결제, CRM, 리워드 통합 |
| **Fooding App (매장용)** | 사장님/직원 | 모바일 웨이팅/예약 관리, 포인트 적립, 쿠폰 발급, 키오스크 연계 |
| **Fooding Place** | 매장 | Zapp 기반 노코드 웹사이트 빌더, 템플릿, SEO, Fooding 예약 연동 |
| **Fooding Partner** | B2B | 식자재·설비·서비스 마켓플레이스, 대량/정기 구매, 입점 지원 |
| **Fooding CEO** | 사장님 | 멀티 매장 대시보드, 매출/CRM 분석, 커뮤니티, 파트너 구매, 채팅 허브 |

## Core Capabilities
- **예약 시스템**: AI 추천, 좌석 선택, 보증금/노쇼 정책, 자동 알림.
- **웨이팅 시스템**: 원격 등록, 실시간 대기 현황, 알림, 이동 시간 보정, 키오스크 연계.
- **리뷰/리워드**: 방문 인증 리뷰, 포토/텍스트/영상 리워드, 등급별 적립률, 통합 쿠폰/포인트샵.
- **CRM & 채팅**: 고객 세그먼트, 자동 템플릿, 직원/매장/파트너 커뮤니티, AI 어시스턴트.
- **스토어 웹 & 마켓**: 노코드 사이트, SNS 연동, B2B 마켓 입점/거래, 정기배송/후불결제.

## Tech & Architecture
```
Fooding Platform
├── Client Apps: User (iOS/Android), CEO, POS, Store App, Web Place
├── Core Services: Reservation, Waiting, Review, Loyalty, Payment, CRM, Chat, Community, AI Assistant
├── Data & Infra: PostgreSQL, Redis, Kafka, Elasticsearch, MongoDB, S3, Realtime Server (SSE), FCM/APNS
└── Ops: Gateway, Job Service, Analytics, Monitoring
```
- **Frontend**: React Native 기반 멀티 앱, Storybook 컴포넌트, Electron(CEO Desktop), Tailwind 기반 디자인 시스템.
- **Backend**: Spring(WebFlux) 마이크로서비스, QueryDSL, Kafka 이벤트, Elasticsearch 검색, Redis 캐시, SSE 기반 실시간 스트림.
- **DevOps**: Docker Compose 스택(ES, Kafka, UI), k6 성능 테스트 계획, Gateway rate-limit, 배포용 Job & Analytics 파이프라인.

## Business Model
- **플랫폼 수수료**: 파트너 거래액 5~10%, 노쇼 보증금 일부 수수료, 프리미엄 노출.
- **구독 플랜**: POS 스타터(무료) → 프로(99,000원) → 엔터프라이즈(299,000원), Place 프리미엄(29,000원) 등급.
- **Partner Benefits**: 도매가 제공(최대 50% 절감), 무료 배송, 후불결제, 정기배송 추가 할인.
- **차별화 포인트**: All-in-One 통합, 낮은 수수료, 양면 네트워크 효과, AI 기반 인사이트.

## Progress Highlights
최근 스프린트와 worklog에서 완료된 대표 항목들:
- **Frontend** (`features/frontend.md`): 사용자 실시간 대기 UI, 리뷰/쿠폰/마일리지 UX 개선, CEO 포인트샵·영업시간 관리, 전반적인 Loading/Toast 패턴 적용, 앱 QA 1차 진행.
- **Backend** (`features/backend.md`): 단골/쿠폰/포인트샵 API, Kafka · Elasticsearch 고도화, WebFlux 기반 realtime 모듈, SSE 웨이팅/적립 스트림, StorePost/Review/통계 API 확장, 캐시 stampede 방지 Job.
- **Design & Product Planning** (`features/plan.md`): POS/CEO 체계화, 리워드·쿠폰·포인트샵·웨이팅·리뷰 등 주요 도메인 기획 완료, 예약/Place 확장 기획 준비.

### Roadmap Snapshot
- ES/Redis/Kafka 고도화 및 성능 버퍼링.
- Realtime gateway 개선과 캐시 기반 추천(함께 본 식당 등).
- Place/Partner 도메인 API 확장과 예약/사이트 통합 고도화.

## Metrics & Impact
- 입점 매장 50,000+, 월간 사용자 3,000,000+, 앱 다운로드 10,000,000+.
- 월간 예약 500,000건, 웨이팅 1,000,000팀, 리뷰 100,000건, POS 거래 3,000억 원.
- 사장님 평점 4.8/5.0, 평균 매출 증가 35%, 재사용률 85%.

## Team
| Name | Role | Email | Key Work | Links |
| --- | --- | --- | --- | --- |
| 강주영 | 팀장 · Product/Infra | karjyk@gmail.com | 프로젝트 총괄, 인프라/CI, 전사 문서화 | [Blog](https://velog.io/@kkang_/posts) · [LinkedIn](https://www.linkedin.com/in/jooyoung-kang-770577160/) |
| 정영현 | Backend | jeongyounghyeon1106@gmail.com | 웨이팅 알림 SSE, Gateway 구성, 캐시 최적화 | [GitHub](https://github.com/Jeongyounghyeon) · [LinkedIn](https://www.linkedin.com/in/%EC%98%81%ED%98%84-%EC%A0%95-7129a3320/) |
| 김지연 | Frontend | cleo0718@gmail.com | User 앱 개발, User/CEO UI 고도화, 리뷰·웨이팅·포인트 UX | [GitHub](https://github.com/CLEO525) · [LinkedIn](https://www.linkedin.com/in/cleo0718) |
| 진혜민 | Backend | hmjin11@gmail.com | 리워드/포인트샵·스토어 검색/ES·Kafka 구축 | [GitHub](https://github.com/hmJin11) · [LinkedIn](https://www.linkedin.com/in/hyemin-jin-b09709393) |
| 고윤아 | Design | ko.yuna0412@gmail.com | User 앱 전반 디자인, 마케팅 에셋 | [GitHub](https://github.com/bnb0412) · [LinkedIn](https://www.linkedin.com/in/%EC%9C%A4%EC%95%84-%EA%B3%A0-2804a8306/) |
| 김모경 | Frontend | monee1001@naver.com | CEO 고객관리·계정 플로우, 리워드 매장관리 앱 | [GitHub](https://github.com/moneekim) · [LinkedIn](https://www.linkedin.com/in/%EB%AA%A8%EA%B2%BD-%EA%B9%80-7a7a33268/) |
| 이원종 | Frontend | leewj5192@gmail.com | 웨이팅 매장관리 앱, CEO 앱/Electron·RN 셋업 | [GitHub](https://github.com/leewj5192) · [LinkedIn](https://www.linkedin.com/in/%EC%9B%90%EC%A2%85-%EC%9D%B4-4a0b19266/) |
| 지윤서 | Design | jysjys7620@naver.com | CEO/APP/POS 멀티 채널 디자인 & 배포 이미지 | [LinkedIn](https://www.linkedin.com/in/younseo-ji-10a5053a0) |
| 임성제 | Backend | seongje00416@gmail.com | WebFlux realtime 모듈, 리워드 알림 SSE, Review/StorePost 확장 | [GitHub](https://github.com/seongje00416) · [Blog](https://www.notion.so/seongje00416/4c36eb99dd704af8b7356173ef0cb247?v=18df116d5c724a3794e5ef8fcd58c77e&source=copy_link) |
| 신상호 | Frontend | nononcrust@gmail.com | 앱 파비콘/브랜딩 에셋, 디자인 시스템 도입, 배포 아이콘 운영 | [Blog](https://nonon.dev/) · [GitHub](https://github.com/orgs/FORCU27/people/nononcrust) |

> 개인별 상세 프로필은 `projects/fooding/members/` 디렉터리를 참고하세요.

## Repository Layout
```
projects/fooding/
├── fooding.md            # 서비스 풀 스펙 문서
├── README.md             # 깃허브 소개 문서 (본 문서)
├── features/             # 영역별 worklog (frontend/backend/design/infra/plan)
├── members/              # 팀원 목록 및 개인 프로필
└── ...                   # 산출물 확장 예정 (deliverables, metrics 등)
```
