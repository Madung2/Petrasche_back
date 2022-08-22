# 📌 Petrasche
- 반려인을 위한 애견 커뮤니티
- 사이트 링크: [https://www.petrasche.com](https://www.petrasche.com)

## 1. 제작 기간 & 참여 인원
- 2022.07.07(목) ~ 2022.08.04(목)
- 팀 프로젝트(5명)

## 2. 사용 기술
<div style='flex'>
<img align='right' src="https://img.shields.io/badge/Python3.-3776AB?style=for-the-badge&logo=Python&logoColor=white" >
  <img align='right'  src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=Django&logoColor=white">
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

📌 Introduction
- 프로젝트면: 펫트라슈
- 사이트: petrasche.com
- 기간: 2022.07.07(목) ~ 2022.08.04(목)
- 김주훈: 웹소켓 실시간 채팅 기능
- 나성근: 엘라스틱 서치 검색기능
- 이민기: 아티클, 댓글, 좋아요, 애견 월드컵
- 엄관용: 마이페이지, 유저프로필, 펫프로필
- 한예슬: 회원가입, 로그인(카카오API), 산책커뮤니티(카카오지도API), 팔로우
- Petrasche_front: https://github.com/Super-fast-decision-making/Petrasche_front
- Petrasche_classification: https://github.com/Super-fast-decision-making/Petrasche_classification
![img_1.png](/static/img_1.png)

📌 로그인/회원가입
- 유효성 검사, 아이디 중복 검사, JWT Token사용, 카카오 소셜 로그인

📌 메인 페이지
- 강아지 히스토리 CRUD
- 댓글 CRUD
- 좋아요, 좋아요 취소
- 인기 게시글 상단 노출
- 엘라스틱서치 엔진을 사용한 초성, 해시태그 검색 기능

📌 마이페이지
- 개인 프로필 CRUD
- 펫 프로필 CRUD
- 자신의 반려동물 프로필 이미지 등록시 AI로 강아지vs고양이 구분 (fastAPI사용, ec2 분리)
- 페이지네이션

📌 산책 매칭 페이지
- 카카오 지도 API 사용하여 게시글 등록시 위치 제공
- 매칭 게시판 CRUD (CKEditor 사용)
- 날짜, 지역, 성별, 시간대등 필터 설정으로 검색
- 실시간 채팅 기능 (Websocket & Django Channels)

📌 애견 월드컵
- 자신의 반려동물을 자랑하는 이벤트 페이지
- 이달의 인기 반려동물  (월별 초기화)
 
📌 Nginx / Gunicorn / Daphne
- Nginx : Proxy 역할
- Gunicorn : Django 배포용 WSGI서버 http protocol 요청 처리 (worker : 2)
- Daphne : Django 배포용 ASGI서버 WebSocket portocol 요청 처리


📌 피그마
-

- 회원가입/로그인
- ![img_5.png](/static/img_5.png) ![img_6.png](/static/img_6.png)


- 메인페이지 / 디테일 모달
![img_7.png](/static/img_7.png)
![img_8.png](/static/img_8.png)

- 애견월드컵 뽐뽐뽐
![img_9.png](/static/img_9.png)

- 산책매칭 / 디테일 모달
![img_10.png](/static/img_10.png)
![img_11.png](/static/img_11.png)

- 실시간 채팅 
![img_12.png](/static/img_12.png)

- 마이페이지 / 프로필 / 좋아요
![img_13.png](/static/img_13.png)
![img_14.png](/static/img_14.png)
![img_15.png](/static/img_15.png)
