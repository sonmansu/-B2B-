## 구현 기능

### 사용자 관리 페이지
![image](https://user-images.githubusercontent.com/106373580/230430100-5b9bf99c-2306-476b-a53c-6c864ef4bfc1.png)
#### 유저 테이블 및 페이지네이션 기능
- 이름 / 이메일 / 전화번호 / 가입일 / 등록 그룹에 따른 테이블 구성
- 1page 당 10명의 유저 데이터 받아오도록 구현
- 5 단위마다 페이지 넘버 보여지고 다음 페이지 존재 유무에 따라 dot(…) 처리
- 다음(>), 이전(<), 맨처음(<<), 맨뒤(>>), 해당 페이지의 숫자 (1,2,3 ~)에 따른 버튼 구현

![image](https://user-images.githubusercontent.com/106373580/230440928-37c02ba8-786c-4586-99ee-6593c73f0647.png)
#### 검색 기능
- 이름/이메일/전화번호 옵션별 유저 조회 가능

![image](https://user-images.githubusercontent.com/106373580/230441026-11a0b39f-bb7b-4a9b-b8d8-5c3ee2c8de04.png)
#### 챗봇 기능
- url 파라미터에 따라(로그인 전/후) 다른 내용의 챗봇 연결
