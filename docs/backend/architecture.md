# Backend Architecture Overview

- **작성 목적**: Fooding 서비스 전반의 모듈/의존성을 빠르게 파악할 수 있는 참조를 제공합니다.
- **업데이트 담당**: 백엔드 리드 (변경 시 리뷰 요청)

## 서비스 구성
```
API Gateway
├── Reservation Service (WebFlux, PostgreSQL)
├── Waiting Service (WebFlux, Redis, Kafka)
├── Review Service (WebFlux, Elasticsearch, S3)
├── Loyalty Service (WebFlux, PostgreSQL, Redis)
├── Payment Service (PG 연동, Vault)
├── CRM/Chat Service (WebFlux, MongoDB, Kafka)
└── Partner Commerce Service (Spring MVC, MySQL)
```

## 핵심 패턴
- **Event Streaming**: Kafka 토픽(`reservation.events`, `waiting.events`, `loyalty.points`)으로 cross-domain 동기화.
- **Realtime**: SSE 서버가 Waiting/Loyalty 이벤트를 push, POS/App이 구독.
- **데이터 계층**: PostgreSQL(거래), Redis(캐싱), Elasticsearch(검색), Kafka(비동기), S3(미디어).
- **Observability**: Grafana/Loki/Tempo 스택 + APM(New Relic). 알람 룰은 `runbooks/incident-response.md` 참고.

## 다이어그램
- 최신 다이어그램 파일: `assets/backend-architecture.drawio`
- 경로: `projects/fooding/docs/backend/assets/backend-architecture.png`
