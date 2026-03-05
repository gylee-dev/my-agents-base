# Architecture

> 시스템 아키텍처 문서입니다. 프로젝트에 맞게 수정하세요.

## 개요

<!-- 시스템의 전체적인 구조를 간략히 설명합니다 -->

예시: 이 프로젝트는 React 프론트엔드 + Express 백엔드 + PostgreSQL 데이터베이스로 구성된 웹 애플리케이션입니다.

## 디렉토리 구조

```
src/
├── api/          # REST API 라우트 및 컨트롤러
├── services/     # 비즈니스 로직
├── models/       # 데이터 모델 및 DB 스키마
├── utils/        # 공통 유틸리티 함수
└── config/       # 환경 설정
```

## 주요 컴포넌트

<!-- 시스템의 핵심 컴포넌트와 역할을 설명합니다 -->

| 컴포넌트 | 역할 | 위치 |
|---------|------|------|
| API Layer | HTTP 요청 처리, 인증 | `src/api/` |
| Service Layer | 비즈니스 로직 | `src/services/` |
| Data Layer | DB 접근, 쿼리 | `src/models/` |

## 데이터 흐름

```
Client → API Route → Controller → Service → Model → Database
                                                  ↓
Client ← Response  ← Controller ← Service ← Model
```

## 중요한 설계 결정

<!-- 프로젝트에서 내린 주요 아키텍처 결정과 그 이유를 기록합니다 -->

- **예시**: Service Layer를 분리한 이유 — 컨트롤러에서 비즈니스 로직을 분리하여 테스트를 용이하게 함
- **예시**: PostgreSQL 선택 이유 — JSON 데이터와 관계형 데이터를 모두 다루어야 하므로

## 주의사항

<!-- 코드를 수정할 때 반드시 알아야 하는 제약이나 주의사항을 적습니다 -->

- 예시: `src/models/`의 스키마를 변경하면 마이그레이션 파일을 함께 생성해야 합니다
- 예시: `src/api/auth.ts`는 모든 인증 로직의 진입점입니다 — 수정 시 보안 리뷰 필수
