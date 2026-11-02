# About
- 백엔드(Spring) 출신 데이터 엔지니어입니다. 2026년부터 통신사 마케팅 본부에서 사내 사업부서에 직접 들어가 데이터 파이프라인·자동화 시스템·AI 코딩 관행을 배포하는 FDE(사내) 역할을 맡고 있습니다.
- 2022~2025년에는 Spring framework(Boot, Security, Gateway)로 일정, 회원/인증, 게이트웨이 도메인의 백엔드를 개발했고, 스트레스 테스트와 모니터링으로 보안·성능·안정성을 입증하며 레거시 시스템을 현대화했습니다.
- 자세한 내용: [hsjung93.github.io/about](https://hsjung93.github.io/about/)

# 2026 — 데이터 엔지니어링 · FDE(사내)
1. 비개발 기획자 2명과 정산 추심 자동화 시스템(FastAPI·React·PostgreSQL, K8s PaaS)을 2개월에 상용 배포. 외주 4개월 추정을 대체. LLM 메일 초안을 일괄 발송 정책·마스터 키·권한 3단계 뒤에 두어 오발송 리스크를 설계에서 흡수. 담당자 분석 시간 75%·메일 작성 50% 절감 <!-- TODO: [글](https://hsjung93.github.io/posts/vibe-coding-two-months-with-non-engineers/) -->
2. 팀 파이프라인 4종(노트북·원시 SQL·셸·파이썬 러너)을 dbt + Airflow 표준으로 통합 주도. 저장소 진단 문서로 합의를 끌어내고, 역치환 검증·양방향 EXCEPT 병행 검증으로 하루 컷오버. 보호 브랜치·정적 확인·MR 규칙을 팀 표준으로 정착(MR 리뷰 팀 최다) <!-- TODO: [글](https://hsjung93.github.io/posts/migrating-notebook-sql-to-dbt-safely/) -->
3. 사업부서 월간 엑셀 통계를 dbt 마트 + React 대시보드로 전환(7주 MVP). "축은 파이프라인, 조합은 화면" 설계로 필터 요청 대부분을 화면 수정만으로 처리. 골든 테스트·dbt 실행 현황 페이지로 숫자 신뢰 확보. Vitest 500건, 커버리지 게이트 <!-- TODO: [글](https://hsjung93.github.io/posts/axes-in-pipeline-combinations-in-ui/) -->
4. 플래그십 캠페인 MMS 효과 측정을 위한 100만/100만 무작위 대조 실험 2회 설계·실행. 해시 기반 재현 가능한 분할, ITT 재집계로 역효과 오판 정정. [uber/causalml Causal Forest 병렬 학습 결함(Cython linetrace → GIL 경합) 수정 PR](https://github.com/uber/causalml/pull/914) v0.17.0 머지, 학습 27분 → 2.6분 — [글](https://hsjung93.github.io/posts/causalml-cython-linetrace-perf/) <!-- TODO: [rand(n)](https://hsjung93.github.io/posts/athena-rand-is-not-a-seed/) [ITT](https://hsjung93.github.io/posts/itt-when-denominators-differ/) -->
5. 본부 14개 팀 비개발 마케터 대상 바이브 코딩·배포 교육 3차수 설계·강의. 본부 AI 전환 TF 상근으로 147명 업무 데이터 분석, 과제 8건 진단, 연 2.4 FTE 절감 실측. Claude Code 스킬 마켓플레이스·저장소 규칙을 팀 표준으로 <!-- TODO: [교육](https://hsjung93.github.io/posts/teaching-git-and-nginx-to-marketers/) [팀 표준](https://hsjung93.github.io/posts/claude-code-team-standard-mistakes/) -->

# 2022~2025 — 백엔드
1. 레거시 회원/인증 시스템을 대체하는 신규 회원/인증 시스템 개발.
  - JWE/JWT 토큰 암호화/복호화 기능을 개발하며 스트레스 테스트를 통해 안정성을 검증했습니다.
  - 캡차 및 로그인 정보 동기화 API 개발 시 비동기 처리를 도입하여 성능과 보안을 개선했습니다.
  - 인증 시스템 대체 작업 후. CI 중복 생성된 사용자 보정 작업을 위한 Batch, Soft Delete, DB Unique 제약 조건 추가 작업 등을 진행하였습니다.

2. B2C 캘린더 서비스 개발, B2B 유심 예약 서비스 개발
  - 일정 서비스에 Outlook 연동 기능을 신규 개발, Graph API와 CalDAV 프로토콜 간의 변환을 서버 사이드에서 구현하여 20만 명 이상의 신규 연동 유저를 확보하는 데 핵심적인 역할을 했습니다.
  - 유심 예약 사이트 신규 구축 시, 본인 인증 트래픽 폭증에 대비한 Rate Limiter를 개발/적용하여 장애 확산을 방지했습니다.
  - 보안팀의 모의 해킹 검수 요건(세션 타임아웃, 로그인 실패 처리 등)을 충족하는 대리점 어드민 인증/인가 기능을 Spring Session 기반으로 개발했습니다.

3. 게이트웨이 인프라 구축
  - 웹 서비스 전용 게이트웨이를 신규 구축하여 인증, 라우팅, SSL 처리를 담당했습니다. Spring Reactive 환경에서 SSE(Server-Sent Events)를 지원하고, OpenTelemetry를 적용해 분산 트레이싱 환경을 구축하며 모니터링 가시성을 확보했습니다.

4. 신기술(LLM) 적용 및 개발 문화 개선
  - LLM 기반 신규 Agent 시스템의 백엔드 시나리오(일정 브리핑, 등록/수정/삭제)를 개발하고, 기획부터 배포(Ansible), 로깅(Fluent Bit, Open Search), 모니터링(Prometheus, Grafana)까지 End-to-End 개발을 주도했습니다.
  - Caldav 프로토콜 기반의 복잡한 캘린더 시스템(Artemis, Caldav, iCalendar, Timezone)의 아키텍처와 도메인 지식을 시각화/ 문서화하고, 신규 구성원을 대상으로 기술 설명회를 진행하여 팀의 빠른 적응과 지식 공유에 기여했습니다.

# 이력
- SK텔레콤 마케팅 본부 데이터 엔지니어 · FDE(사내) [2026.03 ~ 현재]
- SK텔레콤 서버 백엔드 개발자 [2022.01 ~ 2026.02]
- 스마일게이트 스토브 개발 캠프 2기 참여 
- 서울대학교 외교학 전공 대학원 수료(베이즈 통계학, 국제정치경제학 전공)
- 에이젠 글로벌 인턴
- 서울대학교 빅데이터 핀테크 과정 수료
- 공군 만기 전역
- 서울대학교 정치외교학과 졸업
