# QA & Release Checklist

Release 전 반드시 검증해야 할 항목을 영역별로 정리합니다.

## 공통
- [ ] 버전/빌드 넘버 증분 확인.
- [ ] 환경 변수(.env, config.ts) 검증.
- [ ] Storybook/Docs 배포 성공 여부.

## User App
- [ ] 예약/웨이팅 메인 플로(신규/취소/알림) 테스트.
- [ ] 리뷰 작성/업로드, 미디어 권한 확인.
- [ ] 리워드 적립/사용, 잔액 동기화.

## CEO & Store App
- [ ] 멀티 매장 스위치, 권한별 화면 제한.
- [ ] POS/App 동기화 (웨이팅/예약/포인트 이벤트) 실시간 확인.
- [ ] Electron 자동 업데이트 채널 검사.

## 제출 후
- [ ] Crashlytics/Sentry 모니터링 룰 업데이트.
- [ ] QA 리포트 → `features/frontend.md` worklog 링크.
- [ ] 필요한 캡처/비디오는 `frontend/assets/releases/`에 저장.
