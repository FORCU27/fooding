# Backend Knowledge Base

Fooding 백엔드/인프라 팀의 기준 문서를 모은 디렉터리입니다. 시스템 구조, 인프라 구성, CI/CD 파이프라인, 운영 Runbook을 분리해 관리합니다.

## Structure
```
backend/
├── README.md
├── architecture.md
├── infra/
│   └── overview.md
├── cicd/
│   ├── pipeline-overview.md
│   └── deploy-playbook.md
├── runbooks/
│   └── incident-response.md
└── assets/
    └── (다이어그램, 시퀀스 차트 등)
```

## 운영 원칙
1. 다이어그램/아키텍처 PNG, draw.io, Excalidraw 파일은 `assets/`에 저장합니다.
2. 인프라 IaC 소스는 별도 레포에 있더라도, 개념/구성도는 `infra/` 문서로 싱크합니다.
3. 배포/장애 대응 절차는 Runbook 형태로 유지하며, 변경 시 슬랙 공지와 함께 문서를 업데이트합니다.
