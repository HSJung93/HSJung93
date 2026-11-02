# About
- 백엔드(Spring) 출신 데이터 엔지니어입니다. 2026년부터 통신사 마케팅 본부에서 사내 사업부서에 직접 들어가 데이터 파이프라인·자동화 시스템·AI 코딩 관행을 배포하는 FDE(사내) 역할을 맡고 있습니다.
- 2022~2025년에는 Spring framework(Boot, Security, Gateway)로 일정, 회원/인증, 게이트웨이 도메인의 백엔드를 개발했고, 스트레스 테스트와 모니터링으로 보안·성능·안정성을 입증하며 레거시 시스템을 현대화했습니다.
- 자세한 내용: [hsjung93.github.io/about](https://hsjung93.github.io/about/)

# 2026 — 데이터 엔지니어링 · FDE(사내)
1. 정산 추심 자동화 시스템 개발 (비개발 기획자 2명과 2개월 내 상용 배포)
  - FastAPI 백엔드와 React·PostgreSQL·K8s PaaS 개발 환경 전반을 세팅하고, 착수 2일 만에 프로토타입을 띄워 요건을 구체화했습니다. 외주 4개월 추정을 내부 2개월로 대체했습니다.
  - LLM 메일 초안 기능을 일괄 발송 정책·마스터 키·사번 기반 권한 3단계 뒤에 두어 오발송 리스크를 설계 단계에서 흡수했습니다.
  - 담당자의 정산 현황 분석 시간 75%, 독촉 메일 작성 시간 50%를 절감했습니다. <!-- TODO: [글](https://hsjung93.github.io/posts/vibe-coding-two-months-with-non-engineers/) -->

2. 팀 데이터 파이프라인 공용화 (dbt + Airflow 표준 도입 주도)
  - 노트북·원시 SQL·셸·파이썬 러너 4종으로 흩어진 파이프라인을 저장소 진단 문서로 수치화하고, 전환 계획에 대한 팀 합의를 끌어냈습니다.
  - 역치환 검증과 양방향 EXCEPT 병행 검증으로 결과 동일성을 기계적으로 증명한 뒤 하루 만에 컷오버했습니다.
  - 보호 브랜치·MR 전 정적 확인·MR 본문 규칙을 팀 표준으로 정착시켰습니다(저장소 MR 리뷰 팀 최다). <!-- TODO: [글](https://hsjung93.github.io/posts/adopting-dbt-airflow-in-a-marketing-data-team/) -->

3. 사업부서 월간 통계 데이터 마트 + 대시보드 개발 (7주 MVP)
  - 매월 엑셀로 만들던 통계를 dbt 마트와 React 대시보드로 전환했습니다. "축은 파이프라인, 조합은 화면" 설계로 필터 추가 요청 대부분을 화면 수정만으로 처리했습니다.
  - 골든 테스트와 dbt 실행 현황 페이지로 비개발 사용자가 숫자 변화를 스스로 확인할 수 있게 했습니다. Vitest 500건과 커버리지 게이트로 품질을 유지했습니다. <!-- TODO: [글](https://hsjung93.github.io/posts/adopting-dbt-airflow-in-a-marketing-data-team/) -->

4. 캠페인 효과 측정 실험 설계 및 오픈소스 기여
  - 플래그십 캠페인 MMS의 순수 효과를 측정하기 위해 100만/100만 규모 무작위 대조 실험 2회를 설계·실행했습니다. 해시 기반 분할로 재현성을 확보하고, 집계 기준 불일치로 역효과처럼 보이던 결과를 ITT 재집계로 바로잡았습니다.
  - uber/causalml Causal Forest의 병렬 학습이 느려지는 결함(Cython linetrace → GIL 경합)을 규명해 [수정 PR](https://github.com/uber/causalml/pull/914)이 v0.17.0에 머지됐습니다. 학습 시간 27분 → 2.6분. [글](https://hsjung93.github.io/posts/causalml-cython-linetrace-perf/) <!-- TODO: [실험 설계](https://hsjung93.github.io/posts/how-big-an-ab-test-for-an-mms-campaign/) [rand(n)](https://hsjung93.github.io/posts/athena-rand-is-not-a-seed/) -->

5. 본부 AI 전환 교육 및 TF 활동
  - 본부 14개 팀 비개발 마케터를 대상으로 바이브 코딩·배포 교육 3차수 커리큘럼을 설계하고 강의했습니다. 교안·사전조사 웹페이지를 직접 개발해 배포 과정 자체를 시연했습니다.
  - AI 전환 TF 상근으로 147명의 업무 데이터를 분석하고 과제 8건을 진단해 연 2.4 FTE 절감을 실측했습니다.
  - Claude Code 스킬 마켓플레이스와 저장소 규칙(세션 규칙 파일, 경로별 규칙, 주석 금지, MR 4단 본문)을 팀 표준으로 정착시켰습니다. <!-- TODO: [글](https://hsjung93.github.io/posts/teaching-git-and-nginx-to-marketers/) -->

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
