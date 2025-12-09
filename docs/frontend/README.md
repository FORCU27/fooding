# Frontend Knowledge Base

Fooding 프론트엔드 팀이 공유해야 할 장기 지식과 프로세스를 모아둔 공간입니다. `features/frontend.md`와 같은 워크로그는 단기 기록으로 두고, 여기에는 아키텍처·패턴·체크리스트 등 재활용 가능한 내용을 유지합니다.

## Structure
```
frontend/
├── README.md
├── guides/
│   ├── component-library.md
│   ├── state-management.md
│   ├── routing.md
│   └── qa-release-checklist.md
└── assets/
    └── (스토리북 캡처, 사용자 플로 다이어그램 등)
```

## 문서 업데이트 가이드
1. 새로운 가이드가 필요하면 `guides/` 하위에 Markdown 파일을 추가하고, 상단에 목적·적용 범위를 명시합니다.
2. UX 플로, 컴포넌트 트리 등 시각 자료는 `assets/`에 저장하고 문서에서 상대 경로로 참조합니다.
3. 변경 이력/날짜는 문서 상단에 간단히 기재해 팀원이 최신 내용을 빠르게 확인하도록 합니다.
