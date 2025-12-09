# Design → Engineering Handoff Checklist

## 공통
- [ ] Figma 파일 버전 태그 (예: `v1.2-ready`).
- [ ] 컴포넌트/토큰 변경 사항 정리 → `design-system.md` 업데이트 여부 확인.
- [ ] 인터랙션/모션 명세 첨부 (Lottie, mp4 등은 `design/assets/handoff/`에 저장).

## 프론트엔드 전달
- [ ] 화면별 breakpoints, 상태별 UX 정리.
- [ ] API/데이터 의존성 명시 (예: 예약 상태, 웨이팅 지표).
- [ ] QA 체크리스트 업데이트 요청 (`frontend/guides/qa-release-checklist.md`).

## 백엔드 전달
- [ ] 새 데이터 모델/필드 요구사항, validation 규칙.
- [ ] 알림/푸시/채팅 등 타 도메인 연계 포인트 정리.
- [ ] KPI/트래킹 정의 → `features/plan.md`와 동기화.
