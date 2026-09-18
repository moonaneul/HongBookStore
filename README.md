# HongBookStore · 홍책방

홍익대학교 학생을 위한 **중고 교재 거래 및 정보 공유 플랫폼**입니다.

2025년 3월부터 11월까지 진행한 컴퓨터공학과 졸업프로젝트로,  
중고 교재 판매·구매뿐 아니라 구해요 게시판, 채팅, 거래 상태 관리, 리뷰, 장소 정보 등을 하나의 서비스 흐름으로 구성했습니다.

> 이 저장소는 팀 전체의 최종 통합 코드입니다.  
> 문하늘의 개인 기여는 **요구사항 구체화 · Use Case · 화면 설계 · Frontend 연결**을 중심으로 설명하며, Backend / DB / 인프라 전체를 개인 구현으로 주장하지 않습니다.

---

## 1. Project Overview

- **프로젝트:** HongBookStore / 홍책방
- **기간:** 2025.03 ~ 2025.11
- **형태:** 4인 팀 졸업프로젝트
- **문제 영역:** 대학생 중고 교재 거래, 거래 전후 정보 공유, 사용자 간 커뮤니케이션
- **서비스 대상:** 홍익대학교 학생

초기 기획·요구사항 산출물은 별도 초기 개발 저장소에 남아 있습니다.

- [초기 기획 저장소](https://github.com/moonaneul/hong-bookstore)
- Requirement List
- 단계별 기능 설명
- Use Case Diagram
- 주차별 제안서 / 진행자료
- 설문 결과
- 의사결정 정리 자료

---

## 2. Problem

중고 교재 거래는 일반 중고거래와 달리 **학교·수업·교재라는 맥락**이 중요합니다.

단순히 판매글만 제공하면 다음 문제가 남습니다.

- 필요한 교재를 정확히 찾기 어려움
- 판매 중인 글이 없으면 구매 의사를 표현하기 어려움
- 거래 전 질문과 일정 조율을 별도 메신저에서 해야 함
- 거래 상태를 서비스 안에서 추적하기 어려움
- 거래 이후 상대방에 대한 신뢰 정보를 남기기 어려움

HongBookStore는 이를 하나의 서비스 안에서 이어지도록 구성했습니다.

---

## 3. Main Service Flow

```text
교재 탐색
→ 판매글 확인
→ 찜 / 최근 본 글
→ 판매자와 채팅
→ 거래 예약 / 상태 변경
→ 거래 완료
→ 상대방 평가 / 후기
```

판매 중인 교재가 없을 경우에는 `구해요` 게시판에서 구매 의사를 등록하고 댓글·대댓글로 정보를 주고받을 수 있습니다.

---

## 4. Team Features

최종 통합 저장소에서 확인되는 주요 기능은 다음과 같습니다.

### 교재 거래
- 판매글 검색 / 필터 / 정렬
- ISBN 기반 등록 / 직접 등록
- 이미지 업로드
- 판매 상태 변경
- 찜하기
- 최근 본 글

### 구해요 게시판
- 글 작성 / 수정 / 삭제
- 댓글 / 대댓글

### 거래 커뮤니케이션
- STOMP WebSocket 기반 채팅
- 채팅방 / 메시지
- 거래 예약 요청 / 수락 / 취소 / 완료
- SSE 알림

### 사용자 / 인증
- OAuth2
- JWT
- 학생 인증 메일
- 프로필 관리

### 후기 / 정보
- 장소 리뷰
- 거래 상대 평가
- 지도 / 장소 검색
- 외부 도서 검색
- 날씨 정보
- 유해 표현 필터

> 위 기능은 **팀 전체 결과**이며, 전부를 문하늘 개인 구현으로 표현하지 않습니다.

---

## 5. My Contribution

제가 맡은 프로젝트의 핵심은 **기획 내용을 실제 구현 기준으로 구체화하고, 그 기준을 화면 설계와 Frontend 구현으로 연결한 것**입니다.

### 검증된 / 확인된 개인 기여

- 서비스 기능 요구사항을 Requirement List 형태로 구체화
- 사용자 행동과 시스템 기능을 Use Case로 정리
- 기능별 단계와 필요한 의사결정 항목 문서화
- 화면 구조와 사용자 흐름 설계
- Figma 기반 화면 설계
- 설계 내용을 Frontend 구현에 연결

초기 저장소에는 실제로 다음 산출물이 남아 있습니다.

- `requirement list.xlsx`
- `step by step description.xlsx`
- `use case diagra,.mdj`
- `결정해야 하는 사항 정리.xlsx`
- 주차별 요구사항 명세서

Figma 원본 파일은 현재 GitHub 저장소에 포함되어 있지 않으므로,  
Figma 작업은 **본인 확인 사실**로만 사용하고 GitHub 산출물과 동일한 수준의 증거로 취급하지 않습니다.

### 담당하지 않은 범위

- DB 설계
- Backend 전체 구현
- Redis / WebSocket / 인증 인프라 전체 구현
- 배포 / Cloud 구조 전체 설계

자세한 범위:
- [Contribution](./docs/CONTRIBUTION.md)
- [Limitations](./docs/LIMITATIONS.md)

---

## 6. Why This Project Matters in My Portfolio

이 프로젝트에서 보여주려는 것은 기술 스택의 개수가 아니라 다음 과정입니다.

```text
아이디어
→ 요구사항 정의
→ 기능 단위 구체화
→ Use Case
→ 화면 설계
→ Frontend 구현 연결
```

즉, 모호한 서비스 아이디어를 개발 가능한 수준의 요구사항과 사용자 흐름으로 바꾸고  
문서에서 끝내지 않고 실제 서비스 화면까지 연결한 경험입니다.

---

## 7. Team Architecture

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

### Team Stack

- **Frontend:** React, Vite, React Router, React Query, styled-components
- **Backend:** Java 21, Spring Boot, Spring Security, JPA, WebSocket
- **Data:** MySQL, Redis
- **Infra / External:** Docker, GCP, Vercel, GitHub Actions, 외부 API

### My Working Scope

- 요구사항 / Use Case / 기능 흐름 정리
- UX / 화면 구조
- Figma 화면 설계
- Frontend 구현 연결

팀 전체 기술 스택을 개인 숙련 기술 목록으로 그대로 사용하지 않습니다.

---

## 8. Repository Structure

```text
src/main/java/com/hongik/books   # Team Backend
src/main/resources               # Backend resources
src/main/frontend                # Team Frontend
deploy                           # Deployment configuration
Dockerfile
```

초기 기획·요구사항 산출물은  
[moonaneul/hong-bookstore](https://github.com/moonaneul/hong-bookstore)에서 확인할 수 있습니다.

---

## 9. Local Run

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

## 10. Portfolio Boundaries

현재 다음과 같은 표현은 사용하지 않습니다.

- “프로젝트 전체를 PM으로 이끌었다”
- “DB를 설계했다”
- “Backend 아키텍처를 설계했다”
- “Redis / 동시성 / 대규모 트래픽을 직접 해결했다”
- “전체 시스템을 단독 개발했다”
- 근거가 없는 성능 / 사용자 수 / 효율 개선 수치

이 프로젝트의 개인 기여는 **요구사항 → Use Case → UX → Frontend 연결** 범위를 중심으로 설명합니다.

---

## 11. Documents

- [My Contribution](./docs/CONTRIBUTION.md)
- [Limitations & Evidence Boundaries](./docs/LIMITATIONS.md)
- [Early Planning Repository](https://github.com/moonaneul/hong-bookstore)
