# State Management Playbook

- **Scope**: React Query, Zustand, Redux Toolkit 사용 지침 및 캐시 전략.
- **업데이트 주기**: 분기별(스프린트 회고 후 필요 시 즉시)

## Layering
1. **Server State**: React Query (key = `domain/feature/params`), staleTime 기본 60s.
2. **Client State**: Zustand store별 책임 분리 (`useReservationStore`, `useReviewStore` 등).
3. **Global UI State**: Context minimal, toast/loading은 `ui-store`에서 중앙 관리.

## Patterns
- Mutation 후 invalidate: `queryClient.invalidateQueries({ queryKey: [...] })`를 정책화.
- SSE/웹소켓 수신 데이터는 store에서 push하고 React Query `setQueryData`와 동기화.
- Deep link/네비게이션 상태는 `routing.md` 참고.

## Diagnostics
- Devtools(React Query, Zustand) 스냅샷을 `assets/state/`에 저장해 버그 공유.
- 크래시/메모리 이슈는 `projects/fooding/docs/backend/runbooks/incident-response.md`에 연계 기록.
