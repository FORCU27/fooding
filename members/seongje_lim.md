# 임성제 (Seongje Lim)

## 1. 프로필 (Profile)
- **Role**: Backend Developer
- **Email**: seongje00416@gmail.com
- **Links**:
  - [GitHub](https://github.com/seongje00416)
  - [Blog](https://www.notion.so/seongje00416/4c36eb99dd704af8b7356173ef0cb247?v=18df116d5c724a3794e5ef8fcd58c77e&source=copy_link)

## 2. 상세 기여 내역 (Contribution Details)
### Backend Development
- WebFlux 기반 realtime 모듈을 구성(`BE-397`, `BE-406`)하고 POS 적립·웨이팅 API를 SSE로 전환(`BE-408`, `BE-409`).
- CEO/User Review·StorePost·ID/PW 찾기 등 고객 커뮤니케이션 기능을 확장(`BE-396`, `BE-422~BE-426`).
- 신규 API의 캐시/알림 연계를 설계(`BE-432`, `BE-444`, `BE-451`, `BE-455`)해 성능과 마케팅 자동화를 동시에 달성했습니다.

### 주요 담당 기능
- Realtime 서버/게이트웨이 연계, POS 적립/웨이팅 SSE
- CEO 리뷰/답글/사용자 응답 필드 개선
- 새로 오픈 식당 캐시/이메일·SMS 템플릿 정비

## 3. 작성했던 포인트 (Key Points)
*기술적 챌린지 및 해결 과정*
- WebFlux 전환 과정에서 기존 블로킹 코드를 리팩터링하며 성능 향상과 리소스 절감을 이뤘습니다.
- Review/StorePost API 확장 시 도메인 간 권한 이슈를 정리해 CEO·User·Admin 요구를 충족했습니다.
- 캐시 stampede 방지 job을 설계해 인기/신규 식당 데이터가 안정적으로 갱신되도록 했습니다.

## 4. 팀원들에 대한 의견 (Feedback on Teammates)
*협업 과정에서의 피드백*
- 프론트와 스펙 협의를 밀도 있게 진행해 WebFlux 전환 후에도 API 응답 스키마가 유지되도록 했습니다.

## 5. 회고 (Retrospective)
- 실시간/캐시/마케팅 도메인을 동시에 다루며 비동기 이벤트 흐름을 체계적으로 설계하는 경험을 쌓았습니다. 향후에는 WebFlux 기반 테스트/모니터링 툴체인을 강화해 회귀 리스크를 줄이고자 합니다.
