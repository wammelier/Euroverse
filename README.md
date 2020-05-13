# :airplane: Euroverse (여행서비스 사이트)

유렵여행을 계획중인 사람들을 위해 여행계획표작성 서비스 커뮤니티를 통한 정보습득 서비스 동행찾기 서비스 알람서비스, 채팅서비스, 여행일정계획서비스, 동행찾기서비스, 동행채팅서비스 와같은 a~z까지의 서비스를 제공하는 여행계획커뮤니티 홈페이지 입니다. 

<img width="1792" alt="스크린샷 2020-05-13 오후 4 42 06" src="https://user-images.githubusercontent.com/57661474/81785232-005d2400-9539-11ea-8646-49cc5dff27e3.png"> [메인화면 사진입니다.]

### :point_right: <a href="http://13.209.169.241:8080">Euroverse</a> :point_left: 사이트 바로가기

* * *
# :blue_book:목차
## 1.
## 2.
## 3.
## 4.
## 5.
## 6.
### main.jsp 환율정보조회main.jsp

<img width="461" src="https://user-images.githubusercontent.com/57661474/79734897-68ea2400-8332-11ea-8f95-9767da857049.png">

환율정보조회는 foriegnApi를 이용하여 javaScript만으로 구현한 서비스이다.
환율정보를 원하는 국가를 선택할시 국가에 해당하는 iso코드를 통해 환율을 구하고 그 퍼센테이지를 통해 금액을 산출한다.

### main.jsp 이미지 랜덤출력

<img width="461" src="https://user-images.githubusercontent.com/57661474/79734897-68ea2400-8332-11ea-8f95-9767da857049.png">

이미지 랜덤출력은 java에서 발생시킨 난수를 이용하여 각 이미지를 화면에 랜덤으로 출력하여 사용자에게 보여주는 서비스이다.

### admin의 회원정보조회 (getUserList.jsp)

<img width="461" src="https://user-images.githubusercontent.com/57661474/79735819-d2b6fd80-8333-11ea-9694-d7411a8de7e7.png">

사이트에 가입된 회원들의 정보를 보여주는 getUserList.jsp 는 가입한 유저들을 List형태로 보여준다.
홈페이지에 가입된 유저들의 정보를 보여주며 검색은 ajax의 비동기방식을 이용하여 request없이 바로 정보를 출력한다.


### admin의 qna게시판 관리(getQnaList.jsp)

<img width="461" src="https://user-images.githubusercontent.com/57661474/79736149-5375f980-8334-11ea-8746-6fa818943bc2.png">

사이트에 가입된 회원들이 작성한 qna질문 게시판에 게시글에 답변을 달수 있는 게시판이다. ajax의 비동기 처리방식을 이용하여 답변, 삭제를 구현하였다.

### admin의 신고게시판 관리(gerReportList.jsp)

<img width="461" src="https://user-images.githubusercontent.com/57661474/79735847-e19db000-8333-11ea-942b-da286fa127e9.png">

사이트를 이용하는 회원들이 불필요한 게시물을 신고하는 경우 관리자가 신고된 게시글의 내용 게시글 제목 댓글 내용 등을 확인할수 있고 이를 규제시 해당하는 댓글과 게시글은 게시판에서 플래그처리를통해 회원들에게 보여주지 않는다. (실제 디비에는 계속 남아있으며 삭제처리하지 않고 플래그로 처리하여 해당하는 게시물 댓글을 생략하고 출력하는 구조이다.)


