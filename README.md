프로젝트 이름
1. 목표와 기능
1.1 목표 --> 변경하여 작성
유저 로그인/로그아웃
쇼핑몰 물품 조회/구매
쇼핑몰 물품 판매
유저 마이페이지
1.2 기능
[F.E] --> 변경하여 작성
프로젝트 완료 후 채워 넣기

[B.E] --> 변경하여 작성
프로젝트 완료 후 채워 넣기
1.3 팀 구성
[F.E]팀원 소개 --> 변경하여 작성
프로젝트 완료 후 채워 넣기
[B.E]팀원 소개 --> 변경하여 작성
프로젝트 완료 후 채워 넣기
2. 개발 환경 및 배포 URL --> 변경하여 작성
2.1 개발 환경 ※ 예시일뿐 개발에 사용한 프레임워크,API만 작성하면 됩니다.
[F.E]
--> 프로젝트 완료 후 변경하기

Web Framework
Django 3.x (Python 3.8)
서비스 배포 환경
Amazon Lightsail ...
[B.E]
--> 프로젝트 완료 후 변경하기

Web Framework
Django 3.x (Python 3.8)
서비스 배포 환경
Amazon Lightsail ...
2.2 배포 URL --> 변경하여 작성
배포할 URL 여기에 작성해주시면 됩니다.
테스트용 계정 ※ 판매자,구매자 둘다 작성해야합니다.
단, 중고 거래인 경우 하나만 작성해도 괜찮습니다.
id : test@test.test
pw : test11!!
2.3 [F.E] URL 구조 ※ 예시로 작성된 URL입니다.
main
App	URL	Views Function	HTML File Name	Note
main	'/'	home	main/home.html	홈화면
main	'/about/'	about	main/about.html	소개화면
accounts
App	URL	Views Function	HTML File Name	Note
accounts	'register/'	register	accounts/register.html	회원가입
accounts	'login/'	login	accounts/login.html	로그인
accounts	'logout/'	logout	accounts/logout.html	로그아웃
accounts	'profile/'	profile	accounts/profile.html	비밀번호변경기능 /
프로필 수정/ 닉네임추가
boardapp
App	URL	Views Function	HTML File Name	Note
board	'board/'	board	boardapp/post_list.html	게시판 목록
board	'board/int:pk/'	post_detail	boardapp/post_detail.html	게시글 상세보기
board	'board/write/'	post_write	boardapp/post_write.html	게시글 작성
board	'board/edit/int:pk/'	post_edit	boardapp/post_edit.html	게시글 수정
board	'board/delete/int:pk/'	post_delete	boardapp/post_delete.html	게시글 삭제
board	'board/int:pk/comment/'	comment_create	boardapp/comment_form.html	댓글 작성
board	'board/int:pk/comment/
int:comment_pk/edit/'	comment_edit	boardapp/comment_form.html	댓글 수정
board	'board/int:pk/comment/
int:comment_pk/delete/'	comment_delete	boardapp/comment_
confirm_delete.html	댓글 삭제
blog
App	URL	Views Function	HTML File Name	Note
blog	'blog/'	blog	blog/blog.html	갤러리형 게시판 메인 화면
blog	'blog/int:pk/'	post	blog/post.html	상세 포스트 화면
blog	'blog/write/'	write	blog/write.html	카테고리 지정, 사진업로드,
게시글 조회수 반영
blog	'blog/edit/int:pk/'	edit	blog/edit.html	게시물목록보기
blog	'blog/delete/int:pk/'	delete	blog/delete.html	삭제 화면
blog	'blog/search/'	search	blog/search.html	주제와 카테고리에 따라 검색,
시간순에 따라 정렬
blog	'post/int:post_pk/comment/'	comment_new	blog/comment_form.html	댓글 입력 폼
blog	'post/int:post_pk/comment/
int:parent_pk/'	reply_new	blog/comment_form.html	대댓글 폼
blog	'post/int:pk/like/'	like_post	blog/post.html	좋아요를 누르면 blog/post로 Redirect됨
blog	'comment/int:pk/update/'	comment_update	blog/comment_form.html	댓글 업데이터 경로
blog	'comment/int:pk/delete/'	comment_delete	blog/comment_
confirm_delete.html	댓글 삭제 폼
2.4 [B.E] URL 구조 --> 변경하여 작성
App	Method	URL	Views Class	Note	Authentication
blog	GET	'/blog/posts/'	PostViewSet	게시글 목록	
blog	POST	'/blog/posts/'	PostViewSet	게시글 생성 / ChatGPT API 요청	✅
blog	GET	'/blog/posts/{post_id}/'	PostViewSet	게시글 상세보기 / 게시글 조회수 증가	
blog	PATCH	'/blog/posts/{post_id}/'	PostViewSet	게시글 수정	
blog	DELETE	'/blog/posts/{post_id}/'	PostViewSet	게시글 삭제	
blog	POST	'/blog/posts/{post_id}/like/'	PostViewSet	게시글 좋아요 증가	
blog	GET	'/blog/posts/{post_id}/comments/'	CommentViewSet	게시물의 댓글 목록	
blog	POST	'/blog/posts/{post_id}/comments/'	CommentViewSet	게시물의 댓글 생성	
blog	GET	'/blog/posts/{post_id}/comments/{comment_id}/'	CommentViewSet	게시물의 특정 댓글 보기	
blog	PATCH	'/blog/posts/{post_id}/comments/{comment_id}/'	CommentViewSet	게시물의 특정 댓글 수정	
blog	DELETE	'/blog/posts/{post_id}/comments/{comment_id}/'	CommentViewSet	게시물의 특정 댓글 삭제	
3. 요구사항 명세와 기능 명세 --> 변경하여 작성
https://www.mindmeister.com/ 등을 사용하여 모델링 및 요구사항 명세를 시각화하면 좋습니다.
이미지는 셈플 이미지입니다.


