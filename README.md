# :airplane: Euroverse (여행서비스)

<a href="http://13.209.169.241:8080"><img width="1792px" alt="스크린샷 2020-05-13 오후 4 42 06" src="https://user-images.githubusercontent.com/57661474/81785232-005d2400-9539-11ea-8646-49cc5dff27e3.png"></a> 
:point_up: [이미지를 누르시면 홈페이지로 이동합니다.] (사용아이디 : admin 비밀번호 : 000000)
<br/><br/>

유렵여행을 계획중인 사람들을 위해 여행계획표작성 서비스 커뮤니티를 통한 정보습득 서비스 동행찾기 서비스 알람서비스, 채팅서비스, 여행일정계획서비스, 동행찾기서비스, 동행채팅서비스 와같은 a~z까지의 서비스를 제공하는 여행계획커뮤니티 홈페이지 입니다. 
<br/>
<br/>
<br/>
<br/>

- - -
# :blue_book: 목차
### 1. [개요](https://github.com/wammelier/Euroverse/blob/master/README.md#one-개요)

### 2. [담당모듈](https://github.com/wammelier/Euroverse/blob/master/README.md#two-담당모듈)

### 3. [의존성 및 버전 정보](https://github.com/wammelier/Euroverse/blob/master/README.md#three-의존성-및-버전정보)

### 4. [분석 및 설계 과정](https://github.com/wammelier/Euroverse/blob/master/README.md#four-분석-및-설계-과정)

### 5. [추가학습](https://github.com/wammelier/Euroverse/blob/master/README.md#five-추가학습)

### 6. [참고사항](https://github.com/wammelier/Euroverse/blob/master/README.md#six-참고-사항)

- - -
<br/>

- - -
## :one: 개요

+ 개발 기간 : 2개월
  + 분석 및 설계 : 2020/01/01 ~ 2020/01/23 (1개월)
  + 구현 : 2020/01/24 ~ 2020/03/27 (약 1개월)
+ 총 개발 인원 : 6명
+ 시스템 개요 : MVC Model2 아키텍쳐를 기반으로 한 SpringFrameWork를 이용하여 만든 유럽여행 플래너 및 커뮤니티 사이트입니다. 저희 사이트는 회원관리, 주문관리, 플래너, 커뮤니티, 채팅 및 알람 모듈로 구성되어 있습니다.

       
## :two: 담당모듈

### 1. 환율정보 조회(main.jsp)

<img width="861" alt="스크린샷 2020-05-13 오후 6 28 49" src="https://user-images.githubusercontent.com/57661474/81795985-c6474e80-9547-11ea-82aa-1358d0374a49.png">

환율정보조회는 foriegnApi를 이용하여 javaScript만으로 구현한 서비스입니다.
환율정보를 원하는 국가를 선택할시 국가에 해당하는 iso코드를 통해 환율을 구하고 그 퍼센테이지를 통해 금액을 산출합니다.
<br/>

### 2. 이미지 무한클릭 랜덤출력(main.jsp)

<img width="617" alt="스크린샷 2020-05-13 오후 9 17 19" src="https://user-images.githubusercontent.com/57661474/81811197-37463080-955f-11ea-8e71-229727532d9f.png">

사용자가 사진을 클릭하게될 경우 이미지를 랜덤으로 출력합니다. 여행지의 사진은 Selenium 크롤링을 이용하여 db에 사진을 넣었습니다. 난수를 발생시켜 id 값을 이용하여
db에서 사진을 랜덤으로 출력합니다.

### 3. 관리자 회원관리(getUserList.jsp)

<img width="1169" alt="스크린샷 2020-05-13 오후 9 20 27" src="https://user-images.githubusercontent.com/57661474/81811522-bcc9e080-955f-11ea-9a22-4f37cf0477c8.png">

관리자가 사이트에 가입한 회원들의 목록을 조회할수 있는 게시판을 구현하였습니다. 이 게시판을 통하여 해당하는 회원의 아이디 닉네임을 검색하여 조회또한 가능합니다. ajax를 이용하여 비동기 검색이 가능하게 만들었습니다.

### 4. 관리자 QnA게시판 관리(getQna.jsp)

<img width="1151" alt="스크린샷 2020-05-13 오후 9 23 28" src="https://user-images.githubusercontent.com/57661474/81811704-03b7d600-9560-11ea-91d7-33e5b1b90912.png">

