## 토이 프로젝트

### Backend

#### Java(Spring)

- [나홀로 웹에][alone-github]
  - SpringBoot로 배포단계까지 구현한 웹서비스입니다. 스프링 이니셜라이저를 사용하지는 않고, 직접 Gradle에 플러그인 의존성을 위한 관리를 설정하였습니다. JUnit4로 단위 테스트 코드를 작성하였습니다.
  - 인메모리형 관계형 데이터베이스인 h2를 Spring Data JPA를 이용하여 테스트 단계에서 사용하였습니다. 템플릿 엔진으로는 Mustache를 사용하였으며, 스프링 시큐리티와 OAuth 2.0으로 로그인 기능을 구현하였습니다.
  - AWS EC2 인스턴스를 생성하여 서버를, RDS로 관계형 데이터베이스를 구현하여 연동하였습니다. 파일 서버인 S3를 이용하여 배포 파일들을 관리하였으며 Travis CI와 연동하여 배포를 자동화하였습니다. 마지막으로 nginx를 이용하여 무중단 배포를 구현하였습니다.
- [평화지수 웹 어플리케이션][peace-github]
  - SpringBoot로 구현한 웹서비스입니다. 스프링 이니셜라이저를 사용하였으며 Maven을 이용하여 의존성을 관리하였습니다.
  - Maria DB를 Spring Data JPA를 이용하여 API, 페이지 처리 및 검색, @OneToMany 관계 설정, FetchType 설정, 커스텀 쿼리 작성 등을 구현하였습니다.
  - 템플릿 엔진으로는 타임리프를 사용하였으며, 부트스트랩을 참고하여 주요 레이아웃과 버튼 그리고 폼을 작성하였습니다. 스프링 시큐리티를 이용하여 로그인 처리를 하였습니다.
- [부스트코스 풀스택 개발자 과정 백엔드][back-github]
  - SpringMVC를 사용하여 API, Cookie 및 Session, 인터셉터, 아규먼트 리졸버, 로깅, 파일 업로드 및 다운로드 등을 구현한 프로젝트 입니다.
  - 자바로 JSP와 서블릿을 실행할 수 있는 환경을 제공하는 Tomcat을 사용하여, Model, View, Controller를 모델을 이해하고 구현하였습니다.
  - MySQL 데이터 베이스와 Spring JDBC를 사용하였습니다.

#### Python(Django, FastAPI)

- [Django를 이용한 URL Shortener와 블로그 만들기][django-web]
  - 블로그의 경우 글쓰기 수정, 삭제, 댓글 기능을 구현하였습니다. 부트스트랩 4.5.3을 사용하였으며 Django에서 기본적으로 제공하는 admin page를 사용합니다. /feed url에 RSS를 구현하였습니다.
  - Docker-compose를 사용하여 Django와 Nginx로 두 개의 도커를 구동한 뒤 포트와 uwsgi 설정을 연결하였습니다.
- [FastAPI를 이용한 웹 어플리케이션][fast-api]
  - 비동기/ 병렬 처리를 지원하는 파이썬 기반의 웹 프레임워크인 FastAPI를 이용한 프로젝트입니다.
  - 파이썬은 객체를 참조하는 객체들의 갯수를 기록한 뒤, 그 갯수가 0이 되면 메모리를 정리합니다. 이에 복수의 스레드 이용을 방지하는 GIL이 걸려져 있습니다. 이에 파이썬은 비동기/병렬 처리를 위하여 코루틴이라는 기법을 사용합니다.
  - 블로그 포스팅에 따로 [비동기/ 병렬 처리와 코루틴][concurrency-parallelism]에 대한 내용을 공부하고 정리하였습니다.

### Frontend

- [벨로퍼트와 함께하는 모던 리액트][begin-react-github]
  - [깃북 주소][begin-react-gitbook]
  - React, React Router, Redux, Redux Middleware, Typescript
- [부스트코스 풀스택 개발자 과정 프론트엔드][front-github]
  - Vanilla JS
- [To-Do-List 만들기][react-github]
  - React

### Full_Stack

- [React와 Spring으로 인증서버 만들기][react-spring-auth]
  - React와 Typescript로 로그인/회원가입 페이지만들기
  - Spring과 Spring Security로 salt를 사용하는 토큰을 사용한 인증 기능 구현
  - Redis를 Token을 저장하고 파기하는 캐시 DB로 사용/ MySQL를 유저 정보를 저장 및 확인하는 사용자 DB로 사용
  - Google SMTP로 회원가입 메일 발송

### Big_Data

- [도커 컴포즈로 하둡 클러스터 만들기][docker-hadoop]
  - Docker Compose를 이용하여 복수의 컨테이너들을 설치하였습니다.
  - Mapreduce 실습을 위한 jar 파일을 namenode 컨테이너에 복사한 뒤 hdfs에 업로드하였습니다.
  - hadoop jar 명령어로 맵리듀스 작업을 실행합니다.
- [하둡 스파크, 카프카 프로젝트][hadoop-mapreduce-github]
  - 하둡 맵리듀스 설치 후 기본적인 명령어들을 실습하였고, hdfs 등 관련된 내용을 정리하였습니다.
  - 도커와 제플린을 사용하여 하둡 스파크의 기본적인 명령어들을 scala로 실습하였습니다.
  - AWS를 이용하여 하둡 카프카 실습한 내용 또한 정리중입니다.

### Data_Science

- [국회의원의 FTA 반응성에 대한 연구: 지역구 산업 비율과 FTA 발언 횟수의 상관관계][python-r-congress]

### et_cetera

- [자바 병렬 프로그래밍][concurrency-github]
- [자바 계산기][calculator-github]

## 이력

- 서울대학교 정치외교학과 졸업
- 공군 만기 전역
- 서울대학교 빅데이터 핀테크 과정 수료
- 에이젠 글로벌 인턴
- 서울대학교 외교학 전공 대학원 수료(베이즈 통계학, 국제정치경제학 전공)
- 스마일게이트 스토브 개발 캠프 2기 참여
- SK텔레콤 서버 백엔드 개발자

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

