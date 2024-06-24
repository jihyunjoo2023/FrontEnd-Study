# React Component란?

- 컴포넌트를 통해서 UI를 재사용 가능한 개별적인 여러 조각으로 나누고, 각 조각을 개별적으로 살펴볼 수 있음.
- "props" 라고 하는 임의의 입력을 받고 화면에 어떻게 표시되는지를 기술하는 React 엘리먼트 반환

## react component를 표현하는 2가지 방식

### 1. 함수형 컴포넌트

- props라는 입력을 받고 화면에 어떻게 표현되는지를 기술하는 react 엘리먼츠를 반환함(react)
- function App () {
  return <div>hello</div>
  }

### 2. 클래스형 컴포넌트

- class Welcome extends React.Component {
  render() {
  return <div>Hello, {this.props.name}</div>;
  }
  }

=> 두 가지 모두 기능은 동일하지만 함수형이 좀 더 간단하다!

## Component 보는 방법

- 컴포넌트 밖에서는 내가 필요한 파일을 import 하거나, 또는 export default라는 기능을 통해 내가 만든 컴포넌트를 밖으로 내보내는 코드가 있음.
- 컴포넌트 안에서는 자바스크립트를 쓸 수 있는 부분이 있음.
- return을 기준으로 아랫부분에서는 JSX를 작성할 수 있음.

### 주의

- 컴포넌트를 만들 때 반드시 가장 첫 글자는 대문자로 만들어야 합니다.
- 폴더는 소문자로 시작하는 카멜케이스로 작성하고, 컴포넌트를 만드는 파일은 대문자로 시작하는 카멜케이스로 이름을 지음

## 부모 - 자식 컴포넌트

- 컴포넌트는 다른 컴포넌트를 품을 수 있다.
- 품는 컴포넌트 = 부모 컴포넌트
- 품어지는 컴포넌트 = 자식 컴포넌트

- import React from "react";</br>
  function Child() {</br>
  return <div>나는 자식입니다.</div>;
  }</br>
  function App() {</br>
  return <Child />;
  }</br>
  export default App;

- 내보내진 것 = export default
- 화면에 보여지게 하다 = rendering
- 함수로 만들어진 컴포넌트를 html 태그 사용하듯이 코드를 작성하는 방식 = JSX
