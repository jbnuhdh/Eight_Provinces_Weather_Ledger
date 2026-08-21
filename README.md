# 팔도 날씨수첩 — 실행 안내

## 1. 게임 실행

아래 주소에 접속하면 별도 설치 없이 웹 브라우저에서 바로 실행할 수 있습니다.

- 배포 URL: https://jbnuhdh.github.io/Eight_Provinces_Weather_Ledger/
- 권장 브라우저: Chrome, Edge 등 최신 웹 브라우저


## 2. 주요 파일 및 폴더 구성

- `index.dc.html` — 메인 실행 파일
- `gyeongsang.dc.html` — 경상도 지역 콘텐츠
- `hwanghae.dc.html` — 황해도 지역 콘텐츠
- `hamgyeong_jeolla.dc.html` — 함경도·전라도 지역 콘텐츠
- `gyeonggi_chungcheong_jeju_pyeongan.dc.html` — 경기·충청·제주·평안 지역 콘텐츠
- `support.js` — 게임 실행에 필요한 런타임 스크립트
- `assets/` — 게임 이미지 및 리소스
- `data/` — 기상 관측자료(CSV)

※ 파일명과 폴더명을 변경하면 게임에서 이미지 또는 자료를 정상적으로 불러오지 못할 수 있습니다.

## 3. 외부 리소스 출처 및 라이선스

### 3.1 Galmuri 폰트

- 용도: 게임 화면의 한글 픽셀 폰트
- 출처: Galmuri by quiple
- 프로젝트: https://github.com/quiple/galmuri
- CDN: https://cdn.jsdelivr.net/npm/galmuri/dist/galmuri.css
- 라이선스: SIL Open Font License 1.1 (OFL-1.1)

### 3.2 React / ReactDOM 18.3.1

- 용도: 게임 UI 구성 및 브라우저 렌더링
- 출처: React, Meta Open Source
- 프로젝트: https://github.com/facebook/react
- CDN:
  - https://unpkg.com/react@18.3.1/umd/react.production.min.js
  - https://unpkg.com/react-dom@18.3.1/umd/react-dom.production.min.js
- 라이선스: MIT License

### 3.3 @babel/standalone 7.29.0

- 용도: JSX 및 JavaScript 코드의 브라우저 실행 변환
- 출처: Babel Project
- 프로젝트: https://github.com/babel/babel
- CDN: https://unpkg.com/@babel/standalone@7.29.0/babel.min.js
- 라이선스: MIT License

### 3.4 기상청 관측자료

- 사용 자료: 기상청 종관기상관측(ASOS), 방재기상관측(AWS) 등 실제 관측자료
- 출처: 기상청 기상자료개방포털
- URL: https://data.kma.go.kr/
- 이용조건: 기상청 저작권 보호 및 정책과 해당 자료에 표시된 공공누리(KOGL) 유형을 따름
- 저작권 정책: https://data.kma.go.kr/cmmn/static/staticPage.do?page=pageCr
- 출처 표기: 게임 내 관련 화면과 본 README에 기상청 관측자료임을 명시함

### 3.5 게임 이미지 리소스

- 대상: `assets/` 폴더의 캐릭터, 배경, 오브젝트 등 게임 이미지
- 제작 방식: OpenAI GPT(ChatGPT)를 활용하여 팀에서 직접 기획·생성·수정한 팀 자체 제작 이미지
- 출처: 팀 자체 제작(OpenAI GPT 활용)
- 이용범위: 본 프로젝트 및 대회 제출물 내 사용

### 3.6 support.js

- 용도: `.dc.html` 파일 실행을 지원하는 런타임 스크립트
- 출처: 파일 헤더에 명시된 `dc-runtime/src/*.ts`로부터 생성된 런타임 번들
- 제공 방식: 외부 CDN에서 불러오지 않고 제출 소스코드에 포함
- 비고: 본 프로젝트 실행을 위해 생성·포함된 소스 구성요소이며, 파일 내 별도 외부 라이선스 표기는 확인되지 않음

### 3.7 기타 관측자료 표기

일부 콘텐츠에는 북한 지역 등 관측 사례의 검증 및 재현을 위해 NOAA ISD, GHCN-Daily 및 WMO GTS 계열 관측자료가 언급·활용되어 있습니다.

- NOAA Integrated Surface Database (ISD): https://www.ncei.noaa.gov/products/land-based-station/integrated-surface-database
- NOAA Global Historical Climatology Network Daily (GHCN-Daily): https://www.ncei.noaa.gov/products/land-based-station/global-historical-climatology-network-daily
- WMO Global Telecommunication System (GTS): https://community.wmo.int/site/knowledge-hub/programmes-and-initiatives/wmo-information-system-wis
- 이용조건: 각 데이터 제공기관 및 원자료의 데이터 정책·이용조건을 따름

## 4. 저장 데이터

진행 상황(도장·코인·펫·캐릭터)은 사용 중인 웹 브라우저에 저장됩니다.
같은 브라우저에서는 이어서 진행할 수 있으며, 다른 컴퓨터 또는 다른 브라우저에서는 기존 진행 상황이 자동으로 이전되지 않습니다.

## 5. 보안 관련 안내

- 본 제출물에는 API 키, 비밀번호, 인증 토큰 등 비밀값을 포함하지 않습니다.
- 외부 라이브러리는 공개 CDN을 통해 불러오며 별도의 인증키를 사용하지 않습니다.
