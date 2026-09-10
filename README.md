# 이민준 | Backend Developer

금융 서비스의 안정성과 데이터 정합성을 고민하는 백엔드 개발자입니다.

Java와 Spring Boot를 중심으로 금융 서비스의 이체·환전 기능을 개발했고,  
실제 DB 장애를 계기로 장애 감지부터 요청 전환, 데이터 복제, 장애 격리까지 직접 설계하고 검증했습니다.

기능이 정상적으로 동작하는 것에서 끝내지 않고,  
장애가 발생했을 때도 시스템이 어떻게 동작해야 하는지 설명할 수 있는 개발자를 지향합니다.

---

## Core Competencies

- **Java / Spring Boot Backend**
  - REST API
  - 인증·인가
  - 금융 트랜잭션 처리

- **High Availability & Failure Handling**
  - Master / Slave DB 구조
  - 상태 감지
  - 동적 라우팅
  - 장애 격리

- **Database & Cache**
  - Oracle
  - PostgreSQL
  - Redis

- **DevOps & Deployment**
  - Docker
  - Nginx
  - GitHub Actions
  - GCP
  - Vercel

- **Service Development**
  - 팀 프로젝트 리딩
  - 1인 SaaS 기획·개발·배포·운영

---

## Tech Stack

### Backend
`Java` `Spring Boot` `Spring Security` `REST API`

### Database
`Oracle` `PostgreSQL` `Redis` `Supabase`

### DevOps
`Docker` `Nginx` `GitHub Actions` `GCP` `Vercel`

### Frontend / Service
`Next.js` `React` `TypeScript` `Flutter`

### Tools
`Git` `GitHub` `SQL`

---

# Projects

## FLOBANK
### 금융 이체·환전 웹 / 앱 플랫폼

> 실제 DB 장애를 계기로 고가용성 구조를 설계하고, 장애 상황까지 직접 검증한 금융 서비스 프로젝트

**Role**
- 6인 팀 프로젝트
- 팀장
- 백엔드 개발
- GCP 서버 구축

**Tech**
- Java
- Spring Boot
- Oracle
- Redis
- Docker
- Nginx
- GCP
- GitHub Actions

### 주요 구현

- 이체·환전 및 금융 트랜잭션 기능 구현
- 사용자 인증·인가 기능 구현
- Oracle 기반 Master / Slave DB 구조 구성
- GitHub Actions 기반 CI/CD 파이프라인 구축
- Docker / Nginx 기반 배포 환경 구성

### 문제 해결 경험

#### DB 장애 상황에서 서비스 요청까지 영향을 받는 문제

DB 상태 확인 로직이 일반 서비스 요청과 강하게 결합되어 있어,  
Slave 장애가 발생했을 때 서비스 전체 응답에 영향을 줄 수 있는 구조였습니다.

이를 해결하기 위해 다음과 같이 구조를 개선했습니다.

```text
DB 장애 발생
↓
Ping 전용 DataSource로 상태 확인 로직 분리
↓
AbstractRoutingDataSource 기반 요청 라우팅 전환
↓
데이터 중요도에 따라 복제 방식 분리
↓
핵심 데이터: 동기 복제
비핵심 데이터: Redis Queue 기반 순차 복제
↓
Master / Slave TransactionManager 분리
↓
Slave 장애가 Master 트랜잭션에 영향을 주지 않도록 격리
↓
docker stop으로 실제 장애를 발생시켜 Failover 검증
