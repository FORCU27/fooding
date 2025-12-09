# Design Knowledge Base

디자인 시스템, 리서치, 핸드오프 가이드를 정리한 공간입니다. Figma/이미지 자료는 `assets/`에 저장하고, 문서에서 링크를 제공합니다.

## Structure
```
design/
├── README.md
├── guides/
│   ├── design-system.md
│   ├── research.md
│   └── handoff-checklist.md
└── assets/
    └── (Figma export, journey map, 페르소나 등)
```

## 운영 방식
1. 문서 업데이트 시 Figma/Notion 등 외부 링크가 있다면 버전 정보와 함께 기록.
2. 프론트엔드/백엔드 문서에서 참조하는 경우 상대 경로 링크를 사용해 싱글 소스로 유지.
3. 대규모 변경(디자인 시스템 버전 업 등)은 Releases 또는 Roadmap에도 반영합니다.
