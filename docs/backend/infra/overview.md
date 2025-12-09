# Infra Overview

| Layer | Stack | Notes |
| --- | --- | --- |
| Cloud | AWS | VPC 3-tier (public/private/data), Seoul 리전 주 사용 |
| Container | EKS + Fargate | 서비스별 네임스페이스, HPA + KEDA 적용 |
| Data | RDS(PostgreSQL), Elasticache(Redis), MSK(Kafka), OpenSearch | 멀티 AZ 구성 |
| Storage | S3, EFS | 정적 자산/로그 |
| Networking | API Gateway(ALB), NLB(Websocket/SSE), CloudFront | Zero-trust with AWS SSO |

## IaC & 관리
- Terraform 모듈 레포: `infra/terraform` (별도 저장소) → 변경 시 PR 링크를 본 문서에 기록.
- Helm 차트: `charts/<service>` (Gateway, backend services, jobs).
- Secret 관리: AWS Secrets Manager + SOPS.

## 운영 참고
- 새 리소스 추가 시 `Change Request` 템플릿 작성 → 보안 리뷰 이후 merge.
- 장애/장애조치 절차는 `../runbooks/incident-response.md` 참고.
