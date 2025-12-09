# 정영현 (Younghyeon Jeong)

## 1. 프로필 (Profile)
- **Role**: Backend Developer
- **Email**: jeongyounghyeon1106@gmail.com
- **Links**:
  - [GitHub](https://github.com/Jeongyounghyeon)
  - [LinkedIn](https://www.linkedin.com/in/%EC%98%81%ED%98%84-%EC%A0%95-7129a3320/)

## 2. 상세 기여 내역 (Contribution Details)
### Backend Development
- 실시간 웨이팅/적립 스트림을 위해 SSE 전환(`BE-363`, `BE-409`, `BE-411`)과 realtime 서버 아키텍처를 구현했습니다.
- 통계/통합 데이터 파이프라인(`BE-389`, `BE-402~BE-404`, `BE-421`, `BE-428`)을 설계하여 CEO 대시보드에 필요한 지표를 생성했습니다.
- Gateway/Job/캐시 영역(`BE-398`, `BE-427`, `BE-443`, `BE-442`)을 담당하며 요청 제한, 캐시 stampede 방지 job 등을 구축했습니다.
- 메뉴/웨이팅/유저 API 개선(`BE-135`, `BE-365`, `BE-436`)으로 사용자 및 POS 앱의 안정성을 높였습니다.

### 주요 담당 기능
- Realtime 웨이팅/적립/알림 스트림
- 매장 통계/잡 시스템 및 게이트웨이 운용
- 인기/최근 본 식당 캐시 및 Redis 최적화

## 3. 작성했던 포인트 (Key Points)
*기술적 챌린지 및 해결 과정*
- SSE 전환 시 Redis/Kafka 간 backpressure 이슈를 해결하며 안정적인 실시간 경험을 제공했습니다.
- 통계 Job에서 발생한 rollback-only 문제(`BE-421`)를 해결하며 일별 지표 생성의 신뢰도를 확보했습니다.
- 캐시 갱신/분산락 작업(`BE-439~BE-448`)을 계획해 동시성 이슈를 선제적으로 막을 수 있는 구조를 설계했습니다.

## 4. 팀원들에 대한 의견 (Feedback on Teammates)
*협업 과정에서의 피드백*
- 프론트/인프라와 밀접히 협력해 실시간 기능 배포 시 모니터링·게이트웨이 설정까지 일괄로 챙겼습니다.

## 5. 회고 (Retrospective)
- 실시간 요구사항이 많은 서비스에서 게이트웨이·Job·캐시를 하나의 관점으로 바라보는 것이 중요함을 깨달았습니다. 앞으로는 부하 테스트와 관측 지표를 더욱 촘촘히 해 사전 대응력을 높이고 싶습니다.
