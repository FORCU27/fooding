# 진혜민 (Hyemin Jin)

## 1. 프로필 (Profile)
- **Role**: Backend Developer
- **Email**: hmjin11@gmail.com
- **Links**:
  - [GitHub](https://github.com/hmJin11)
  - [LinkedIn](https://www.linkedin.com/in/hyemin-jin-b09709393)

## 2. 상세 기여 내역 (Contribution Details)
### Backend Development
- `BE-215~237` 단골/포인트샵/쿠폰 CRUD, 로그인 예외 처리 등 회원·리워드 핵심 API를 설계하고 운영했습니다.
- `BE-242~257`에서 Elasticsearch·Kafka 스택을 구축하고 docker-compose/Kafka UI 등 로컬 개발 인프라를 표준화했습니다.
- 스토어 도메인 개선(`BE-329~373`)으로 매장 이미지/필터/최근 본 식당/포인트샵 조회까지 사용자 경험을 고도화했습니다.
- `BE-214`, `BE-372` 등으로 웨이팅 SSE와 메뉴판 API를 추가해 멀티 채널 서비스 간 일관성을 맞췄습니다.

### 주요 담당 기능
- 리워드/포인트샵/쿠폰: CRUD, 로그인/구매 로직, 이벤트 기반 평균가 업데이트, 쿠폰 사용내역 API.
- 스토어 검색/필터: Elasticsearch 전환, 추천 API, 캐시/정렬 고도화, 북마크·최근 본 목록 확장.
- 인프라 연동: Kafka/ES/Redis 초기 구성, docker-compose 표준화, Kafka 이벤트 기반 처리.

## 3. 작성했던 포인트 (Key Points)
*서버 성능 개선 및 트러블 슈팅*
- ES 검색 전환(`BE-252`, `BE-344~347`)과 캐시 전략으로 스토어 검색 응답을 안정화하고 필드 확장을 빠르게 반영했습니다.
- Kafka/이벤트 기반 구조(`BE-278`, `BE-348`)로 평균 가격/리워드 적립 로직의 일관성을 확보했습니다.
- 웨이팅 SSE/캐시 작업에서 Redis/Kafka 성능 이슈를 모니터링하며 장애 없이 전환했습니다.

## 4. 팀원들에 대한 의견 (Feedback on Teammates)
*협업 과정에서의 피드백*
- FE/디자인과 긴밀하게 API 스펙을 조율해 사용자·사장님 앱 모두에서 요구하는 데이터를 빠르게 제공했습니다.

## 5. 회고 (Retrospective)
- 쿠폰·리워드·스토어 등 다양한 도메인을 동시에 다루며 도메인 이벤트 설계의 중요성을 체감했습니다. 향후에는 테스트 자동화 범위를 더 넓혀 신규 기능 추가 시 회귀 부담을 줄이고 싶습니다.
