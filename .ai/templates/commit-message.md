# Commit Message Template

> Conventional Commits 형식을 따릅니다.

## 형식

```
<type>: <description>

[optional body]

[optional footer]
```

## Type 목록

| Type | 용도 | 예시 |
|------|------|------|
| `feat` | 새 기능 추가 | `feat: add user login page` |
| `fix` | 버그 수정 | `fix: resolve null pointer in parser` |
| `refactor` | 리팩토링 (동작 변화 없음) | `refactor: extract validation logic` |
| `docs` | 문서 변경 | `docs: update API reference` |
| `test` | 테스트 추가/수정 | `test: add unit tests for auth service` |
| `chore` | 빌드, 설정 등 | `chore: update dependencies` |
| `style` | 코드 포맷팅 (동작 변화 없음) | `style: fix indentation` |
| `perf` | 성능 개선 | `perf: optimize database query` |
| `ci` | CI/CD 설정 변경 | `ci: add test coverage report` |

## 규칙

- description은 소문자로 시작한다
- description은 명령형으로 쓴다 ("added" 아닌 "add")
- description 끝에 마침표를 붙이지 않는다
- 50자 이내로 작성한다
- 관련 이슈가 있으면 footer에 참조: `Closes #42`

## 예시

```
feat: add email verification on signup

Send a verification email when a new user registers.
The email contains a one-time link valid for 24 hours.

Closes #128
```

```
fix: prevent crash when config file is missing (#42)
```

```
refactor: split user service into auth and profile modules
```
