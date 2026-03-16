# 🏡 나중사 (나를 위한 중개사)

부동산 매물 요청자와 중개사를 연결하는 **부동산 매칭 플랫폼**입니다.  
사용자가 원하는 매물 조건을 등록하면 조건에 맞는 중개사가 제안을 제공하고, 채팅 및 전화 상담을 통해 실시간으로 소통할 수 있습니다.

---

# 🏗 System Architecture

<img width="475" height="688" alt="System Architecture" src="https://github.com/user-attachments/assets/c20c5d8d-3f2f-4d19-bf88-196697275f10" />

* 사용자 앱 / 중개사 앱에서 REST API 요청
* Spring Boot 기반 서버에서 비즈니스 로직 처리
* MySQL DB에서 데이터 저장 및 조회

---

# 📌 Project Overview

* **프로젝트 기간:** 2023.07 ~ 2025.05  
* **프로젝트 유형:** 회사 프로젝트  
* **역할:** Backend Developer  
* **주요 담당:** 핵심 도메인 API 설계 및 구현, DB 구조 개선, 성능 최적화

---

# 📊 System Scale

* 사용자 앱과 중개사 앱이 함께 운영되는 부동산 매칭 플랫폼
* 데이터 누적 항목
  - 매물 요청 / 매물 등록 / 중개사 회원 / 알림 및 상담 데이터
* 관리자 서비스에서는 조건 기반 조회가 많아 **조회 성능 최적화**가 중요한 환경

---

# ⚙️ Key Responsibilities

* 매물 요청 수정 / 조회 API 개발
* 매물 내놓기 등록 / 수정 / 조회 / 삭제 기능 구현
* 사용자/중개사 알림 기능 (서비스 알림, 방해금지 시간 설정)
* 관리자 매물 / 회원 관리 / 메모 / 블랙리스트 등 API 구현
* 회원 탈퇴 및 데이터 정합성 유지 로직 설계

---

# 🚀 Performance & Cost Optimization

### 1️⃣ QueryDSL 기반 조회 성능 개선
* 다중 서브쿼리 → Join 기반 동적 조건 조회 구조로 재설계
* Fetch Join 적용 및 인덱스 활용
* **결과:** DB 조회 성능 약 30% 개선, 관리자 API 응답 속도 약 400ms 단축

### 2️⃣ 안심번호 발급 구조 개선
* 고정 발급 → 사용 기반 발급 모델로 전환
* 결제 시점에만 발급, 1개월 사용 후 자동 해지, 5일 유예 기간 제공
* **결과:** 운영 비용 약 40% 절감

---

# 🔍 Troubleshooting

* 관리자 매물 조회 API에서 다중 서브쿼리로 인한 성능 저하 발생
* QueryDSL 기반 Join + 동적 조건 조합 방식으로 쿼리 재설계
* 결과: DB 조회 성능 약 30% 개선, API 응답 속도 약 400ms 단축

---

# 📊 Achievements

* 플랫폼 핵심 도메인 REST API 설계 및 구현
* DB 조회 성능 약 30% 개선
* 관리자 API 응답 속도 약 400ms 단축
* 안심번호 발급 구조 개선으로 운영 비용 약 40% 절감

---

# 🛠 Tech Stack

### Backend
* Java
* Spring Boot
* Spring Data JPA
* QueryDSL

### Database
* MySQL

### DevOps
* GitHub Actions

### Collaboration
* Git / GitHub / Jira / Swagger / Slack / Naver Works

---

# 📱 Service Links

* [사용자 앱](https://play.google.com/store/apps/details?id=com.najoongsa.user.app)  
* [중개사 앱](https://play.google.com/store/apps/details?id=com.najoongsa.realtor.app)
