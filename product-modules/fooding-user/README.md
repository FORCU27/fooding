# Fooding User

| Field | Detail |
| --- | --- |
| **Primary Target** | 외식 고객(탐색 → 예약/웨이팅 → 방문 → 리뷰 → 리워드) |
| **Value Promise** | 신뢰 가능한 리뷰와 편리한 방문 경험을 단일 앱에서 제공 |
| **Current Stage** | 출시(안드로이드/웹), iOS 런치 준비 |

## Value Proposition
- 지역 기반 검색과 인증 리뷰를 결합해 **실제 방문 이력** 중심의 추천을 제공합니다.
- 예약, 웨이팅, 리뷰, 리워드까지 끊김 없는 여정을 설계해 재방문률을 높입니다.
- Fooding 통합 포인트/쿠폰과 연동돼 **교차 채널 리워드**를 경험하게 합니다.

## User Journey
1. 홈/탐색: 지역, 취향, 상황(모임/데이트 등) 기반 큐레이션.
2. 식당 상세: 실시간 좌석/웨이팅 정보, 사진, 인증 리뷰, 시그니처 메뉴.
3. 예약/웨이팅: 좌석 선택, 보증금/노쇼 정책 확인, 예상 대기시간 안내.
4. 방문 인증: 체크인 → 주문 연동 → 리뷰 작성 → 포인트 적립.
5. 마이페이지: 쿠폰/포인트, 다녀온 식당, 저장 리스트, 커뮤니티 활동.

## Core Capabilities
- **검색/추천**: Elasticsearch + AI 랭킹으로 개인화된 추천 피드.
- **예약·웨이팅**: 실시간 슬롯, 자동 알림, 이동시간 보정, 친구 공유.
- **리뷰/UGC**: 방문 인증 기반 리뷰, 포토/영상 첨부, 신고 및 품질 필터.
- **리워드/쿠폰**: 방문 미션, 등급별 적립률, 쿠폰북, 포인트샵 연동.
- **커뮤니케이션**: 매장/CS 채팅, 방문 전 알림, 후기 피드백에 대한 사장님 답글.

## KPIs & Dashboards
- MAU / WAU, 신규 예약률, 웨이팅 전환률, 리뷰 작성률, 재방문률.
- 리워드 적립 대비 사용 비율, NPS, 앱 스토어 평점.
- 데이터는 `metrics/kpi.md` 및 App Analytics 대시보드에 반영.

## Dependencies
- Backend: Reservation, Waiting, Review, Loyalty, Payment, Notification 서비스.
- Infra: PostgreSQL(트랜잭션), Redis(세션/큐), Kafka(이벤트 스트림), Elasticsearch(검색), FCM/APNS(푸시).
- 외부: 지도/주소 API, 결제 PG, 소셜 로그인.

## Status & Next Steps
- ✅ 실시간 대기 UI, 리뷰/쿠폰/마일리지 UX 개선, Loading/Toast 패턴 통일.
- 🔄 iOS 빌드, 친구 초대 리워드, AR 기반 대기열 안내, 포인트샵 내 인벤토리 추천.
- 📌 향후에는 리뷰 신뢰도 지수(리워드/방문/사진)와 생성형 요약을 도입 예정.
