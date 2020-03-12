JavaScript 데이터 타입과 변수

데이터 타입

```javascript
var x = 32;
// x: 변수
// 32: 리터럴
```

- 숫자

  - 자바스크립트에서는 정수와 실수 구분하지 않음

- 문자열

  - 자바스크립트는 char 타입이 없음
  - 참고: 이스케이프 시퀀스

- Boolean

  - True, False

- 단순 데이터 타입

  - null
  - undefine
    - 생성되지 않은 객체에 접근할 때

- 객체 데이터 타입

  - 다양한 값의 집합

  - {}로 쌓여있음

    ```javascript
    var square = {width:20, height:30, position:{x:200,y:400}};
    ```

  - 생성자 new를 통해 property를 쉽게 추가 가능

- 배열

  - 배열의 생성

    ```javascript
    var a = new Array();
    var b = {10, True, "orange"};
    ```

- 함수

  - function 함수이름(전달인자){}
  - 함수리터럴: 함수를 값으로 변수에 할당(return값이 할당됨)

변수

- 변수타입
  - 타입 설정하지 않아도 됌
  - 변수 타입에 자유로움(파이썬같이)
- 변수 선언: var