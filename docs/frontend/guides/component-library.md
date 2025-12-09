# Component Library Guide

- **Scope**: React Native + Web 컴포넌트, Storybook 문서화, 디자인 시스템 토큰 적용 방식을 정리합니다.
- **마지막 업데이트**: TODO(작성 시 갱신)

## Principles
1. 모든 공용 UI는 Storybook 스토리와 Doc 블록을 함께 작성합니다.
2. 디자인 토큰(색상, 타이포, 스페이싱)은 `@fooding/theme` 패키지에서만 import합니다.
3. 컴포넌트 props는 `aria`/접근성 속성을 기본 포함하고, 테스트 ID 명명 규칙(`ft-<scope>-<component>`)을 맞춥니다.

## Checklist
- [ ] 신규 컴포넌트 → Figma 링크 / 시나리오 링크 추가.
- [ ] Storybook Controls 정의.
- [ ] Jest/RTL 스냅샷 or 인터랙션 테스트.
- [ ] 디자인 리뷰 완료 상태 캡처를 `assets/component-library/`에 보관.

## References
- 디자인 시스템: `projects/fooding/docs/design/guides/design-system.md`
- Storybook 배포 파이프라인: `projects/fooding/docs/backend/cicd/pipeline-overview.md`
