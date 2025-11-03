# About
- 4년차 백엔드 엔지니어로 Spring framework(Boot, Security, Gateway)를 사용하여 일정, 회원/인증, 게이트웨이 도메인의 개발을 경험하였습니다.
- 단순 기능 개발을 넘어, 스트레스 테스트와 모니터링으로 시스템의 보안, 성능, 안정성을 입증하고, 레거시 시스템을 현대화하며, 신기술(LLM, Reactive)을 비즈니스에 성공적으로 적용한 경험을 보유하고 있습니다. 

# 주요 성과 및 역할
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
- SK텔레콤 서버 백엔드 개발자 [2022.01.01 ~ 현재]
- 스마일게이트 스토브 개발 캠프 2기 참여 
- 서울대학교 외교학 전공 대학원 수료(베이즈 통계학, 국제정치경제학 전공)
- 에이젠 글로벌 인턴
- 서울대학교 빅데이터 핀테크 과정 수료
- 공군 만기 전역
- 서울대학교 정치외교학과 졸업

# 토이 프로젝트

## Web
- [React와 Spring으로 풀스택 인증서버 만들기][react-spring-auth]
- [평화지수 웹 어플리케이션][peace-github]
- [Django를 이용한 URL Shortener와 블로그 만들기][django-web]
### Backend
- [나홀로 웹에][alone-github]
- [부스트코스 풀스택 개발자 과정 백엔드][back-github]
- [자바 병렬 프로그래밍][concurrency-github]
- [자바 계산기][calculator-github]
- [FastAPI를 이용한 웹 어플리케이션][fast-api]
### Frontend
- [벨로퍼트와 함께하는 모던 리액트][begin-react-github]
- [부스트코스 풀스택 개발자 과정 프론트엔드][front-github]
- [To-Do-List 만들기][react-github]

## Data Science/ Engineering
- [국회의원의 FTA 반응성에 대한 연구: 지역구 산업 비율과 FTA 발언 횟수의 상관관계][python-r-congress]
- [메타버스 체류 시간 리텐션 비교][metaverse]
- [도커 컴포즈로 하둡 클러스터 만들기][docker-hadoop]
- [하둡 스파크, 카프카 프로젝트][hadoop-mapreduce-github]

[react-github]: https://github.com/HSJung93/-React-ToDoList
[concurrency-github]: https://github.com/HSJung93/-Java-ConcurrencyInPractice

<!-- [resume-page]: {{ site.baseurl }}/blog/development-blog -->

[peace-github]: https://github.com/HSJung93/-Java-WebPeaceIndex
[hadoop-mapreduce-github]: https://github.com/HSJung93/-Java-Backend-HadoopMapreducePractice
[back-github]: https://github.com/HSJung93/-Java-Backend-SpringMVCPractice
[front-github]: https://github.com/HSJung93/frontend_practice
[calculator-github]: https://github.com/HSJung93/Calculator
[alone-github]: https://github.com/HSJung93/alone-webservice
[fast-api]: https://github.com/HSJung93/FastAPIProject
[concurrency-parallelism]: https://hsjung93.github.io/%EC%BD%94%EB%93%9C/2021/09/14/coroutine.html
[docker-hadoop]: https://github.com/HSJung93/DockerHadoop
[git-co-work]: https://github.com/HSJung93/-Git-forGitTest
[django-web]: https://github.com/HSJung93/django_docker
[python-r-congress]: https://github.com/HSJung93/-Python-R-CongressFTA
[begin-react-github]: https://github.com/HSJung93/begin-react
[begin-react-gitbook]: https://react.vlpt.us/
[react-spring-auth]: https://github.com/HSJung93/spring-auth-token
[metaverse]: https://github.com/HSJung93/junior_talent_experiment/blob/master/analysis.ipynb

