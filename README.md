# 📌 Petrasche
- 반려인을 위한 애견 커뮤니티
- 사이트 링크: [https://www.petrasche.com](https://www.petrasche.com)

## 1. 제작 기간 & 참여 인원
- 2022.07.07(목) ~ 2022.08.04(목)
- 팀 프로젝트(5명)

## 2. 사용 기술
<div style='flex'>
<img src="https://img.shields.io/badge/Python3.10.5-3776AB?style=for-the-badge&logo=Python&logoColor=white" >
  <img src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=Django&logoColor=white">
  <img  style='float:left' src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=FastAPI&logoColor=white"><img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=JavaScript&logoColor=white">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=HTML5&logoColor=white">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=CSS3&logoColor=white">
</div>


<div style="display:flex">
    <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=PostgreSQL&logoColor=white">
    <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=Docker&logoColor=white">
	<img src="https://img.shields.io/badge/Amazon EC2-FF9900?style=for-the-badge&logo=Amazon EC2&logoColor=white">
	<img src="https://img.shields.io/badge/Amazon RDS-527FFF?style=for-the-badge&logo=Amazon RDS&logoColor=white">

</div>

## 3. 아키텍쳐 및 ERD 설계
![img_1.png](/static/img_1.png)
![image](https://user-images.githubusercontent.com/104334219/185877181-2682c4d3-743c-46bf-9827-3c6a5ee1eb8f.png)

## 4. 핵심 기능
<details close>
  <summary>📌 로그인/회원가입</summary>
  유효성 검사, 아이디 중복 검사, JWT Token사용, 카카오 소셜 로그인
</details>
<details close>
  <summary>📌 메인페이지</summary>
  - 강아지 히스토리 CRUD<br>
  - 댓글기능<br>
  - 좋아요 기능<br>
  - 팔로우 기능<br>
  - 엘라스틱서치 엔진을 사용한 초성, 해시태그 검색 기능
</details>

<details close>
  <summary>📌 마이페이지</summary>
  - 유저/ 펫 프로필 CRUD<br>
  - 자신의 반려동물 프로필 이미지 등록시 AI로 강아지vs고양이 구분 (fastAPI사용, ec2 분리)<br>
  - DRF페이지네이션<br>
</details>
<details close>
  <summary>📌 산책 매칭 페이지</summary>
  - 매칭 게시판 (CKEditor 사용)<br>
  - 날짜, 지역, 성별, 시간대등 필터 설정으로 검색<br>
  - 실시간 채팅 기능 (Websocket & Django Channels)<br>
</details>

<details close>
  <summary>📌 애견 월드컵</summary>
  - 자신의 반려동물을 자랑하는 이벤트 페이지<br>
  - 이달의 인기 반려동물  (월별 초기화)<br>
</details>

<details close>
  <summary>📌 배포</summary>
  - Docker/EC2사용<br>
</details>

## 5. 핵심 트러블 슈팅

-도커 배포 
배포 전 과정이 아직 익숙하지 않은 상태에서 도커를 처음 배우고 배포하는게 쉽지 않았습니다.

## 6. 기타 트러블 슈팅
<details close>
  <summary>📌EC2배포 초반 sqlite에서 postgreSQL로 바꾸면서 속도가 오히려 줄어든 문제 </summary>
	
  EC2 배포를 처음 시작하면서 로컬에서 했을 때에 비해 속도가 확연하게 줄어든걸 느낄 수 있었습니다.<br>
  개발자도구->Network->fetch 탭에서 확인해봐도 눈에 띄는 속도차이가 드러났습니다.<br>
  이건 내 지식으로 해결하기 어려운 부분이다 싶어서 튜터님들과 잘 아시만한 분들을 찾아갔고,<br>
  EC2 배포할때 지역이 한국이 아닌 캘리포니아로 설정되어 있었단걸 발견했다.<br>
  그 외에도 당시 EC2서버는 내가 배포하고 postgreSQL을 배포한 RDS서버는 다른 팀원이 배포했는데 이게 문제가 될 수 있다는 얘기를 들어,
  RDS도 내가 배포하게 되었다. 
</details>
<details close>
  <summary>📌drf pagination이 settings.py에서 전역설정으로 되지 않는 문제 </summary>
	
  자동 drf 페이지네이션 기능 일반적인 apiview가 아닌 viewsets이나 generic views 사용 할 때만 가능하다.
  pagination.py파일을 만든뒤 mixin을 사용해서 페이지네이션 api 자체를 불러왔다.
</details>
<details close>
  <summary>📌마감 기능 백엔드로 처리시 어려움</summary>
	
  프로젝트 초기에 친구매칭 프로그램의 마감기능을 프론트에서 자바스크립트로 처리했었는데, 이를 리팩토링하는 과정에서 백엔드로 옮겨왔습니다.
  메소드를 마치 필드인 것처럼 취급할 수 있게 해주는 property decorator를 사용해서 생각보다 간단하게 해결할 수 있었습니다. 
<img src='https://user-images.githubusercontent.com/104334219/186092270-471d1c5e-5ee4-460d-bf7a-49af8a72242e.png'>
</details>
<details close>
  <summary>📌팀 협업 문제</summary>
	
  팀 활동 초기에 팀 분위기가 다운되어 있었고, 다들 활동시간이 달라 업무 관련 커뮤니케이션이 잘 되지 않는 문제가 있었습니다.
  매일 점심식사 전에 회의를 하기로 정한 뒤, 시간이 되면 팀원들을 전화해서 불러들이고 회의를 주도해나갔습니다.
  이후 회의 문화와 모르는 것이 있으면 바로 팀원에게 질문하는 문화가 정착이 되었고, 커뮤니케이션이 가장 잘 된 팀중에 하나였다고 생각합니다.
  덕분에 혼자서 하기 어려운 기능들도 함께 도전해보고 성취해낼 수 있었습니다.
</details>


## 7. 성장 & 회고
그 동안 해보고 싶었던 다양한 기능들을 시도해 볼 수 있었고,<br> 구글링을 통해 바닥부터 시작해서 하나씩 구현해 나가는 재미를 느낄 수 있었습니다. <br>
그 외에도 팀원들 디버깅을 도와주는 경험을 통해 문제 해결 능력을 키울 수 있었습니다.<br>
스스로 독립적으로 해나갈 수 있는 범위가 커지면서 코딩에 대한 자신감도 커졌다는 점이 가장 가치있었습니다.<br> 
