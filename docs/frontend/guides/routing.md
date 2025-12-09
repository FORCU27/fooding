# Routing & Navigation

- **앱 범위**: React Navigation (User/Store App), Electron Router (CEO), Next.js (웹).

## Naming & Structure
- Stack ID: `<app>-<domain>-stack` (예: `user-discovery-stack`).
- Deep link scheme: `fooding://<route>?params`. 웹 공유용 링크는 `https://fooding.im/app/<route>`.
- Route params는 `Zod` 스키마로 검증하고 `useRouteParams` 훅으로 공통 처리.

## Cross-App Links
- User 앱 → CEO/App: `Linking.openURL('fooding-ceo://...')` 대신 `BridgeService`를 거쳐 권한 체크.
- 웹 Place → User 앱: Smart App Banner + fallback web view.

## Checklist
- [ ] 신규 라우트는 analytics 태깅(`screen_view`)을 정의했는가?
- [ ] 접근 제어(로그인/권한) 훅이 적용되었는가?
- [ ] Deep link 테스트 케이스를 QA 체크리스트에 추가했는가?
