# 🏡 나중사 (나를 위한 중개사)

부동산 매물 요청자와 중개사를 연결하는 **부동산 매칭 플랫폼**입니다.  
사용자가 원하는 매물 조건을 등록하면 조건에 맞는 중개사가 제안을 제공하고  
채팅 및 전화 상담을 통해 실시간으로 소통할 수 있습니다.

---

# 🏗 System Architecture

<img width="475" height="688" alt="Image" src="https://github.com/user-attachments/assets/c20c5d8d-3f2f-4d19-bf88-196697275f10" />

- 사용자 앱 / 중개사 앱에서 REST API 요청
- Spring Boot 기반 API 서버에서 비즈니스 로직 처리
- MySQL 기반 데이터 저장 및 조회

---

# 📌 Project Overview

- **프로젝트 기간:** 2023.07 ~ 2025.05  
- **프로젝트 유형:** 회사 프로젝트  
- **역할:** Backend Developer  
- **주요 담당:** 핵심 도메인 API 설계 및 구현, DB 구조 개선, 성능 최적화  

---

# 📊 System Scale

본 서비스는 사용자 앱과 중개사 앱이 함께 운영되는 부동산 매칭 플랫폼입니다.

플랫폼 특성상 다음과 같은 데이터가 지속적으로 누적되는 구조였습니다.

- 매물 요청 데이터
- 매물 등록 데이터
- 중개사 회원 데이터
- 알림 및 상담 관련 데이터

특히 관리자 서비스에서는 다양한 조건 기반 조회가 발생하기 때문에  
복잡한 조회 쿼리 성능 최적화가 중요한 환경이었습니다.

---

# ⚙️ Key Responsibilities

### 핵심 도메인 API 설계 및 구현

플랫폼의 주요 기능을 담당하는 REST API를 설계하고 구현했습니다.

주요 개발 기능

- 매물 요청 등록 / 수정 / 조회 API
- 매물 내놓기 등록 / 수정 / 조회 / 삭제 API
- 알림 기능 (서비스 알림, 방해금지 시간 설정)
- 중개사 영업 리스트 관리 기능
- 관리자 매물 / 회원 관리 API
- 회원 탈퇴 및 데이터 정합성 유지 로직 구현

---

# 🚀 Performance Optimization

### QueryDSL 기반 조회 성능 개선

관리자 매물 조회 API에서 복잡한 조건 필터링을 위해  
다중 서브쿼리가 사용되면서 조회 성능 저하 문제가 발생했습니다.

이를 해결하기 위해

- QueryDSL 기반 동적 쿼리 구조로 재설계
- 서브쿼리 제거 후 Join 기반 조회 구조로 변경
- Fetch Join 적용
- 인덱스를 활용할 수 있도록 쿼리 구조 개선

개선 결과

- **DB 조회 성능 약 30% 개선**
- **관리자 API 평균 응답 속도 약 400ms 단축**

---

# 💰 Cost Optimization

### 안심번호 발급 구조 개선

기존에는 중개사 회원 가입 시 안심번호가 **고정 발급**되는 구조였습니다.

이로 인해 실제 사용 여부와 관계없이 번호 유지 비용이 지속적으로 발생하는 문제가 있었습니다.

개선 내용

- 중개사 **결제 시점에만 안심번호 발급**
- 번호 **1개월 사용 후 자동 해지**
- 서비스 편의를 위해 **5일 유예 기간 제공**
- 해지된 번호 **다른 중개사에게 재사용 가능하도록 설계**

개선 결과

- 안심번호 발급 구조를  
  **고정 발급 → 사용 기반 발급 모델**로 전환
- **운영 비용 약 40% 절감**

---

# 📊 Achievements

- 매물 요청 / 매물 등록 / 알림 / 관리자 기능 등 **플랫폼 핵심 도메인 API 설계 및 구현**
- QueryDSL 기반 구조 개선으로 **DB 성능 약 30% 향상**
- 관리자 API **응답 속도 약 400ms 단축**
- 안심번호 발급 구조 개선으로 **운영 비용 약 40% 절감**

---

# 🛠 Tech Stack

### Backend

- Java
- Spring Boot
- Spring Data JPA
- QueryDSL

### Database

- MySQL

### DevOps

- GitHub Actions

### Collaboration

- Git
- GitHub
- Jira
- Swagger
- Slack
- Naver Works

---

# 📱 Service Link

사용자 앱  
https://play.google.com/store/apps/details?id=com.najoongsa.user.app

중개사 앱  
https://play.google.com/store/apps/details?id=com.najoongsa.realtor.app
