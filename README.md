# 프로젝트 명

- 포트폴리오 메인 사이트

## 프로젝트 개요

- Server단(port2023-mainsite-server)과 Client단(port2023-portmainsite)으로 사이트 구성
- eslint, prettier를 이용하여 버그를 분석하여 해결하고 질 좋은 코드를 작성
- node.js 형식으로 cafe24 호스팅 배포

## 기술 스택

### Server

- express는 Node.js 기반의 웹 프레임워크로, 웹 애플리케이션 및 API를 개발하기 위해 사용됩니다.
- nodemon은 파일의 변경을 감지하여 자동으로 애플리케이션을 다시 시작해주는 패키지입니다.

### Client

- HTML, CSS 기반으로 웹사이트의 기본 레이아웃 설계하고, 웹 표준 및 웹 접근성을 준수하여 작업합니다.
- react를 사용하여 사이트를 번들링하고 관리합니다.
- gsap를 이용하여 패럴랙스 효과를 줍니다.
- lenis를 이용하여 smooth 효과를 구현합니다.
- cafe24를 통해 사이트를 배포합니다.
- git을 사용하여 파일을 관리합니다.

### eslint-config-prettier

- eslint, prettier를 설치하여 코드분석의 편의성을 높입니다.
- eslint-config-prettier를 설치하여 rule이 겹치는 충돌을 막습니다.

## 프로젝트 실행

### Server

- 디렉토리 생성과 이동을 합니다.
  `$ mkdir Server타이틀 && cd Server타이틀`
- node_modules 디렉토리를 Git으로 관리하지 않기 위해 node_modeles 디렉토리를 설정합니다.
  `$ echo node_modules > .gitignore`
- 프로젝트(Server)를 기본값으로 설정합니다.
  `$ npm init -y`
- serve를 설치합니다.
  `npm install -g serve`
- express, nodemon를 설치합니다.
  `$ npm install express nodemon`

### Client

- react를 설치합니다. `npx create-react-app 타이틀`
- react-router-dom, sass, gsap, lenis를 설치합니다.
  `npm install react-router-dom sass gsap @studio-freight/lenis`

### prettier, eslint

- pretteier를 설치합니다.
  `npm install prettier --save-dev`
- eslint를 설치합니다.
  `npm install eslint --save-dev`
- eslint-config-prettier를 설치합니다.
  `npm install eslint-config-prettier --save-dev`
- node_modules > eslint-plugin-jsx-ally > .eslintrc에 코드를 추가합니다.
  `{
  "plugins": [
  "jsx-ally"
],
"rules": {
  "jsx-a11y/rule-name": 2,
  "react/prop-types": "off",
  "no-var": "error",
  "no-multiple-empty-lines": "error",
  "no-console": "off",
  "eqeqeq": "error",
  "dot-notation": "error",
  "no-unused-vars": "error"
},
"extends": [
  "react-app",
  "eslint:recommended",
  "prettier",
  "airbnb-base",
  "plugin:jsx-a11y/recommended"
]
}`

- Client 디렉토리 > .eslintrc.cjs에 .eslintr 에 있는 rules를 추가합니다.
