# B2B 어드민 웹페이지



<img width="447" alt="b2b관리자페이지노트북사진" src="https://user-images.githubusercontent.com/115059778/230389525-0e8434b5-df6e-484a-ac5e-e646a281455d.png">
<br/>

## 프로젝트 소개

- 개인 맞춤형 영양제 서비스를 제공하는 알고케어의 B2B사업인 ‘알고케어 앳 워크’ 서비스를 이용하는 **고객사의 담당자(고객사 임직원)에게 제공될 관리자페이지**입니다.


- 서비스 이용 현황 및 유저 관리, 재고 관리 등을 위해 이용하게 될 **관리자 서비스**를 제작한 프로젝트입니다. 

- 사용자가 필요한 핵심기능과 화면(로그인, 유저관리, 임직원들의 서비스이용 현황을 파악할 수 있는 대시보드, 챗봇 등)을 구현하여 고객사에서 **실제 사용할 수 있는 MVP**를 제작하였습니다.

- 해당 프로젝트 결과물은 현재 알고케어 사내 DEV계에 배포되어있습니다.

<br/>

### + 프로젝트 개발 방법론
- PM(Product Manager), PD(Product Designer) 2명, Backend 3명, Frontend 5명으로 팀이 이루어짐.
- 2주 단위의 스프린트 형태로 개발을 진행. 전사적인 방향성과 싱크를 맞춘 개발 백로그 및 타임라인에 맞추어 스프린트 플래닝을 통해 2주간 진행할 테스크를 선정하고 R&R을 배정.
- 매일 데일리 미팅을 통해 각자의 업무 현황을 공유/체크하고 협업이 필요한 지점을 논의하여 해결.
- 모든 코드는 PR(Pull Request)을 거쳐 코드리뷰를 진행해야만 Merge 되는 방식을 취하고 있음.

<br/>
<br/>

 


## 팀원 소개 및 역할 분담


