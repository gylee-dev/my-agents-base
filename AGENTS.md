# AGENTS.md

> 이 파일은 프로젝트의 모든 AI 코딩 에이전트가 참조하는 **공유 규칙의 단일 원천(Single Source of Truth)** 입니다.
> Cursor, GitHub Copilot, Codex, Gemini CLI, Windsurf, Aider 등 AGENTS.md를 지원하는 도구는 이 파일을 자동으로 읽습니다.

---

## Code Style

<!-- 프로젝트에 맞게 수정하세요 -->

- TypeScript strict mode 사용
- 함수형 스타일 우선, class는 꼭 필요한 경우에만
- 변수명: `camelCase`, 타입/인터페이스: `PascalCase`, 상수: `UPPER_SNAKE_CASE`
- 파일명: `kebab-case.ts`
- 한 파일은 200줄을 넘지 않도록 분리

## Git Conventions

- **Conventional Commits** 형식을 따른다
  - `feat:` 새 기능
  - `fix:` 버그 수정
  - `refactor:` 리팩토링 (동작 변화 없음)
  - `docs:` 문서 변경
  - `test:` 테스트 추가/수정
  - `chore:` 빌드, 설정 등 기타
- PR당 하나의 관심사만 다룬다
- 커밋 메시지 템플릿: `.ai/templates/commit-message.md` 참조

## Build & Test

<!-- 프로젝트에 맞게 실제 명령어를 기재하세요 -->

```bash
npm install          # 의존성 설치
npm run dev          # 개발 서버 실행
npm run build        # 프로덕션 빌드
npm run lint         # 린트 검사
npm run lint:fix     # 린트 자동 수정
npm test             # 전체 테스트 실행
npm test -- <path>   # 단일 파일 테스트
npm run test:coverage # 커버리지 확인
```

- 새 기능은 반드시 테스트를 포함한다
- 버그 수정 시 실패하는 테스트를 먼저 작성한다
- 테스트 파일 위치: 소스 파일과 같은 디렉토리의 `__tests__/` 하위
- 코드 변경 후 반드시 `npm run lint`와 `npm test`를 실행하여 통과를 확인한다

## Forbidden

- `any` 타입 사용 금지
- `console.log`를 프로덕션 코드에 남기지 않음 (디버깅 후 반드시 제거)
- 사용하지 않는 import/변수를 남기지 않음
- 하드코딩된 비밀 값(API key 등)을 코드에 포함하지 않음

## Finalization

- 사용자와의 작업을 마무리할 때는 반드시 작업 일지를 남긴다
- 작업 일지는 `.ai/workflows/work-log.md` 절차를 따른다
- 일지 템플릿은 `.ai/templates/work-log.md`를 사용한다
- 일지 저장 위치: `docs/work-journal/YYYY-MM-DD.md` (해당 날짜 파일이 없으면 생성)
- 코드 작성/수정이 있었으면 코드 변경 의도 문서를 반드시 남긴다
- 코드 변경 의도 문서는 `.ai/workflows/code-change-log.md` 절차를 따른다
- 코드 변경 의도 템플릿은 `.ai/templates/code-change-log.md`를 사용한다
- 코드 변경 의도 저장 위치: `docs/code-change-notes/YYYY-MM-DD.md` (해당 날짜 파일이 없으면 생성)

## References

프로젝트 상세 문서는 아래 경로를 참조한다:

| 구분 | 경로 |
|------|------|
| 시스템 아키텍처 | `.ai/context/architecture.md` |
| 기술 스택 | `.ai/context/tech-stack.md` |
| 워크플로우 (버그 수정, 기능 개발, PR 리뷰 등) | `.ai/workflows/` |
| 템플릿 (커밋 메시지, PR, 작업 일지 등) | `.ai/templates/` |