머메이드를 이용해 시각화 할 수 있습니다.
4. 개발 일정 --> 변경하여 작성
데일리 스크럼 시간 : 매일 오후 2시
4.1 개발 일정(WBS) --> 변경하여 작성


좀 더 가벼운 프로젝트는 아래 일정표를 사용하세요.
아래 일정표는 habitmaker.co.kr 에서 작성되었습니다.
관련된 스택 표시는 dev.habitmaker.co.kr 에서 작성되었습니다.
5. 와이어프레임 / UI / BM --> 변경하여 작성
5.1 와이어프레임
아래 페이지별 상세 설명, 더 큰 이미지로 하나하나씩 설명 필요


와이어 프레임은 디자인을 할 수 있다면 '피그마'를, 디자인을 할 수 없다면 '카카오 오븐'으로 쉽게 만들 수 있습니다.
5.2 화면 설계 ※ 화면은 gif,jpg 파일로 업로드해주세요.
표는 가로/세로 상관이 없습니다.
메인	로그인
	
회원가입	정보수정
	
검색	번역
	
선택삭제	글쓰기
	
글 상세보기	댓글
	
6. 데이터베이스 모델링(ERD) 및 변수명 --> 변경하여 작성
프론트와 백엔드 간에 정보를 주고 받는 과정에서 혼선이 일어나지 않도록 변수명을 설정이 필요합니다.

프론트에서 submit과정을 진행할 때 어떤 변수명으로 보내는지 알아야 데이터 맞추기가 수월합니다.

아래 ERD는 ERDCloud를 사용했습니다.



https://dbdiagram.io/home도 많이 사용합니다.
7. Architecture --> 변경하여 작성
아래 Architecture 설계도는 PPT를 사용했습니다.
image

PPT로 간단하게 작성하였으나, 아키텍쳐가 커지거나, 상세한 내용이 필요할 경우 AWS architecture Tool을 사용하기도 합니다.
8. 메인 기능 --> 변경하여 작성
머메이드나 이미지 파일을 사용하면 좋을 것 같습니다.
요구사항 및 기능 명세에서 제외한 기능을 작성하면 좋을 것 같습니다.
예를 들어, 이미지 저장을 위해 Amazon S3를 사용했다. OAuth 기능 구현을 위해 카카오로그인 API를 사용했다. 등등
요구사항 및 기능 명세에서 간단하게 설명만 하였다면 구현한 API를 자세하게 설명해도 괜찮습니다.
