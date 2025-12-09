# CI/CD Pipeline Overview

| Stage | Tooling | Description |
| --- | --- | --- |
| Lint/Test | GitHub Actions (`ci.yml`) | PR마다 lint, unit/integration 테스트 실행 |
| Build | GitHub Actions + Docker Buildx | 다중 아키텍처 이미지 빌드, SBOM 생성 |
| Security | Trivy, Snyk | 이미지 스캔, 의존성 CVE 체크 |
| Deploy | Argo CD | main/production 브랜치 기준으로 EKS 배포 |
| Release | Slack + Notion | 배포 로그, 릴리스 노트 자동 게시 |

## Flow
1. PR merge → `build-and-push` 워크플로가 이미지 태그(`service:git-sha`) 생성.
2. Argo CD가 Helm values 업데이트 감지 → 자동 Sync.
3. 배포 완료 후 Slack webhook으로 상태 통지, Sentry 릴리스 트래킹.

## 추가 참고
- 프론트엔드 Storybook/앱 배포 파이프라인: `projects/fooding/docs/frontend/guides/component-library.md`
- 배포 절차 상세: `deploy-playbook.md`
