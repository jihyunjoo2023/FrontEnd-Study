# yarn과 npm

### 공통적인 특징

- 동일하게 자바스크립트 런타임 환경인 Node.js 의 패키지 관리자
- 애플의 앱스토어, 구글의 플레이리스트처럼 개발자들이 만든 패키지나 프로그램을 올려둔 온라인 데이터베이스를 쉽게 설치하고 삭제 가능

### 다른 특징

1. NPM

- node.js를 설치할 때 자동 생성
- Node Package Manager의 약자
- NPM platform 자체

2. Yarn

- 2016년에 페이스북에서 개발
- npm과의 호환성이 좋고, 속도나 안정성 측면에서는 npm보다 훨씬 나음

3. 요약

- 속도와 보안 모두 yarn이 좋음

## 명령어

### 1. npm

- dependencies 설치: npm install
- 패키지 설치: npm install [패키지명]
- dev 패키지 설치: npm install --save -dev [패키지명]
- 글로벌 패키지 설치: npm install --global [패키지명]
- 패키지 제거: npm uninstall [패키지명]
- dev 패키지 제거: npm unistall --save -dev [패키지명]
- 글로벌 패키지 제거: npm uninstall --global [패키지명]
- 업데이트: npm update
- 패키지 업데이트: upm update [패키지명]

### 2. yarn

- dependencies 설치: yarn
- 패키지 설치: yarn add [패키지명]
- dev 패키지 설치: yarn add -dev [패키지명]
- 글로벌 패키지 설치: yarn global add [패키지명]
- 패키지 제거: yarn remove [패키지명]
- dev 패키지 제거: yarn remove [패키지명]
- 글로벌 패키지 제거: yarn global remove [패키지명]
- 업데이트: yarn upgrade
- 패키지 업데이트: yarn upgrade [패키지명]
