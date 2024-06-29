# Props

## 컴포넌트끼리의 정보교환 방식

- 컴포넌트: 컴포넌트 간의 정보 교류 방법

1. props는 반드시 위에서 아래 방향으로 흐름. [부모] -> [자식] 방향으로만 흐른다.(단방향)
2. props는 반드신 읽기 전용으로 취급하며, 변경하지 않는다.

## props로 값 전달하기

### (1) 전달하기 - [주체: 부모]

- 컴포넌트 간의 정보를 교류할 때 props를 사용함.
- motherName 이라는 이름으로 name값을 Child 컴포넌트에게 전달해준 것임 -> 이 과정을 "props로 정보를 전달했다"라고 표현

### (2) 받기 - [주체: 자식]

function Child(props){</br>
console.log(props) </br>
// 이게 바로 props다.</br>
return </br>
연결 성공</br>
}

- mother가 보내준 정보가 객체 형태로 보여야 함
- props란 결국 부모 컴포넌트가 자식에게 넘겨준 데이터들의 묶음임

## props로 받은 값을 화면에 렌더링하기

- props는 object literal 형태이기 때문에 {props.motherName}로 꺼내서 사용할 수 있음. object literal의 key가 motherName인 이유는 우리가 child 로 보내줄 때 motherName={name}으로 보내주었기 때문!
- object literal란 {key: "value"} 데이터 형태를 의미함
- JSX에서도 {} 중괄호를 사용하면 자바스크립트 코드를 사용할 수 있음.

## prop deilling

- [부모] -> [자식] -> [그 자식] -> [그 자식의 자식]이 데이터를 받기 위해선 무려 3번이나 데이터를 내려줘야 함. </br>
  => prop drilling, props가 아래로 뚫고 내려가는 것.
- 이러한 문제를 해결하기 위해서는 'Redux'와 같은 데이터 상태관리 툴이 필요

## props children

- children props를 보내는 방법: <User> 안녕하세요 </User>
- 보통은 layout 컴포넌트를 짤 때 사용 많이 함
- header 컴포넌트를 Layout 컴포넌트에서 한번만 작성해도 여러페이지에서 모두 보여줌!

## 구조분해 할당과 props

- 원래 기존에서는 props를 사용하는 곳에서 props.를 전부 붙여줘야 함
- 자바스크립트의 구조분해 할당을 이용하면 더 짧게 쓰기 가능함!!!
- 만약 여러개의 props를 받는다면 {} 중괄호 안에 여러 개의 props를 그대로 써주면 됨!!!

## defaultProps

- defaultProps: 부모 컴포넌트에서 props를 보내주지 않아도 설정될 초기 값
- props를 받다보면 자주 받거나 무조건 받아야 하는 props가 발생함
- child 컴포넌트 입장에서는 부모 컴포넌트에서 값을 props 정보를 받기 전까지는 그 값이 없는 상태임. => 결과적으로 화면에 아무 값도 나오지 않음
- 그래서 부모 컴포넌트에서 props를 받기 전까지 child 컴포넌트에서 직접 임시로 사용 가능한 props를 설정할 수 있음
- 이후 부모 컴포넌트에서 값이 오게되면 설정한 defaultProps는 사라지고 내려받은 props로 값이 변경되는 구조
- Child.defaultProps={</br>
  name: '기본 이름'</br>
  }
- 이런 식으로 먼저 설정해두면 임시로 값을 채워둘 수 있음.
- 비슷하게 사용하는 것: 함수의 default argument 설정
