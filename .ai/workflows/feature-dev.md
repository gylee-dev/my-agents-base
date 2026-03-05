# Feature Development Workflow

> 새 기능 개발 시 따르는 표준 절차입니다.

## 절차

### 1. 요구사항 확인

- 기능의 목표와 범위를 명확히 이해한다
- 불확실한 부분은 구현 전에 확인한다

### 2. 설계

- 기존 코드와의 관계를 파악한다
- 영향 범위를 최소화하는 방향으로 설계한다
- 필요하면 `.ai/context/architecture.md`를 참고한다

### 3. 구현

- 작은 단위로 나누어 점진적으로 구현한다
- AGENTS.md의 코드 스타일 규칙을 따른다
- Over-engineering을 피한다 — 현재 필요한 만큼만 구현한다

### 4. 테스트 작성

- 핵심 동작을 검증하는 테스트를 작성한다
- 엣지 케이스도 고려한다
- 테스트 파일 위치: 소스와 같은 디렉토리의 `__tests__/` 하위

### 5. 검증

- 전체 테스트 실행: `npm test`
- 린트 검사: `npm run lint`

### 6. 커밋 & PR

- 커밋 메시지: `feat: <기능 설명>`
- PR 작성 시 `.ai/templates/pr-template.md` 템플릿을 따른다

## 예시

```bash
# 기능 브랜치 생성
git checkout -b feat/user-profile

# 구현 & 테스트 후 커밋
git commit -m "feat: add user profile page"

# PR 생성
gh pr create --title "feat: add user profile page" --body-file .ai/templates/pr-template.md
```
