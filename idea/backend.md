# backend

## 1.sendbox 이용
### process
- 유저 : 문제풀이 SQL 전송
- 서버 : sendbox 생성
- 서버 : 문제DB 생성 및 적용
- 서버 : 유저관련 처리
- 유저 : 결과 확인
- 서버 : sendbox 삭제

### idea
...

### advantage
- 일반적인 온라인 저지에서 사용된다.

### problem
- 복잡하다.
- window 서버에서 불가능 할 것 같다.

---

## 2.한개의 DB를 여럿이서 공유하는 구조
### process
- 유저 : 문제풀이 SQL 전송
- 서버 : DB에 SQL 적용후 반환
- 서버 : 유저관련 정보 처리
- 유저 : 결과 확인

### idea
...

### advantage
- ...

### problem
- 하나의 DB에 여러명의 접속으로 부하가 생길것이다. 여러개의 DB를 만들어 부하를 분산하면 괜찮을지도 모르겠다.
- SELECT 밖에 사용할수 없다.

---

## 3.각회원마다 DB를 한개씩 가지는 구조

### process
- 유저 : 회원가입
- 서버 : DB생성
- 유저 : 문제풀이 SQL 전송
- 서버 : 유저의 DB에 문제 DB에 있는 table 복사
- 서버 : 유저의 DB에 SQL 적용후 반환
- 서버 : 유저관련 정보 처리
- 유저 : 결과 확인
- 서버 : 유저의 DB에서 문제 table 삭제

### idea
...

### advantage
- 안전하게 DML, DCL 을 작성 할 수 있다.

### problem
- DB서버 작업량 많아 부하가 생길것같다.
