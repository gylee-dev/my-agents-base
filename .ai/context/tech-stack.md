# Tech Stack

> 프로젝트에서 사용하는 기술 스택과 의존성 목록입니다. 프로젝트에 맞게 수정하세요.

## Runtime & Language

| 항목 | 선택 | 버전 |
|------|------|------|
| Runtime | Node.js | 20.x LTS |
| Language | TypeScript | 5.x |
| Package Manager | npm | 10.x |

## Frontend

| 항목 | 선택 | 비고 |
|------|------|------|
| Framework | React | 18.x |
| Styling | Tailwind CSS | utility-first |
| State | Zustand | 경량 상태관리 |
| Routing | React Router | v6 |

## Backend

| 항목 | 선택 | 비고 |
|------|------|------|
| Framework | Express | REST API |
| ORM | Prisma | type-safe DB 접근 |
| Validation | Zod | 런타임 스키마 검증 |

## Database

| 항목 | 선택 | 비고 |
|------|------|------|
| Primary DB | PostgreSQL | 16.x |
| Cache | Redis | 세션 및 캐싱 |

## Testing

| 항목 | 선택 | 비고 |
|------|------|------|
| Test Runner | Vitest | 유닛/통합 테스트 |
| E2E | Playwright | 브라우저 테스트 |

## DevOps

| 항목 | 선택 | 비고 |
|------|------|------|
| CI/CD | GitHub Actions | `.github/workflows/` |
| Linting | ESLint + Prettier | 코드 스타일 통일 |
| Container | Docker | 개발/배포 환경 |

## 주요 커맨드

```bash
npm install          # 의존성 설치
npm run dev          # 개발 서버 실행
npm test             # 테스트 실행
npm run build        # 프로덕션 빌드
npm run lint         # 린트 검사
npm run lint:fix     # 린트 자동 수정
```
