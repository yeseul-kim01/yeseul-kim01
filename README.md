## Hi there 👋  
I'm Yeseul Kim, a passionate developer interested in building practical, real-world solutions using AI, web technologies, and system design.

---

## 🚀 Projects & Collaborations

---

### 🏷️ [LedgerMate](https://github.com/yeseul-kim01/2025-PROJECT_ledgermate-platform)  — 규정 기반 예·결산 어시스턴트 (개인 프로젝트 · 진행중)
총칙/세칙 PDF를 파싱→검색 가능한 청크로 저장하고, 예산/결산 작성 시 규정 근거·분류·코드 추천까지 지원하는 **라이브러리 중심** 파이프라인

🧩 **역할**
기획 · 데이터 모델링 · 백엔드/CLI · 스토리지 설계 · 배포 자동화 전부 단독 수행

🛠 **기술 스택 (현재 + 완료 기준)**

* **Core/Parsing**: Python 3.11, venv, Typer CLI, Requests, python-dotenv, Pydantic, Upstage Document Parse API, HTML Table Extractor, 커스텀 Chunker(heading/문단/표 포함)
* **Reasoning/RAG**: Trigram 검색(pg\_trgm) 기반 규칙 검색, 휴리스틱 룰 매칭, (완성 시) 임베딩 + pgvector, 재랭킹, LLM(Upstage/Solar, OpenAI) 플러그블 전략, 앙상블 오케스트레이션
* **Storage/Infra**: PostgreSQL 14, psycopg3, JSONB, 파일 아티팩트 스토리지(Local/Docker Volume), 다중 테넌시(org\_id) + RLS, 인덱스 최적화(pg\_trgm)
* **Packaging/Dev**: 라이브러리 모듈 구조(`lm-docparse`, `lm-store`, `lm-reasoner`), 편집 설치(-e), 요구사항 프로파일(dev/prod), (완성 시) PyPI 릴리스, pre-commit
* **Ops/배포(완성 시)**: Docker, docker-compose, GitHub Actions CI, (선택) Cloud Run/Render + Cloud SQL/Postgres

📦 **구성/기능**

* **문서 파싱 CLI**: 단일/배치 파싱, 진행 로그/디버그, 표 텍스트+셀 구조 동시 보존
* **청크 스키마**: `{order, code, title, text, path, context_text, tables}` 일관 포맷
* **DB 적재**: `policy`, `rule_chunk`, `artifact`, `budget_doc` 스키마 및 인덱스/보안 정책(RLS) 포함
* **예산안 적재**: 예산안 PDF 업로드→아티팩트 저장→(옵션) 파서 결과 JSON 함께 보관
* **추천 베이스라인**: 규정 키워드/유사도 기반 섹션 서치 → 사업분야/비목 코드 후보 생성
* **확장 가능 설계**: 휴리스틱/LLM/히스토리 기반 추천 전략을 전략 패턴으로 플러그인화

🧪 **예시 워크플로우**

* `parse_policies.py` → PDF 총칙 파싱/청크화
* `ingest_policy_pg.py` → 정책/청크 PostgreSQL 적재
* `ingest_budget_pdf.py` → 예산안 PDF/파싱 결과 아티팩트+메타 저장
* (완성 시) `/reasoner` CLI → 영수증 입력 시 규정 근거·코드 추천, 설명가능 로그 제공

🚀 **목표**

* 라이브러리 우선(API/프론트 없이도 사용) → 기업 환경에 **내장형 SW API**로 통합 용이
* 규정 변화에 강인한 파이프라인 + 플러그블 추론으로 **정확도·추론비용**을 상황별 최적화

---

### 🏫 [WeCampus](https://github.com/wecampus-platform) — 2025 PNU SW 융합 해커톤(예선 수상, 본선 진행중) 대학 협업 플랫폼 (진행중)
- 학생회 및 학과 간 소통, 일정/업무 관리를 위한 플랫폼
- 🛠 **Spring Boot**, **Next.js**, **MySQL**, **Docker**, **GCP**, **GITHUB ACTION**

- 🧩 팀장 및 백엔드 , 서비스 배포 , 일부 프론트 
---

### 🗣 [SpeakNote](https://github.com/2025-AI-SW-Hackathon) — 2025 AI·SW 해커톤 최우수상 , 2025 PNU DAIC 최우수상 수상 (진행중)
- 강의 음성을 요약하여 실시간 주석으로 표시하는 LLM 기반 강의 보조 시스템
- 🛠 **FastAPI**, **React**, **Google STT**, **OpenAI GPT**, **WebSocket** , **PDF.JS** , **Docker** 


- 🧩 PDF 상 실시간 주석 생성 및 배치, 드래그 앤 드롭 기반 인터랙션 UI 구현

- 🔗 FastAPI 기반 AI 서버와 Spring Boot 백엔드 연동, WebSocket 및 REST API 통신 직접 구현

- 🗄 MongoDB 기반 주석 저장 구조 설계, 주석 위치 및 텍스트 저장/복원 기능 구현

- ☁️ GCP VM 기반 전체 인프라 구성 및 배포, AI 서버 및 백엔드 컨테이너화 직접 담당

---

### ☁️ [AI Model Serving Platform](https://github.com/2025-PNU-CC-TERM-PROJECT) (완료)
- 다양한 AI 모델을 Kubernetes + Istio 기반으로 서빙하는 텀 프로젝트
- 🛠 **TorchServe**, **FastAPI**, **Spring Boot**, **Kubernetes**, **Istio**
- 모델 API 개발 및 백엔드 서버 구축

---

### 👩‍🏫 [JUSTICE](https://github.com/PNU-IBE-JUSTICE) — IBE 멘토링 플랫폼 (완료)
- 멘토링 출결·일지·과제 관리를 위한 웹 시스템
- 🛠 **Spring Boot**, **MySQL**, **Thymeleaf**


---

## 💡 Skills & Interests
- **Back-end**: Java, Spring Boot, JPA, MySQL,NoSQL-MONGO, Redis, WebSocket
- **Front-end**: React, Next.js, Tailwind CSS, PDF.js
- **AI/ML**: PyTorch, TorchServe, OpenAI GPT
- **Infrastructure**: Docker, Kubernetes, Istio, GitHub Actions, AWS EC2 , GCP



---

## 📫 Let's connect!
- GitHub: [yeseul-kim01](https://github.com/yeseul-kim01)
- Email: yesul0718@pusan.ac.kr , ysk010718@gmail.com

