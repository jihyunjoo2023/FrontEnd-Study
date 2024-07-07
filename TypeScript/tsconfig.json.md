# tsconfig.json

- tsc --init 명령을 실행하면 생성되는 파일
- typescript 프로젝트의 설정 파일이며, 주로 프로젝트의 컴파일 옵션 및 입력 파일들을 정의하는데 사용됨

## 주요 옵션

### compilerOption - target 옵션

- 해당 typescript 프로젝트 내 코드들이 어떤 javascript 버전으로 변환을 할 지 정하는 옵션
- es5로 설정하면 commonJS 버전으로 컴파일됨
- es2016(=es7)으로 설정하면 ES2016버전으로 컴파일 됨
  (최신 브라우저의 경우 보통 ES2016버전으로 컴파일됨)
- 실행환경 고려 필요
  - 레거시한 환경에서 동작 = es5
  - 그렇지 않은 경우 = es7

### compilerOption - module 옵션

- typescript 파일 컴파일 후 생성되는 js 모듈 형식 지정함
- 모듈을 가져오고 내보내는 방식을 결정하는 옵션
