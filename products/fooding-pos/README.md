# Fooding POS

| Field | Detail |
| --- | --- |
| **Primary Target** | 매장 운영팀(홀/주방/카운터) |
| **Value Promise** | 주문, 주방, 결제, CRM을 하나의 화면에서 통합 관리 |
| **Deployment** | Windows/Mac 앱(계획), 웹 관리 콘솔, 하드웨어 연동 |

## Operational Goals
- 테이블 회전율과 주문 정확도를 높이고, 주방·홀 간 커뮤니케이션을 단축합니다.
- 매장 내 웨이팅/예약 현황과 POS 주문을 실시간 동기화해 이중 입력을 제거합니다.
- 고객 데이터(적립, 쿠폰, 방문 기록)를 POS 내에서 바로 활용하게 합니다.

## Core Features
- **테이블/QR 주문**: 테이블 매핑, QR 주문, 합석/이석 처리, 메뉴 옵션 제어.
- **주방/제조 관리**: KDS 연동, 주문 단계(접수 → 조리 → 서빙), 알림음/대기열.
- **결제/정산**: 카드/현금/QR 결제, 멤버십 할인, 부분 결제, 후불 정산.
- **예약/웨이팅 통합**: 사전 주문, 예상 도착 알림, 좌석 자동 배정.
- **CRM/리워드**: 방문 고객 식별, 포인트 적립, 쿠폰 사용, 단골 메모.
- **오프라인 모드**: 네트워크 이슈 시 로컬 큐에 저장 후 복구 동기화.

## Metrics
- 주문 처리 시간, 테이블 회전률, POS → 주방 전달 지연, 오프라인 모드 사용 빈도.
- 쿠폰 사용률, 적립 처리 속도, POS 내 신규 고객 등록 수.

## Integrations & Dependencies
- Hardware: 영수증 프린터, 캐시드로어, 키오스크, 바코드 스캐너.
- Services: Ordering, Payment, Loyalty, CRM, Inventory, Notification.
- Infra: Electron 앱 + WebFlux API, Kafka 이벤트 버스(KDS, 리포트), Redis 캐싱.

## Roadmap
- ✅ WebFlux 기반 realtime 모듈, SSE 웨이팅/적립 스트림 연동.
- 🔄 POS 스타터/프로 플랜 구성, 키친 디스플레이 다중 화면, 다국어 UI.
- 📌 장기적으로는 AI 기반 예상 주문량, 재고 자동 발주, 하드웨어 배포 자동화 예정.
