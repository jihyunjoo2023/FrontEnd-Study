# ES6 문법

## 상수와 변수

- 상수: const(constant: 변함없는 수)
- 변수: let

  상수의 경우 아래에 값을 재 지정하더라도 적용되지 않고 오류가 발생

- var을 사용하지 않는 이유: block level scope(중괄호) 바깥에서도 그 값이 나오면 문제가 생김
- var의 문제를 개선하기 위해서 const 와 let이 나옴!

## Object 선언

- 자바스크립트에서 말하는 object?  
  : key - value pair을 뜻함!
- value 형태에는 어떤 것도 다 올 수 있다
- 위에 값이 있다면 키의 value를 생략할 수도 있다!
- 얕은 복사 주의
- if! JSOn.parse(JSON.stringify()); 를 사용해서 JSON 아닌걸로 문자열로 쭈욱 풀어내서 다시 묶는다면 -> 새로운 주소값으로 변환됨! 결론적으로 value값이 바뀌더라도 이 안에 들어가는 키의 값은 바뀌지 않는다!

## Template Literals

- `` => 백틱
- 백틱 안에 변수로 사용이 가능하다!
- 백틱 안에서 플레이스 홀더에 ${} 이 중괄호 안에 변수명 넣어주기
- 멀티라인 사용 가능 </br>
  -> 기존의 경우 "" 안에 문자열을 넣고 +로 라인을 여러 개 두었으나 백틱 안에서는 멀티라인으로 한번에 입력이 가능하다.

## 배열/객체 비구조화

- 구조분해 할당이라고도 함
- 객체의 비구조화(구조분해 할당)
- 키 값이 맞아야 함</br>
  ex. </br>
  const person = {</br>
  name: "zoo",</br>
  age: "100",</br>
  };

const {name,age} = person;

- 배열의 비구조화(구조분해 할당)
- 위치가 맞아야 함</br>
  ex. </br>
  const testArr = {1,2,3,4,5}; </br>
  const {one, two, three, four, five} = testArr;

## 전개 연산자

- ...을 의미
- let{name, ... rest} = {"zoo", 100, "front"} 이런식이면 앞의 값을 제외하고 나머지 값인 100,"front"가 다 ...rest안에 들어간다는 소리
- let names = {"a","b"};에서 let al = {"c",..names};로 쓰면 "c","a","b" 이렇게 나열됨 그냥 names로 쓰면 나열안에 나열됨

## Arrow Fuctions

- 무조건 함수선언 시 function (){}; 구조 명심
- return 할 수식이 1줄이면 return문 생략이 가능. 하지만!!! 중괄호도 빼줘야 함
