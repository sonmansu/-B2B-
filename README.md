# B2B 어드민 웹페이지

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

- 노션으로 작성된 기획 문서를 확인하고 일정을 관리 하였습니다.  
  <img
              src="https://user-images.githubusercontent.com/80534651/230412120-987f4cdd-7ff9-4291-9f2f-15798251fc66.png"
              alt="작성된 기획 문서"
              width="300px"
          />

- UI 디자인은 디자이너분께서 피그마를 통해 전달해주셨습니다.  
  <img
              src="https://user-images.githubusercontent.com/80534651/230414032-faf0c389-a53b-4657-81e8-80338e0ebd74.png"
              alt="디자인"
              width="300px"
          />

- 메신저로 슬랙을 사용하였습니다.  
  <img
              src="https://user-images.githubusercontent.com/80534651/230414641-64f4443c-a0fc-4856-a9e4-8a532dc4579a.png"
              alt="사수 분께 라이브러리 사용에 관한 질문"
              width="300px"
          />

  <사수 분께 라이브러리 사용에 관해 질문>

  <img
      src="https://user-images.githubusercontent.com/80534651/230415524-ea14873c-dbe7-410e-a054-eff899ac1f7c.png"
      alt="백엔드 개발자 분께 API 관한 질문"
      width="300px"
  />  
  <백엔드 개발자 분께 API 관해 질문>

</p>

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
