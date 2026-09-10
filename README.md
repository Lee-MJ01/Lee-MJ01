<div align="center">

# 이민준
### Backend Developer

금융 서비스의 안정성과 데이터 정합성을 고민하는 백엔드 개발자입니다.

Java와 Spring Boot를 중심으로 금융 서비스를 개발하고,  
실제 DB 장애를 계기로 장애 감지부터 요청 전환, 데이터 복제, 장애 격리까지 설계·검증했습니다.

<br/>

<a href="https://github.com/Lee-MJ01">
  <img src="https://img.shields.io/badge/GitHub-Lee--MJ01-181717?style=for-the-badge&logo=github"/>
</a>
<a href="mailto:alswnstl23@gmail.com">
  <img src="https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/>
</a>

</div>

---

## About Me

<table>
<tr>
<td width="50%" valign="top">

### Backend
- Java / Spring Boot 기반 서버 개발
- REST API 및 인증·인가
- 금융 트랜잭션 처리
- Oracle / PostgreSQL / Redis

</td>
<td width="50%" valign="top">

### Reliability
- Master / Slave DB 구조
- 장애 감지 및 Failover
- 동적 DataSource Routing
- 장애 격리 및 복제 전략 설계

</td>
</tr>
<tr>
<td width="50%" valign="top">

### DevOps
- Docker / Nginx
- GitHub Actions
- GCP
- Vercel

</td>
<td width="50%" valign="top">

### Experience
- 금융 프로젝트 팀 리더
- 1인 SaaS 개발·배포·운영
- BNK 금융 DT 아카데미
- SSAFY 16기

</td>
</tr>
</table>

---

## Tech Stack

### Backend

<p>
<img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white"/>
<img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white"/>
<img src="https://img.shields.io/badge/Spring%20Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white"/>
</p>

### Database

<p>
<img src="https://img.shields.io/badge/Oracle-F80000?style=flat-square&logo=oracle&logoColor=white"/>
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"/>
<img src="https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white"/>
</p>

### DevOps

<p>
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
<img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white"/>
<img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white"/>
<img src="https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white"/>
<img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white"/>
</p>

### Frontend / Service

<p>
<img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white"/>
<img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black"/>
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/>
<img src="https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white"/>
</p>

---

# Projects

## FLOBANK
### 금융 이체·환전 웹 / 앱 플랫폼

> **DB 장애를 계기로 고가용성 구조를 설계하고 실제 장애 상황까지 검증한 금융 프로젝트**

<table>
<tr>
<td><b>Team</b></td>
<td>6인 프로젝트 / 팀장</td>
</tr>
<tr>
<td><b>Role</b></td>
<td>Backend / Infrastructure</td>
</tr>
<tr>
<td><b>Tech</b></td>
<td>Java, Spring Boot, Oracle, Redis, Docker, Nginx, GCP</td>
</tr>
<tr>
<td><b>Result</b></td>
<td>프로젝트 최우수상</td>
</tr>
</table>

### What I Built

- 이체·환전 및 금융 트랜잭션 기능
- 사용자 인증·인가
- Master / Slave DB 이중화
- GitHub Actions 기반 CI/CD
- Docker / Nginx 기반 배포

### Problem Solving

```text
DB 장애 발생
    ↓
Ping 전용 DataSource로 상태 확인 분리
    ↓
AbstractRoutingDataSource 기반 요청 전환
    ↓
데이터 중요도에 따라 복제 전략 분리
    ↓
핵심 데이터      → 동기 복제
비핵심 데이터    → Redis Queue
    ↓
Master / Slave TransactionManager 분리
    ↓
Slave 장애 격리
    ↓
docker stop 기반 장애 주입 테스트