|이름|손수민|최윤나|이지혜|
|:-------:|:----------:|:-----------:|:----------------:|
|역할 및 담당|프론트엔드|프론트엔드|프론트엔드|
|담당기능|로그인,대시보드|사용자관리,챗봇|대시보드|
|개인깃헙주소|[sonmansu](https://github.com/sonmansu)|[goodafteryoon](https://github.com/goodafteryoon)|[wisdom0122](https://github.com/wisdom0122)|

<br/>

## 개발 일정


**전체 개발 일정: 2023.01.30 ~ 2023.03.08**

1️⃣ 환경 구축 : 2023.01.30 ~ 2023.02.03<br/>
2️⃣ 로그인 개발 및 배포: 2023.02.06 ~ 2023.02.13<br/>
3️⃣ 사용자관리,대시보드 개발 및 배포: 2023.02.14 ~ 2023.03.03<br/>
4️⃣ 최종 배포: 2023.03.08

<br/>

## 주요 기능


### 🚪 로그인

- 로그인
- 로그아웃
- 관리자계정 유효성검사

### 📃 사용자관리

- 유저목록
- 사용자 검색필터
- 페이지네이션

### 📊 대시보드

- 브래드스크럼
- 캘린더
- 월 복용률 데이터 요약 표
- 임직원 월별 몸상태 랭킹 차트
- 요일별 몸상태 차트
- 몸상태 최근 6개월 추이 차트

<br/>
<br/>

## 개발환경(기술 스택)

- 프레임워크: React + hooks
- 언어: Typescript
- 에디터: Eslint + Prettier
- node: 16.13.0
- 상태관리: apollo-client
- 통신: graphql
- 스타일: emotion
- 디자인툴: Figma
- 소스관리: Github/algocare



<br/>
<br/>
<br/>




## 프로젝트 구조

```
 ├─ App.tsx
 ├─ assets
 │  ├─ icons
 │  └─ images
 ├─ common
 │  └─ utils
 │     ├─ apolloClient.ts
 │     ├─ apolloVariables.ts
 │     ├─ ChannelService.ts
 │     ├─ constants.ts
 │     ├─ functions.ts
 │     └─ types
 │        └─ index.ts
 ├─ components
 │  ├─ AuthGuard.tsx
 │  ├─ Breadcrumbs.tsx
 │  ├─ Button.tsx
 │  ├─ Dropdown.tsx
 │  ├─ GuestGuard.tsx
 │  ├─ Header.tsx
 │  ├─ index.ts
 │  ├─ LoadingScreen.tsx
 │  ├─ Modal.tsx
 │  └─ Navigation.tsx
 ├─ data
 │  └─ UserInfo.json
 ├─ graphql
 │  ├─ B2BBackend
 │  │  └─ query
 │  └─ GeneralBackend
 │     ├─ mutation
 │     └─ query
 ├─ index.tsx
 ├─ layouts
 │  └─ DefaultLayout.tsx
 ├─ pages
 │  ├─ BodyStatus
 │  │  ├─ components
 │  │  │  └─ index.ts
 │  │  └─ index.tsx
 │  ├─ Dashboard
 │  │  ├─ components
 │  │  │  └─ index.ts
 │  │  ├─ hooks
 │  │  │  └─ useSelectedDate.ts
 │  │  ├─ index.tsx
 │  │  └─ utils
 │  │     ├─ functions.t
 │  │     └─ types.ts
 │  ├─ Login
 │  │  ├─ index.tsx
 │  │  └─ styled.ts
 │  ├─ NotFound
 │  │  └─ index.tsx
 │  ├─ Router.tsx
 │  └─ UserList
 │     ├─ components
 │     │  ├─ Category.tsx
 │     │  ├─ Pagination.tsx
 │     │  ├─ Search.tsx
 │     │  ├─ SearchButton.tsx
 │     │  ├─ SearchIcon.tsx
 │     │  ├─ Tbody.tsx
 │     │  ├─ Thead.tsx
 │     │  ├─ User.tsx
 │     │  ├─ UserListHeader.tsx
 │     │  └─ UserListTable.tsx
 │     ├─ index.tsx
 │     ├─ styled.ts
 │     └─ utils
 │        └─ types.ts
 └─ styles
    ├─ colors.ts
    ├─ GlobalStyle.tsx
    └─ mixins.ts
```

## 팀 협업 방식

### 주 단위 스프린트 관리

- 1주 혹은 2주 단위의 스프린트로 일정을 관리했습니다.
- 매주 스프린트 첫 날에 스프린트 플래닝을 하여 목표를 설정하고 역할을 분배했습니다.
- 매일 데일리 미팅을 통해 각자 업무 현황을 점검했습니다.
- 스프린트가 끝나는 주의 마지막 날에는 스프린트 회고를 진행했습니다.
  - 상황에 따라 적절한 회고 방법론(KPT, PMI 등)을 선택하여 진행했습니다.
  - 회고를 통해 도출된 액션 아이템은 다음 스프린트 때 시도하여 업무 수행 프로세스를 지속적으로 개선했습니다.

<img src="https://user-images.githubusercontent.com/80534651/230407019-4a7387f9-6af6-4479-b3aa-74327ccbfe78.png" alt="주 단위 스프린트 관리" width="800px" />

### 협업 툴 적극 활용

> 알고케어의 PM, 백엔드, 프론트엔드, 디자이너 분들과 팀을 이뤄 협업하였으며 이 때 필요한 협업 툴을 적극적으로 활용하였습니다.

<table>
    <tr align="center">
        <th>노션</th>
        <th>피그마</th>
        <th>슬랙</th>
    </tr>
    <tr>
        <td>
            <img
                src="https://user-images.githubusercontent.com/80534651/230412120-987f4cdd-7ff9-4291-9f2f-15798251fc66.png"
                alt="작성된 기획 문서"
                width="300px"
            />
        </td>
        <td>
            <img
                src="https://user-images.githubusercontent.com/80534651/230414032-faf0c389-a53b-4657-81e8-80338e0ebd74.png"
                alt="디자인"
                width="300px"
            />
        </td>
        <td>
            <img
                src="https://user-images.githubusercontent.com/80534651/230414641-64f4443c-a0fc-4856-a9e4-8a532dc4579a.png"
                alt="사수 분께 라이브러리 사용에 관한 질문"
                width="300px"
            />
        </td>
    </tr>
    <tr align="center">
        <td>기획안 확인, 일정 관리</td>
        <td>UI 디자인</td>
        <td>사내 메신저</td>
    </tr>
</table>

### 컨벤션 설정

- 깃 브랜치 전략으로 Git-flow를 사용하였습니다.  
  <img
      src="https://user-images.githubusercontent.com/80534651/230416019-464caaa8-6eb2-4a84-a6a5-b2fabd92aee3.png"
      alt="개발기간 동안 생성한 브랜치들"
      width="200px"
  />  
  <관리되고 있는 브랜치들>

- 알고케어의 코드 컨벤션에 맞춰 일관성 있고 유지 보수가 용이한 코드를 작성하고자 하였습니다.

- 커밋 컨벤션을 정해 일관성 있고 가독성 있는 커밋 메시지를 작성하였습니다.  
  <img
      src="https://user-images.githubusercontent.com/80534651/230416622-a37764de-ceb1-4604-9429-dd536765a025.png"
      alt="커밋 메시지"
      width="500px"
  />

- Issue, Pull request는 템플릿에 맞춰 작성하여 팀원들이 작업한 사항에 대해 파악하기 쉽도록 했습니다.  
  <img
      src="https://user-images.githubusercontent.com/80534651/230417025-89101613-76ea-4c44-b5c5-ba651c75b5a5.png"
      alt="pr 예시"
      width="500px"
  />  
  <작성한 PR 예시>

### 코드 리뷰

- 모든 코드는 팀원들과 사내 사수 분의 코드 리뷰 과정을 거쳤습니다.
- 자유로운 의견 토론을 통해 코드를 개선하고 지식을 공유했습니다.

  <img
      src="https://user-images.githubusercontent.com/80534651/230417667-6a0ec0b7-261f-4d3d-9a04-c35f5812899c.png"
      alt="사수 분의 코드 리뷰"
      width="500px"
  />  
  <사수 분의 코드 리뷰>

  <img
      src="https://user-images.githubusercontent.com/80534651/230417995-21e60dbb-eccc-4d99-be92-c1a3c1146d0c.png"
      alt="팀원에게 질문"
      width="500px"
  />  
  <팀원에게 질문>

  <img
      src="https://user-images.githubusercontent.com/80534651/230418253-30d73a7a-3519-49fa-99c9-94a7e93c8be8.png"
      alt="의견 제안"
      width="400px"
  />  
  <의견 제안>

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
<br/>

#### 대시보드 내 몸상태페이지
![1](https://user-images.githubusercontent.com/115059778/230389719-d2152d65-af0d-4f1e-a22f-36ef32e20064.png)
![2](https://user-images.githubusercontent.com/115059778/230389738-373b6fb3-15d7-434e-bdde-006dfeff2397.png)
- 임직원 월별 몸상태 랭킹5 차트
- 몸상태 선택 select-box
- 요일별 몸상태 차트
- 몸상태 최근 6개월 추이 차트
