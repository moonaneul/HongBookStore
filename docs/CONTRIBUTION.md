# HongBookStore Contribution

이 문서는 HongBookStore에서 **팀 전체 결과와 문하늘의 개인 기여를 분리**하기 위한 포트폴리오용 기록입니다.

---

## 1. Team Context

- 4인 팀 졸업프로젝트
- 2025.03 ~ 2025.11
- 홍익대학교 학생 대상 중고 교재 거래 / 정보 공유 서비스

최종 Repository에는 Frontend, Backend, DB, 인증, 채팅, 외부 API, 배포 설정까지 팀 전체 결과가 통합되어 있습니다.

---

## 2. My Role

한 문장으로 정리하면:

> **서비스 아이디어를 실제 개발 가능한 요구사항과 Use Case로 구체화하고, 화면 구조를 설계해 Frontend 구현까지 연결했습니다.**

---

## 3. Requirement Definition

초기 기획 Repository에 다음 산출물이 남아 있습니다.

- `requirement list.xlsx`
- `step by step description.xlsx`
- `결정해야 하는 사항 정리.xlsx`
- 주차별 요구사항 명세서

이 자료를 통해 기능을 단순 아이디어 수준에 두지 않고,

- 누가 사용하는지
- 어떤 행동을 하는지
- 어떤 기능이 필요한지
- 어떤 예외나 정책을 정해야 하는지

를 기능 단위로 구체화했습니다.

해당 문서의 대부분을 직접 작성했다는 점은 **사용자 확인 사실**이며, GitHub 파일 존재 자체가 개인 단독 작성자를 증명하지는 않습니다.

다만 추가로 제공된 프로젝트 시트에서는 팀 의사결정 표에 `문하늘`이라는 개인 열이 존재하고, 다음과 같은 안건에 직접 의견을 남긴 기록을 확인했습니다.

- 거래를 위해 등록한 장소를 홍익지도에서 활용할지
- 위치 등록을 주소 입력 / 현위치 중 어떻게 제공할지
- 장소 코멘트 사진 개수
- 거래·장소 경로에 교통수단을 포함할지
- AI chatbot을 버튼 / 직접 입력 중 어떤 방식으로 제공할지
- 미인증 회원 권한
- 아이디 / 닉네임 정책
- 거래 평가 방식
- 신고 처리 방식

따라서 **팀 제품 정책 논의에 실제로 참여했다는 점은 자료로 직접 확인됩니다.**

---

## 4. Use Case

초기 Repository에는 StarUML 기반 Use Case 파일이 남아 있습니다.

- `use case diagra,.mdj`

사용자 행동과 시스템 기능의 관계를 시각적으로 정리하고, 이후 화면 / 기능 설계의 기준으로 활용했습니다.

Use Case 작업의 주요 작성자가 문하늘이라는 점은 **사용자 확인 사실**입니다.

---

## 5. UX / Figma

문하늘은 화면 구조와 Figma 설계를 담당했다고 확인했습니다.

다만 Figma 원본은 현재 GitHub Repository에 포함되어 있지 않기 때문에 증거 수준을 구분합니다.

### 확인된 사실
- 화면 설계를 수행했다는 본인 확인
- 실제 최종 서비스에 React 기반 Frontend가 존재
- 요구사항 / Use Case 산출물이 초기 저장소에 존재

### 추가 증거가 있으면 강화 가능한 부분
- Figma 원본 링크
- 화면별 담당 범위
- Figma와 실제 화면의 대응 자료

현재 포트폴리오에서는 “UI/UX 전체를 단독 설계했다”보다  
**“요구사항과 Use Case를 바탕으로 Figma 화면 설계를 진행했다”**고 표현합니다.

---

## 6. Frontend

설계 내용을 실제 Frontend에 연결한 경험이 있습니다.

최종 Team Frontend에는 React / Vite 기반으로 판매글, 게시판, 채팅, 거래, 마이페이지 등 여러 화면이 통합되어 있습니다.

다만 현재 GitHub만으로는 최종 Frontend의 모든 파일에 대한 개인별 소유권을 분리하기 어렵습니다.

따라서 안전한 표현은:

> **요구사항과 화면 설계를 Frontend 구현으로 연결했다.**

이며,

> “최종 Frontend 전체를 단독 개발했다”

는 표현은 사용하지 않습니다.

---

## 7. Not My Work

문하늘 개인 기여로 주장하지 않는 범위:

- DB 설계
- Spring Backend 전체
- 인증 / Security 전체
- WebSocket / Redis 전체
- 서버 아키텍처 전체
- 배포 / Cloud 전체
- 외부 API 전체 연동

해당 기능은 팀 전체 결과로만 설명합니다.

---

## 8. Evidence

### Repository evidence
- [Final Repository](https://github.com/moonaneul/HongBookStore)
- [Early Planning Repository](https://github.com/moonaneul/hong-bookstore)

### Additional provided evidence
- 프로젝트 포스터: 4명의 Developer 중 문하늘 이름 확인
- 프로젝트 시트 모음: 기능 명세서 / 사용자 중심 요구사항 정의서 / 화면 정의서 / Requirement List / Step-by-step / 의사결정 / 권한 / Use Case 모음 확인
- 의사결정 시트: `문하늘` 열에 다수의 직접 의견 기록 확인

### Early artifacts
- Requirement List
- Step-by-step Description
- Use Case Diagram
- Decision List
- Weekly Requirement Specifications
- Proposal / Progress Materials

---

## 9. Interview-safe Description

> **홍책방은 홍익대 학생을 위한 중고 교재 거래 서비스 졸업프로젝트입니다. 저는 DB나 Backend를 맡기보다 초기 서비스 요구사항을 기능 단위로 구체화하고 Use Case와 화면 구조를 정리하는 역할을 했습니다. Requirement List와 Use Case를 만들고 Figma로 화면을 설계한 뒤 Frontend 구현까지 연결했습니다. 최종 서비스에는 채팅, 거래 상태, 인증 등 다양한 기능이 있지만 이 기능 전체를 제 개인 구현으로 설명하지 않고, 제가 직접 맡은 기획·UX·Frontend 연결 범위를 중심으로 설명합니다.**