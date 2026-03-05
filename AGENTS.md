# AGENTS.md

> 이 파일은 프로젝트의 모든 AI 코딩 에이전트가 참조하는 **공유 규칙의 단일 원천(Single Source of Truth)** 입니다.
> Cursor, GitHub Copilot, Codex, Gemini CLI, Windsurf, Aider 등 AGENTS.md를 지원하는 도구는 이 파일을 자동으로 읽습니다.

---

<!-- 예시: 아래는 실제 프로젝트에 맞게 수정하세요 -->

## Code Style

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

## Testing

- 새 기능은 반드시 테스트를 포함한다
- 버그 수정 시 실패하는 테스트를 먼저 작성한다
- 테스트 파일 위치: 소스 파일과 같은 디렉토리의 `__tests__/` 하위
- 테스트 실행: `npm test`
- 커버리지 확인: `npm run test:coverage`

## Forbidden

- `any` 타입 사용 금지
- `console.log`를 프로덕션 코드에 남기지 않음 (디버깅 후 반드시 제거)
- 사용하지 않는 import/변수를 남기지 않음
- 하드코딩된 비밀 값(API key 등)을 코드에 포함하지 않음

## Project Structure

- `src/` — 소스 코드
- `tests/` — 통합 테스트
- `docs/` — 사용자 문서
- `scripts/` — 빌드/배포 스크립트

## Workflows

작업 유형별 상세 절차는 아래 문서를 참조:

- 버그 수정: `.ai/workflows/bug-fix.md`
- 기능 개발: `.ai/workflows/feature-dev.md`
- PR 리뷰: `.ai/workflows/pr-review.md`

## Architecture & Context

- 시스템 아키텍처: `.ai/context/architecture.md`
- 기술 스택: `.ai/context/tech-stack.md`
