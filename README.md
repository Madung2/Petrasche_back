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
## 6. 기타 트러블 슈팅
## 7. 성장 & 회고
그 동안 해보고 싶었던 다양한 기능들을 시도해 볼 수 있었고,<br> 구글링을 통해 바닥부터 시작해서 하나씩 구현해 나가는 재미를 느낄 수 있었습니다. <br>
그 외에도 팀원들 디버깅을 도와주는 경험을 통해 문제 해결 능력을 키울 수 있었습니다.<br>
스스로 독립적으로 해나갈 수 있는 범위가 커지면서 코딩에 대한 자신감도 커졌다는 점이 가장 가치있었습니다.<br> 
