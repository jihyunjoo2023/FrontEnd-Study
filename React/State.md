# State

- state: 컴포넌트 내부에서 바뀔 수 있는 값.
- state를 만들 때는 useState()를 사용함

## useState 훅

- const로 선언 후 [] 빈 배열을 생성, 배열의 첫번째 자리에는 state의 이름, 두번째 자리에는 set을 붙이고 state의 이름을 붙여줌. 그리고 useState()의 인자에는 state의 원하는 처음값을 넣어줌!
- 처음 값: initial state

## State 변경

- state를 변경할 시 setValue(바꾸고 싶은 값)를 사용함
- 사용자가 input에 어떤 값을 입력하면, 그 값을 입력할때마다, 같은 말로 onChange 될 때마다 value라는 state에 setValue해서 넣어주는 것.
- 이러한 과정을 통해서 사용자의 input 값을 state로 관리하는 것.

## 불변성

- 불변성: 메모리에 있는 값을 변경할 수 없는 것.
- 자바스크립트의 데이터 형태 중에 원시 데이터는 불변성이 있고, 원시 데이터가 아닌 객체, 배열, 함수는 불변성이 없음!
