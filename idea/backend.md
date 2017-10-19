# backend

## 3.각회원마다 DB를 한개씩 가지는 구조

### process
- 유저 : 회원가입
- 서버 : DB생성
- 유저 : 문제풀이 SQL 전송
- 서버 : 유저의 DB에 문제 table 생성
- 서버 : 유저의 DB에 SQL 적용후 반환
- 서버 : 유저관련 처리
- 유저 : 결과 확인
- 서버 : 유저의 DB에서 문제 table 삭제

### advantage
- 안전하게 DML, DCL 을 작성 할 수 있다. 

### problem
- DB서버 작업량 많음
