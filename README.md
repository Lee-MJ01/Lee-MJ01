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
```

단순히 이중화 구조를 만드는 데 그치지 않고  
**장애 감지 → 요청 전환 → 데이터 복제 → 장애 격리 → 장애 주입 검증**까지 직접 진행했습니다.

<p>
<a href="https://github.com/Lee-MJ01/busan-bank-project1">
  <img src="https://img.shields.io/badge/Web%20Repository-181717?style=for-the-badge&logo=github"/>
</a>
<a href="https://github.com/Lee-MJ01/BNK_Project2_1team">
  <img src="https://img.shields.io/badge/App%20Repository-181717?style=for-the-badge&logo=github"/>
</a>
</p>

---

## Opo
### 1인 SaaS 서비스

> **아이디어부터 설계·개발·배포·운영까지 직접 수행한 개인 프로젝트**

<table>
<tr>
<td><b>Role</b></td>
<td>1인 개발</td>
</tr>
<tr>
<td><b>Tech</b></td>
<td>Next.js, React, TypeScript, Supabase, PostgreSQL, Vercel</td>
</tr>
<tr>
<td><b>Scope</b></td>
<td>기획 → 설계 → 개발 → 배포 → 운영</td>
</tr>
</table>

- 서비스 아이디어 및 기능 구조 설계
- 데이터 구조 설계
- 인증 및 데이터베이스 연동
- Vercel + Supabase 기반 배포
- 실제 서비스 운영 경험

<p>
<a href="http://opo.ai.kr">
  <img src="https://img.shields.io/badge/Live%20Service-000000?style=for-the-badge&logo=vercel"/>
</a>
</p>

---

## Smart Plant
### IoT 기반 자율 이동 식물 관리 시스템

> **센서값을 수집하는 데 그치지 않고 햇빛 방향을 탐색해 스스로 이동하는 화분을 구현한 캡스톤 프로젝트**

- 4인 팀 프로젝트 / 팀장
- Python / Flask / Arduino
- 센서 데이터 수집
- APScheduler 기반 주기 작업
- Serial Communication 기반 하드웨어 제어

---

# Experience

<table>
<tr>
<td width="30%"><b>SSAFY 16기</b></td>
<td>Java 기반 알고리즘 / 자료구조 / 문제 해결 역량 강화</td>
</tr>
<tr>
<td><b>BNK 부산은행 금융 DT 아카데미</b></td>
<td>약 1,000시간 실무형 교육 / Java, Spring, DB, Flutter, 생성형 AI</td>
</tr>
<tr>
<td><b>동의대학교</b></td>
<td>컴퓨터공학과 졸업</td>
</tr>
<tr>
<td><b>항공 부품 관련 실무</b></td>
<td>Excel 기반 재고 및 납기 관리</td>
</tr>
<tr>
<td><b>컴퓨터공학과 학생회장</b></td>
<td>1년간 조직 운영 및 협업 경험</td>
</tr>
</table>

---

# Certifications

<p>
<img src="https://img.shields.io/badge/정보처리기사-Passed-4CAF50?style=for-the-badge"/>
<img src="https://img.shields.io/badge/SQLD-Passed-4479A1?style=for-the-badge"/>
</p>

---

# Developer Mindset

> **동작하는 것과 무너지지 않는 것은 다르다고 생각합니다.**

기능이 정상적으로 동작하는 순간뿐 아니라,  
예상하지 못한 값이나 장애가 발생했을 때 시스템이 어떻게 반응하는지도 함께 고민합니다.

> **문제가 해결되더라도 원인을 설명할 수 있어야 끝났다고 생각합니다.**

문제를 임시로 우회하기보다,  
왜 문제가 발생했고 왜 이 방식으로 해결되는지를 이해하려고 합니다.

---

<div align="center">

### Contact

<a href="https://github.com/Lee-MJ01">
  <img src="https://img.shields.io/badge/GitHub-Lee--MJ01-181717?style=for-the-badge&logo=github"/>
</a>
<a href="mailto:alswnstl23@gmail.com">
  <img src="https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/>
</a>

</div>
    ↓
Master / Slave TransactionManager 분리
    ↓
Slave 장애 격리
    ↓
docker stop 기반 장애 주입 테스트
