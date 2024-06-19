## ES6 문법

### 상수와 변수

- 상수: const(constant: 변함없는 수)
- 변수: let

  상수의 경우 아래에 값을 재 지정하더라도 적용되지 않고 오류가 발생

- var을 사용하지 않는 이유: block level scope(중괄호) 바깥에서도 그 값이 나오면 문제가 생김
- var의 문제를 개선하기 위해서 const 와 let이 나옴!

### Object 선언

- 자바스크립트에서 말하는 object?  
  : key - value pair을 뜻함!
- value 형태에는 어떤 것도 다 올 수 있다
- 위에 값이 있다면 키의 value를 생략할 수도 있다!
- 얕은 복사 주의
- if! JSOn.parse(JSON.stringify()); 를 사용해서 JSON 아닌걸로 문자열로 쭈욱 풀어내서 다시 묶는다면 -> 새로운 주소값으로 변환됨! 결론적으로 value값이 바뀌더라도 이 안에 들어가는 키의 값은 바뀌지 않는다!
