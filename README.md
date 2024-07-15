# 게시판 시스템
* 이 프로젝트는 다양한 기능을 갖춘 게시판 시스템을 구현하는 것을 목표로 합니다. 백엔드 기능을 충분히 구현함으로써 완성도 높은 게시판 시스템을 만들고자 합니다.
---
# 사용 기술
* 개발 언어 : Java 17
* 개발 환경 : SpringBoot 3.3.1, gradle 7.2, jpa(Spring Data JPA), Spring Security, Thymeleaf, lombok, gradle 8.8, tomcat
* 데이터베이스 : MySQL
* 형상관리 툴 : GitHub
---
## 사용자 기능
### 1. 공지사항:
* __좋아요 기능:__ 좋아요로 공지의 인기도를 표시.
* __추가 기능:__ 공지사항에 댓글을 달 수 있는 기능 추가.
* **회원가입:**
  
1. 닉네임은 최소 2~10자이며, 특수문자를 제외한 한글, 알파벳 대소문자, 숫자로 구성

2. 이메일 형식 패턴 적용해 확인 

3. 비밀번호는 최소 8~16자 이상이며, 영문 대, 소문자, 숫자, 특수문자를 사용

4. 데이터베이스에 존재하는 아이디를 입력한 채 회원가입 버튼을 누른 경우 "이미 사용중인 닉네임입니다."의 메시지를 보여줌
     - 이는 아이디, 비밀번호, 이메일도 동일함

5. 회원가입이 완료되었다면 로그인 페이지로 이동
6. 회원가입을 하지 않았을 시에는 게시판 내용을 보는 것만 가능
7. 만약 로그인을 하지 않고, 신고/글/댓글 작성을 시도하면 로그인 페이지로 넘어감

* __회원 정보 수정:__ 닉네임과 비밀번호 수정. 과정은 회원가입과 동일함.
* __회원 탈퇴:__ 계정 탈퇴 가능.
* __게시판:__ 게시글 작성, 수정 및 삭제.

1. 제목, 닉네임(username), 작성 내용, 작성 날짜를 조회
  
2. 각각의 게시글에 등록된 모든 댓글을 게시글과 같이 Client에 반환
  
3. 게시글, 댓글 모두 작성 날짜 기준 내림차순으로 정렬

4. 게시글, 댓글, 좋아요 개수 함께 반환
* __댓글:__ 게시글에 댓글 달기, 삭제.
* __대댓글:__ 댓글에 답글 달기, 삭제.
* __조회수:__ 게시글 조회수 표시.
* __좋아요:__ 게시글 인기도 표시.
* __신고하기:__ 부적절한 게시글이나 댓글 신고.
* __이미지 첨부:__ 게시글 및 댓글에 이미지 첨부.
### 3. 통계:
* __총 방문자 수:__ 총 인원수 표시.
* __어제 방문자 수:__ 어제 방문자 수 표시.
## 관리자 기능
* __공지사항 작성:__ 게시판에 공지사항을 작성 및 삭제.
* __메일 전송:__ 중요한 공지를 메일로 발송.
* __관리자 페이지:__ 사용자가 받은 신고수를 확인할 수 있으며, 관리자의 판단하여 사용자를 차단 혹은 차단을 해제할 수 있습니다.
---
# ERD
![ERD파일](https://github.com/seungh22/BoardProject/blob/master/Board_ERD.png)
