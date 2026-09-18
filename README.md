# HongBookStore · 홍책방

홍익대학교 학생을 위한 **중고 교재 거래 및 정보 공유 플랫폼**입니다.

학생들이 필요한 교재를 찾고, 판매자와 대화하고, 거래를 진행한 뒤 후기까지 남길 수 있도록 교재 거래 전 과정을 하나의 서비스로 구성했습니다.

---

## 프로젝트 개요

- 기간: 2025.03 ~ 2025.11
- 형태: 4인 팀 졸업프로젝트
- 대상: 홍익대학교 학생
- 주요 영역: 중고 교재 거래, 구해요 게시판, 채팅, 거래 상태 관리, 리뷰, 장소 정보

초기 기획과 요구사항 문서는 별도 저장소에 정리되어 있습니다.

- [초기 기획 저장소](https://github.com/moonaneul/hong-bookstore)

---

## 주요 기능

### 중고 교재 거래
- 판매글 검색 / 필터 / 정렬
- ISBN 기반 등록 / 직접 등록
- 이미지 업로드
- 판매 상태 변경
- 찜하기
- 최근 본 글

### 구해요 게시판
- 글 작성 / 수정 / 삭제
- 댓글 / 대댓글

### 채팅과 거래
- STOMP WebSocket 기반 실시간 채팅
- 거래 예약 요청 / 수락 / 취소 / 완료
- SSE 알림

### 사용자
- OAuth2 로그인
- JWT 인증
- 학생 인증 메일
- 프로필 관리

### 후기와 장소
- 거래 상대 평가
- 장소 리뷰
- 지도 / 장소 검색
- 경로 안내
- 외부 도서 검색
- 날씨 정보
- 유해 표현 필터

---

## 서비스 흐름

```text
교재 탐색
→ 판매글 확인
→ 찜 / 최근 본 글
→ 판매자와 채팅
→ 거래 예약
→ 거래 완료
→ 상대방 평가 / 후기
```

판매 중인 교재가 없을 경우에는 `구해요` 게시판에서 구매 의사를 등록하고 댓글로 정보를 주고받을 수 있습니다.

---

## 화면 예시

서비스에는 다음과 같은 화면이 포함되어 있습니다.

- 메인 홈
- 책 구해요 게시글 상세 / 댓글
- 지도 기반 거래 장소 정보
- 거래 장소 상세 / 경로 안내
- 채팅 / 거래 상태 화면

---

## 시스템 구성

```text
[ React / Vite Frontend ]
          │
          ▼
[ Spring Boot Backend ]
          │
     ┌────┴────┐
     ▼         ▼
 [ MySQL ]  [ Redis ]
          │
          ▼
External APIs / Storage / Notification
```

### Frontend
- React
- Vite
- React Router
- React Query
- styled-components

### Backend
- Java 21
- Spring Boot
- Spring Security
- JPA
- WebSocket(STOMP)

### Data / Infra
- MySQL
- Redis
- Docker
- GCP
- Vercel
- GitHub Actions

---

## 기획 산출물

초기 저장소에는 프로젝트 기획 과정에서 작성한 자료가 남아 있습니다.

- Requirement List
- Step-by-step Description
- Use Case Diagram
- 사용자 중심 요구사항 정의
- 화면 정의
- 권한표
- 팀 의사결정 정리
- 주차별 요구사항 명세
- 설문 결과

이 자료를 바탕으로 기능 범위와 정책을 정하고 실제 서비스 구현으로 연결했습니다.

---

## 팀 역할

4인 팀으로 진행했습니다.

문하늘은 주로 다음 범위를 담당했습니다.

- 요구사항 정리
- Use Case 작성
- 기능 / 정책 논의
- 화면 구조 설계
- Figma 화면 설계
- Frontend 구현 연결

Backend, DB, 인프라 등은 팀 내에서 역할을 나누어 진행했습니다.

자세한 역할 정리는 [docs/CONTRIBUTION.md](./docs/CONTRIBUTION.md)에서 확인할 수 있습니다.

---

## 프로젝트 구조

```text
src/main/java/com/hongik/books   # Backend
src/main/resources               # Backend resources
src/main/frontend                # Frontend
deploy                           # Deployment configuration
Dockerfile
```

---

## 실행

### Backend

```bash
./gradlew bootRun
```

### Frontend

```bash
cd src/main/frontend
npm install
npm run dev
```

---

## 관련 문서

- [초기 기획 저장소](https://github.com/moonaneul/hong-bookstore)
- [Contribution](./docs/CONTRIBUTION.md)
- [Limitations](./docs/LIMITATIONS.md)
