# Deploy Playbook

## 사전 체크
- [ ] 릴리스 노트 초안 (`projects/fooding/releases/release-notes.md`) 업데이트.
- [ ] Feature flag 상태 확인.
- [ ] DB 마이그레이션 검토(롤백 플랜 작성).

## 절차
1. `main` → `production` 브랜치에 cherry-pick 및 버전 태깅.
2. Argo CD Dashboard에서 해당 애플리케이션 Sync 확인.
3. HPA/Pod 상태가 안정화될 때까지 Grafana 대시보드 모니터링.
4. Smoke 테스트 스크립트 실행 (API health, 핵심 플로).

## 배포 후
- [ ] Sentry/New Relic 알람 여부 확인.
- [ ] Slack `#fooding-release`에 결과 공유.
- [ ] 문제가 있을 경우 `runbooks/incident-response.md` 절차에 따라 롤백.
