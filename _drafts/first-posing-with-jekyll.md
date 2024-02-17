---
layout: post
title:  "2024 상반기 디케이테크인 경력직 공개 채용 코딩 과제 제출"
date:   2024-02-17 15:29:38 +0900
categories: jekyll first
tag: hello,world

---

## 2024 상반기 디케이테크인 경력직 공개 채용 코딩 과제 제출

- 제출자: 김새나
- 제출일: 2023.02.09
- 지원직무: [Frontend] 카카오 그룹사 서비스 개발자

### 개발 환경
### server
- node: v12.22.12 (npm: 6.14.16)

### client
- vue: v3.2.13
- node: v18.18.0 (npm: 8.19.4)

#### 추가 라이브러리

- axios: api 요청을 위해 추가. 비동기적으로 데이터를 가져옵니다.
- lodash:  JavaScript 유틸리티 라이브러리. 해당 프로젝트에서는 검색시 debounce 구현을 위해서 추가하였습니다.
- vue-router vue 페이지 이동 라이브러리. 해당 프로젝트에서는 정의되지 않은 주소 호출시, 404 에러 페이지 라우팅을 위해서 사용하였습니다. 

#### local 실행 방법

1. .env 파일 설정

```
VUE_APP_PORT = 4000
VUE_APP_MOCK_SERVER = "http://localhost:3001"
```

2. 설치 및 실행

```
cd client
npm install
npm run serve
```

### 소스 구조
client는 아래의 주요 소스 구조는 아래와 같습니다. 
```
├── client          
|   ├── public
|   ├── src   // 소스 코드 전체
|   |   ├── api // API 호출 코드
|   |   ├── assets // css, font, image 등의 정적 파일
|   |   ├── components // 재사용 및 일반 컴포넌트
|   |   ├── pages // 페이지 컴포넌트
|   |   ├── main.js // 어플리케이션 진입점
|   |   ├── router.js // 어플리케이션 라우터 구성
|   |   └── App.vue // root 컴포넌트
|   ├── packgage.json
|   └── README.md
├── result
├── server       
└── README.md     
```

### 과제 요구 사항

#### 요구 사항 > 일반

- [x] `/client` 디렉토리 내에서 작업 했습니다.
- [x] `Vue` 로 개발 했습니다.
- [x] .env 환경 변수를 사용해 실행 포트를 `4000` 으로 설정하였습니다. 
- [x] `/markup` 디렉토리의 `index.html`, `style.css` 의 태그 구조 및 class이름을 최대한 활용하여 구현하였습니다.

#### 요구 사항 > 기능

- [x] 영역 별로 Header, Footer, Search, JobCard 컴포넌트로 구분하였습니다. 
- [x] 제공된 API (`GET /rest/v1/jobs`) 를 통해 불러온 데이터를 최신순으로 정렬해 표시합니다.
- [x] 오늘 날짜 기준으로 등록일(createdAt)이 2일내 라면 new 데이터로 표시합니다.
  - [x] 당일일 경우 'Today'
  - [x] 2일 내 데이터는 '${diff} days ago'
  - [x] 그 외는 'YYYY.MM.DD' 포맷으로 출력합니다.
- [x] 주어진 검색 인풋 박스에 대해 입력된 문자로 실시간 검색하는 기능을 구현합니다.
  - api 재호출 없이 기존 목록에서 필터링 합니다.
  - 제목, 고용형태, 직무, 위치, 키워드가 검색됩니다. 
  - 단, 날짜는 검색되지 않습니다. 
  - debounce를 사용하여 200ms 내에 한번만 검색이 호출되도록 구현하였습니다.    
- [x] 실행 중 일어날 수 있는 오류에 대한 예외 처리를 해주셔야 합니다.
  - /src/api/util 함수에서 api 호출에 대한 일반적인 오류 처리를 수행합니다.
  - error.vue를 이용하여 정의되지 않은 주소 호출시 오류 페이지로 호출되로록 수정하였습니다.
- [x] 코드 작성 시, `ECMAScript6+` 스펙을 적극적으로 활용하는 것을 권장합니다.
  - import, export
  - const, let
  - arrow function
  - async, await
  - 구조 분해 할당
  - 등 es6 문법을 활용하였습니다.
