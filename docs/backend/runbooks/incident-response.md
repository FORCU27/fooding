# Incident Response Runbook

## 트리아지
1. PagerDuty/Slack Alert 수신 → 담당자 확인.
2. 장애 레벨 결정 (P0/P1/P2) 및 타임라인 기록 시작.
3. 고객 영향 범위 파악: 예약/웨이팅/결제 등 영향 도메인.

## 공통 대응
- **Monitoring**: Grafana(서비스 지표), Loki(로그), Tempo(트레이싱) 순으로 확인.
- **릴리즈 여부**: 최근 배포 있었는지 `backend/cicd/deploy-playbook.md`와 비교.
- **Rollback**: Helm/Argo CD에서 이전 Revision으로 롤백.

## 커뮤니케이션
- 15분 내 `#fooding-incident`에 업데이트.
- 고객 공지 필요 시 CS/비즈니스 팀과 협업하여 템플릿 사용.

## 포스트모템
- 48시간 내 RCA 문서 작성 (템플릿 TBD).
- 개선 액션은 `planning/backlog.md`에 티켓 링크 후 추적.