관리자가 회원들이 올린 QnA를 조회하고 해당하는 질문에 답변을 달수있는 게시판을 구현하였습니다. 게시판에 해당하는 CRUD는 ajax 비동기 방식으로 구현하여 삭제 삭제 수정 등록이 비동기로 바로바로 화면에 표시됩니다.

### 5. 관리자 신고게시판 관리(getReportList.jsp)

<img width="1182" alt="스크린샷 2020-05-13 오후 9 25 28" src="https://user-images.githubusercontent.com/57661474/81811889-51344300-9560-11ea-8151-3149ef92c533.png">

회원들이 신고한 게시물 댓글은 관리자의 의해 규제될수있는 게시판을 구현하였습니다. 회원들은 해당하는 게시물/댓글이 불필요하다고 여기질 경우 이를 신고할수 있고 신고된 게시물/댓글은 관리자에 의해 규제되며 규제된 게시물은 flag처리를 통해 게시판에 보여지지 않게됩니다.

## :three: 의존성 및 버전정보
+ Laguage : Java
+ Back-end : Spring Framework 4.0.1 / MyBatis / Apache Tomcat / Selenium
+ Front : HTML5 / BootStrap 4 / CSS3 / jQuery / Ajax / JSP
+ Database : Oracle 10g / MongoDB 3.6.1
+ VCS tool : GitHub
+ IDE : Eclipse

<img width="808" alt="스크린샷 2020-05-13 오후 5 42 52" src="https://user-images.githubusercontent.com/57661474/81812705-783f4480-9561-11ea-986a-8aeccf9ee07c.png">

<img width="811" alt="스크린샷 2020-05-13 오후 9 35 57" src="https://user-images.githubusercontent.com/57661474/81812947-cce2bf80-9561-11ea-8b0e-4cab779d8a95.png">

## :four: 분석 및 설계 과정

1. 주제 선정

    2.1. 업무 분석 : Use Case Modeling
        2.1.1 현업 요구사항 정의서 작성  
        2.1.2 요구사항 추적표 작성
        2.1.3 Use Case 유형정의 작성    
        2.1.4 Use Case Diagram 작성    
        2.1.5 Use Case 정의서 작성
    
    2.2. 업무 분석 : Application Modeling
        2.2.1 Class Diagram 작성    
        2.2.2 VOPC(View Of Participating Class) Diagram 작성

    2.3. 화면 분석
        2.3.1 화면 정의서 작성

    2.4. 데이터 분석(Logical)
        2.4.1 ERD(Logical) 작성
        
    3.1 업무 분석 : Application Modeling 
        3.1.1 설계표준 정의
        3.1.2 Class Diagram 작성
        3.1.3 VOPC(View Of Participating Class) Diagram 작성

    3.2 화면 분석
        3.2.1 화면 정의서 

    3.3 데이터 분석(Physical)
        3.3.1 ERD(Physical) 작성
        3.3.2 테이블 목록 작성
        3.3.3 테이블 정의서 작성
        
## :five: 추가학습

### **⚡️ AWS 이용한 배포
학원 수료 후 AWS를 이용해 배포를 해보았습니다. 아마존 **EC2**의 **인스턴스**를 2개 생성하여 각각 **웹 서버와 MongoDB**를 설치하였고, 아마존 **RDS**를 이용하여 Oracle 12를 설정했습니다. 각 인스턴스끼리 연동을 한 뒤 **탄력적 IP**를 생성하여 고정 IPv4 주소를 연결했습니다. 현재(2020/04/24) 셀레늄 구동을 완성하지 못해 항공권 검색과 숙소 검색 기능은 작동하지 않습니다.
  
## :six: 참고 사항  

**프로젝트 구현 홈페이지 링크**

<a href="http://13.209.169.241:8080"><img width="200px" alt="스크린샷 2020-05-13 오후 4 42 06" src="https://user-images.githubusercontent.com/57661474/81785232-005d2400-9539-11ea-8646-49cc5dff27e3.png"></a> :point_left: 클릭하세요!

**프로젝트 발표 영상(썸네일 클릭 시 이동)**

[![](https://img.youtube.com/vi/xGH5Dzj8rAY/mqdefault.jpg)](https://youtu.be/xGH5Dzj8rAY)

**프로젝트 포토폴리오 자료**

[Euroverse Document - 최종안.pdf](https://github.com/wammelier/Euroverse/files/4621995/Euroverse.Document.-.pdf)






- - -
