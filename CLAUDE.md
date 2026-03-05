# CLAUDE.md

> Claude Code 전용 포인터 파일입니다.
> Claude Code는 아직 AGENTS.md를 네이티브로 지원하지 않으므로, 이 파일을 통해 공유 규칙을 참조합니다.
> Claude Code가 AGENTS.md를 네이티브 지원하게 되면 이 파일은 삭제해도 됩니다.

## 공유 규칙

프로젝트 루트의 `AGENTS.md` 파일을 읽고 그 안의 모든 규칙을 따르세요.

## 세부 문서

- `.ai/workflows/` — 작업별 워크플로우 (bug-fix, feature-dev, pr-review, work-log, code-change-log)
- `.ai/context/architecture.md` — 시스템 아키텍처
- `.ai/context/tech-stack.md` — 기술 스택 및 의존성
- `.ai/templates/` — 커밋 메시지, PR, 작업 일지, 코드 변경 의도 템플릿

## 작업 마무리 규칙

- 작업 종료 시 반드시 작업 일지를 작성하세요.
- 저장 경로: `docs/work-journal/YYYY-MM-DD.md`
- 작성 기준: `.ai/workflows/work-log.md`
- 템플릿: `.ai/templates/work-log.md`

## 코드 변경 설명 규칙

- 코드 작성/수정이 있었으면 코드 변경 의도 문서를 반드시 작성하세요.
- 저장 경로: `docs/code-change-notes/YYYY-MM-DD.md`
- 작성 기준: `.ai/workflows/code-change-log.md`
- 템플릿: `.ai/templates/code-change-log.md`

## Claude Code 고유 설정

<!-- 아래는 Claude Code에서만 의미 있는 설정을 작성하는 영역입니다 -->
<!-- 예시: 특정 slash command나 skill에 대한 안내 등 -->

<!-- 공통 규칙은 여기에 쓰지 마세요. AGENTS.md에 작성하세요. -->
