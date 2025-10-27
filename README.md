# ☕ 카페 주문 시스템
![Java](https://img.shields.io/badge/Java-21-red?style=flat-square&logo=openjdk)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.5.3-green?style=flat-square&logo=spring)
![Next.js](https://img.shields.io/badge/Next.js-15.3.5-black?style=flat-square&logo=next.js)
![React](https://img.shields.io/badge/React-19-blue?style=flat-square&logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5-blue?style=flat-square&logo=typescript)
> **프로그래머스 백엔드 데브코스 6기 8회차 2팀 1차 프로젝트** (2025.07.14 ~ 2025.07.21)

<br>

## 📚 목차
- [👥 팀 소개](#-팀-소개)
- [📝 프로젝트 개요](#-프로젝트-개요)
- [🎬 프로젝트 데모](#-프로젝트-데모)
- [🛠️ 기술 스택](#️-기술-스택)
- [✨ 주요 기능](#-주요-기능)
- [📘 ERD](#-erd)
- [🧾 API 명세서](#-api-명세서)
- [🏗️ 시스템 아키텍처](#️-시스템-아키텍처)
- [🏗️ 프로젝트 구조](#️-프로젝트-구조)
- [🚀 빠른 시작](#-빠른-시작)
- [🔄 개발 프로세스](#-개발-프로세스)
- [🧠 트러블슈팅](#-트러블슈팅)

<br>

## 👥 팀 소개
| 팀원 | GitHub | 담당 기능 |
|------|--------|-----------|
| **김주은** | [@jueunk617](https://github.com/jueunk617) | • 회원가입<br>• 로그인<br>• 주문 등록<br>• 주문 내역 조회 (마이페이지) |
| **박태규** | [@NewplayerKOR](https://github.com/NewplayerKOR) | • 주문 Entity 설계<br>• 주문서 작성<br>• 주문 총 금액 계산<br>• 주문 저장, 메뉴 조회<br>• DTO (주문 요청, 반환) |
| **서지우** | [@Jiwoo-Seo](https://github.com/Jiwoo-Seo) | • 커피 메뉴 생성 API 구현<br>• 커피 메뉴 전체 조회 API 구현<br>• 커피 메뉴 수정 API 구현<br>• 커피 메뉴 삭제 API 구현<br>• Swagger 테스트 환경 구축<br>• API 테스트 작성<br>• 권한기반(관리자) 접근제어 |
| **홍민애** | [@meohin](https://github.com/meohin) | • 메뉴 목록 조회<br>• 메뉴 등록<br>• 메뉴 수정<br>• 메뉴 삭제<br>• 주문 내역 조회 |
| **순태열** | [@SoonTaeYouL](https://github.com/SoonTaeYouL) | • 회원가입 구현<br>• 비밀번호 암호화<br>• 로그인 구현<br>• JWT 토큰<br>• 스프링 시큐리티 설정 |

<br>

## 📝 프로젝트 개요

현대적인 **풀스택 음식 주문 시스템**으로, 사용자 친화적인 UI/UX와 안전한 백엔드 시스템을 제공합니다.

### 🎯 핵심 가치
- **사용자 중심 설계**: 직관적이고 반응형 인터페이스
- **보안 중심**: JWT 기반 인증 및 Spring Security 적용
- **확장 가능성**: 모듈화된 아키텍처와 RESTful API
- **개발자 경험**: 자동화된 문서화(Swagger) 및 테스트 환경

<br>

## 🎬 프로젝트 데모
https://github.com/user-attachments/assets/926a6343-a6f1-4a3f-b384-fcb76c4bb305

<br>

## 🛠️ 기술 스택

### 🌐 Frontend
| 기술 | 버전 | 용도 |
|------|------|------|
| **Next.js** | 15.3.5 | React 프레임워크, SSR/SSG |
| **React** | 19 | UI 라이브러리 |
| **TypeScript** | 5 | 정적 타입 검사 |
| **Tailwind CSS** | 3.4.13 | 유틸리티 우선 CSS 프레임워크 |
| **Framer Motion** | 12.23.6 | 애니메이션 라이브러리 |
| **React Toastify** | 11.0.5 | 사용자 알림 |

### ⚙️ Backend
| 기술 | 버전 | 용도 |
|------|------|------|
| **Java** | 21 | 프로그래밍 언어 |
| **Spring Boot** | 3.5.3 | 애플리케이션 프레임워크 |
| **Spring Security** | - | 보안 및 인증 (JWT) |
| **Spring Data JPA** | - | 데이터 접근 계층 |
| **MySQL** | 8.0+ | 관계형 데이터베이스 |
| **Gradle** | - | 빌드 도구 |
| **Swagger/OpenAPI** | 3.0 | API 문서화 |

<br>

## ✨ 주요 기능

### 👤 사용자 기능
- 🔐 **회원가입 / 로그인**
  - JWT 토큰 기반 인증
  - 보안 강화된 패스워드 암호화
- 📋 **메뉴 조회**
  - 카테고리별 메뉴 분류
  - 실시간 메뉴 정보 업데이트
- 🛒 **주문 시스템**
  - 장바구니 기능
  - 주문 수량 조절
  - 실시간 총 금액 계산
- 📊 **마이페이지**
  - 주문 내역 조회
  - 개인정보 관리

### 👨‍💼 관리자 기능
- 🍔 **메뉴 관리**
  - 메뉴 추가/수정/삭제
  - 이미지 업로드 기능
  - 가격 및 설명 관리
- 📦 **주문 관리**
  - 실시간 주문 현황 모니터링
  - 주문 상태 업데이트
- 📁 **파일 관리**
  - 메뉴 이미지 업로드
  - 파일 저장소 관리

<br>

## 📘 ERD
[![ERD-NBE6-8-1-beullulaiteu-ERD.png](https://i.postimg.cc/kGDJ99zq/ERD-NBE6-8-1-beullulaiteu-ERD.png)](https://postimg.cc/dZPPjMJx)

<br>

## 🧾 API 명세서
[![api.png](https://i.postimg.cc/jjm25D6g/api.png)](https://postimg.cc/R314pVDK)

<br>

## 🏗️ 시스템 아키텍처

```
┌─────────────────┐    HTTP/HTTPS    ┌─────────────────┐
│   Frontend      │ ◄─────────────► │   Backend       │
│   (Next.js)     │                 │ (Spring Boot)   │
│   Port: 3000    │                 │   Port: 8080    │
└─────────────────┘                 └─────────────────┘
         │                                    │
         │                                    │
         ▼                                    ▼
┌─────────────────┐                 ┌─────────────────┐
│   Browser       │                 │   MySQL         │
│   (Client)      │                 │   Database      │
└─────────────────┘                 └─────────────────┘
```

<br>

## 🏗️ 프로젝트 구조

```
NBE6-8-1-Team2/
├── 📁 frontend/                 # Next.js 프론트엔드
│   ├── 📁 src/
│   │   ├── 📁 app/             # App Router 페이지
│   │   ├── 📁 _components/     # 재사용 컴포넌트
│   │   ├── 📁 _hooks/          # 커스텀 훅
│   │   ├── 📁 lib/             # 유틸리티 라이브러리
│   │   └── 📁 types/           # TypeScript 타입 정의
│   ├── 📄 package.json
│   └── 📄 next.config.ts
├── 📁 backend/                  # Spring Boot 백엔드
│   ├── 📁 src/
│   │   ├── 📁 main/java/com/back/
│   │   │   ├── 📁 domain/      # 도메인 로직
│   │   │   │   ├── 📁 member/  # 회원 관리
│   │   │   │   ├── 📁 menu/    # 메뉴 관리
│   │   │   │   └── 📁 order/   # 주문 관리
│   │   │   └── 📁 global/      # 공통 설정 및 유틸리티
│   │   └── 📁 resources/
│   ├── 📄 build.gradle.kts
│   └── 📄 api-test.http        # API 테스트 파일
└── 📄 README.md
```

<br>

## 🚀 빠른 시작

### 📋 사전 요구사항
- **Java 21** 이상
- **Node.js 18** 이상
- **npm** 또는 **yarn**

### 🔧 설치 및 실행

#### Backend 실행
```bash
cd backend
./gradlew bootRun
```

#### Frontend 실행
```bash
cd frontend
npm install
npm run dev
```

### 🌐 접속 정보
| 서비스 | URL | 설명 |
|--------|-----|------|
| **Frontend** | http://localhost:3000 | 사용자 인터페이스 |
| **Backend API** | http://localhost:8080 | REST API 서버 |
| **API 문서** | http://localhost:8080/swagger-ui.html | Swagger UI |
| **MySQL** | localhost:3306 | 데이터베이스 서버 |

<br>

## 🔄 개발 프로세스

### 🌿 Git 브랜치 전략
```
main              // 최종 배포 브랜치
develop           // 개발 통합 브랜치

feat/login-api          // 백: 로그인 기능
feat/menu-crud          // 백: 메뉴 등록/수정/삭제
feat/order-create       // 백: 주문 등록 기능
feat/menu-page          // 프론트: 사용자 메뉴 보기 페이지
feat/admin-order-page   // 프론트: 관리자 주문 관리 페이지
```

- `main` : 최종 결과물
- `develop` : 개발 통합 브랜치
- `feat/*` : 기능 단위 브랜치
- 모든 브랜치는 `develop`에서 파생하여 작업
- 작업 완료 후 PR을 통해 `develop`에 merge

### 🧪 테스트 전략
- **단위 테스트**: JUnit 5 활용
- **통합 테스트**: Spring Boot Test
- **API 테스트**: REST Client 활용

<br>

## 🧠 트러블슈팅

### 1️⃣ 인증 방식 불일치
- **문제**: 프론트는 Authorization 헤더, 백엔드는 쿠키 기반 → 로그인 성공했으나 인증 실패  
- **해결**: JWT 쿠키 방식으로 통일, `JwtAuthenticationFilter`에서 쿠키 검증 후 인증 객체 등록

### 2️⃣ 토큰 재발급 실패
- **문제**: refreshToken DB 저장 누락으로 `/reissue` 실패  
- **해결**: 로그인 시 `member.updateRefreshToken()` + `memberRepository.save()` 필수 추가

### 3️⃣ 관리자 권한 처리
- **문제**: 관리자 로그인 후 일반 페이지 이동, `/admin/**` 접근 시 403  
- **해결**: 
  - Security 설정에 `hasRole("ADMIN")` 명시
  - 로그인 후 `role === "ADMIN"` 체크하여 `/admin/orders`로 리디렉션
  - `isLoading` 상태로 권한 체크 완료 후 페이지 분기

### 4️⃣ 사용자 정보 접근 복잡
- **문제**: `@AuthenticationPrincipal` null 처리 번거로움, `memberId` 파라미터 반복 전달  
- **해결**: `rq.getActor()` 유틸로 일관된 사용자 정보 접근

### 5️⃣ 토스트 메시지 중복
- **문제**: 로그아웃 시 메시지 여러 곳에서 출력  
- **해결**: `AuthContext.logout()` 내부 메시지 제거, 호출부에서만 표시
