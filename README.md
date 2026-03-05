# my-agents-base

여러 AI 코딩 에이전트가 하나의 프로젝트에서 동일한 규칙과 워크플로우를 공유하기 위한 샘플 구조입니다.

## 폴더 구조

```
my-project/
├── AGENTS.md                        # 공유 규칙의 단일 원천 (Single Source of Truth)
│                                    # Cursor, Copilot, Codex, Gemini CLI, Windsurf 등이 직접 읽음
│
├── CLAUDE.md                        # Claude Code 전용 포인터
│                                    # AGENTS.md를 참조하도록 안내만 담음
│                                    # (Claude Code가 AGENTS.md를 네이티브 지원하면 삭제 가능)
│
├── .ai/                             # 세부 문서 디렉토리
│   ├── workflows/                   # 작업별 워크플로우 정의
│   │   ├── bug-fix.md               #   버그 수정 절차
│   │   ├── feature-dev.md           #   기능 개발 절차
│   │   ├── pr-review.md             #   PR 리뷰 절차
│   │   ├── work-log.md              #   작업 일지 작성 절차
│   │   └── code-change-log.md       #   코드 변경 의도 기록 절차
│   │
│   ├── context/                     # 프로젝트 컨텍스트 문서
│   │   ├── architecture.md          #   시스템 아키텍처 설명
│   │   └── tech-stack.md            #   기술 스택 및 의존성
│   │
│   └── templates/                   # 템플릿 모음
│       ├── commit-message.md        #   커밋 메시지 템플릿
│       ├── pr-template.md           #   PR 작성 템플릿
│       ├── work-log.md              #   작업 일지 템플릿
│       └── code-change-log.md       #   코드 변경 의도 템플릿
│
├── docs/
│   ├── work-journal/                # 작업 일지 저장 위치 (YYYY-MM-DD.md)
│   └── code-change-notes/           # 코드 변경 의도 문서 저장 위치 (YYYY-MM-DD.md)
│
└── README.md                        # 이 파일 (구조 설명)
```

## 핵심 원칙

### 1. AGENTS.md가 유일한 원천

모든 공통 규칙은 `AGENTS.md`에 작성합니다. AI 도구별 설정 파일(CLAUDE.md 등)은 이를 참조만 합니다.

### 2. AI별 설정 파일은 최소화

각 AI 도구의 고유 설정 파일에는 **포인터**(참조 안내)만 넣습니다. 규칙을 중복 작성하지 않습니다.

### 3. 세부 문서는 `.ai/` 하위에 분리

`AGENTS.md`가 너무 길어지면 AI가 핵심을 놓칠 수 있습니다. 워크플로우, 아키텍처 등 상세 문서는 `.ai/` 하위 파일로 분리하고 `AGENTS.md`에서 참조합니다.

### 4. 규칙 변경은 한 곳에서만

규칙을 수정할 때 `AGENTS.md` (또는 `.ai/` 하위 파일) 한 곳만 고치면 모든 AI 에이전트에 즉시 반영됩니다.

### 5. 작업 종료 시 일지 작성

모든 AI 에이전트는 작업을 마칠 때 `docs/work-journal/YYYY-MM-DD.md`에 작업 일지를 남깁니다.

### 6. 코드 변경 의도 기록

코드 작성/수정이 있었던 세션에서는 `docs/code-change-notes/YYYY-MM-DD.md`에 변경 의도와 근거를 남깁니다.

## AI 도구별 지원 현황

| AI 도구 | 읽는 파일 | AGENTS.md 네이티브 지원 |
|---------|----------|----------------------|
| Cursor | `.cursorrules` / `AGENTS.md` | O |
| GitHub Copilot | `.github/copilot-instructions.md` / `AGENTS.md` | O |
| Codex (OpenAI) | `AGENTS.md` | O |
| Gemini CLI | `AGENTS.md` | O |
| Windsurf | `.windsurfrules` / `AGENTS.md` | O |
| Aider | `AGENTS.md` | O |
| Claude Code | `CLAUDE.md` | X (feature request 중) |

## 새 프로젝트에 적용하는 방법

1. 이 샘플의 `AGENTS.md`, `CLAUDE.md`, `.ai/` 디렉토리를 프로젝트 루트에 복사합니다.
2. `AGENTS.md`의 규칙을 프로젝트에 맞게 수정합니다.
3. `.ai/` 하위 문서를 프로젝트에 맞게 수정합니다.
4. 사용하지 않는 AI 도구의 포인터 파일은 삭제해도 됩니다.
