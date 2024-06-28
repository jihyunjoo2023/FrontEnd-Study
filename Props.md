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
