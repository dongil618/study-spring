# 프로젝트 개요

## 프로젝트 명 : 스프링 입문 주차 개인 과제

### 유튜브 영상 및 과제 링크
- <a href="https://youtu.be/x1WEjLpU8Cw" target="_blank">스프링 입문 주차 개인 과제 유튜브 영상</a>
- <a href="http://s-f-s.shop" target="_blank">http://s-f-s.shop</a>

### 요구사항

- 서비스 완성
  1. 전체 게시글 목록 조회 API
     - 제목, 작성자명, 작성 날짜를 조회하기
     - 작성 날짜 기준으로 내림차순 정렬하기
  2. 게시글 작성 API
     - 제목, 작성자명, 비밀번호, 작성 내용을 입력하기
  3. 게시글 조회 API
     - 제목, 작성자명, 작성 날짜, 작성 내용을 조회하기(검색 기능이 아닙니다. 간단한 게시글 조회만 구현해주세요.)
  4. 게시글 수정 API
     - API를 호출할 때 입력된 비밀번호를 비교하여 동일할 때만 글이 수정되게 하기
  5. 게시글 삭제 API
     - API를 호출할 때 입력된 비밀번호를 비교하여 동일할 때만 글이 삭제되게 하기
- AWS 배포
  1. RDS 연결
     - MySQL을 이용하기
  2. EC2 배포
     - Ubuntu EC2 를 구매한 뒤, 8080 포트와 80번 포트를 연결하여 포트 번호 없이도 서비스에 접속 가능하게 하기

### 환경
- Java 8
- Spring Boot 2.7.1
- IntelliJ Ultimate 2022.1
- Spring Web
- Lombok
- H2
- JPA
- MySQL


## API 설계

|  화면  |      기능      | Method |    URL     |    Return    |
|:----:|:------------:|:------:|:----------:|:------------:|
| 메인화면 | 전체 게시글 목록 조회 |  GET   |   posts    | Lsit\<Post\> | 
| 메인화면 |    게시글 조회    |  GET   | posts/{id} |     Post     | 
| 메인화면 |    게시글 작성    |  POST  |   posts    |     Post     |
| 메인화면 |    게시글 수정    |  PUT   | posts/{id} |     Long     |  
| 메인화면 |    게시글 삭제    | DELETE | posts{id}  |     Long     | 


