# Fooding CEO

| Field | Detail |
| --- | --- |
| **Primary Target** | 멀티 매장 사장님, 운영 관리자 |
| **Platform** | Web + Electron Desktop(App) |
| **Promise** | 매출/CRM/운영 현황을 한 대시보드에서 통합 분석 |

## Value Proposition
- POS, Partner, User 앱의 데이터를 하나로 묶어 **실시간 BI**를 제공합니다.
- 다수의 매장과 직원을 관리하며 **행동형 인사이트**(쿠폰 발송, 재고 발주)를 바로 실행하게 합니다.
- 커뮤니티/채팅 허브를 통해 사장님 간 정보 교류와 Fooding 지원을 통합합니다.

## Feature Highlights
- **멀티 매장 대시보드**: 매출, 예약/웨이팅, 리뷰 지표, 고객 구성, 트렌드 비교.
- **CRM & 세그먼트**: 고객 필터, 자동 캠페인, AI 템플릿, 메시지 A/B 테스트.
- **리워드/포인트샵 관리**: 등급/룰 설정, 인벤토리 관리, 쿠폰 발급 내역.
- **파트너 구매**: Fooding Partner 연동, 재고/소모품 발주, 정기배송 관리.
- **운영/커뮤니티**: 직원 공지, 채팅 허브, 교육 자료, 장애 알림.

## KPIs
- 일/주/월 활성 사장님 수, 데이터 조회 빈도, 자동 캠페인 실행 수.
- 매출/리워드/파트너 구매 증감, 커뮤니티 참여도, CEO Desktop 사용시간.

## Dependencies
- Data Warehouse(매출/리워드/고객), Analytics, Campaign 서비스, Partner API, Chat/Notification.
- Electron + React frontend, Spring WebFlux backend, Kafka 이벤트 스트림.

## Status & Plans
- ✅ CEO 포인트샵·영업시간 관리, 통합 UI 패턴(Loading/Toast), Electron 셋업.
- 🔄 커뮤니티/채팅 허브, 파트너 구매 연동, KPI 위젯 커스터마이즈, 자동화 리포트.
- 📌 차기 목표는 AI 어시스턴트 기반 요약, 이상징후 감지 알림, 다중 브랜드 모드입니다.
