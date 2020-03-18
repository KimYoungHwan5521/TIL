### JavaScript 상속

##### class 상속

```javascript
// superclass
function Character(name,title,level){...}
Character.orcs = function(){
    var newOrc = new Character('orc', '일꾼');
    newOrc.arms = ['도끼']
    return newOrc
}
```



- prototype 지정으로 상속

  ```javascript
  Orc.prototype = new Character("orc","일꾼");
  ```

  - 문제점: 일꾼 캐릭터의 이름과 타이틀을 객체마다 다르게 줄수 없음

- superclass의 생성자 이용

  ```javascript
  function Orc(name,title,level){
      Character.apply(this,arguments);
      this.arms['도끼']
  }
  ```

  - 문제점: superclass의 프로토타입을 상속받지 못함

- prototype 지정과 superclass의 생성자 사용으로 단점 보완 가능

  - 문제점: superclass의 생성자 함수에 정의된 프로퍼티와 메소드가 프로토타입 지정 시 , 한번 더 생성

- subclass의 프로토타입을 superclass의 프로토타입으로 지정

  ```javascript
  function Orc(name, title,level){
      Character.apply(this, arguments);
      this.arms = ['도끼'];
  }
  Orc.prototype = Character.prototype
  ```

  - 문제점: subclass의 프로토타입과 superclass의 프로토타입 참조로 연결 -> subclass의 프로토타입 변경시, sueprclass의 프로토타입도 변경됨

- subclass의 프로토타입 공유 방지: 객체를 복사하여 할당

  1. 빈 생성자 함수 작성
  2. 빈 생성자 함수에 프로퍼티 복사하고자 하는 객체에 할당
  3. 변수에 new 연산자와 생성자를 사용하여 새로운 객체 생성

  ```javascript
  function copyObject(obj){
      var TempFunc = function(){};
      TempFunc.prototype = originalObj;
      var duplicatedObj = new TempFunc();    
  }
  ```

- cunstructor 프로퍼티 설정

  - cunstructor: 객체의 생성자
  - constructor 프로퍼티: 생성자 함수로 객체 생성시 생성자 함수의 프로토타입에 생성
  - 프로토타입의 cunstructor의 프로퍼티는 superclass의 것으로 변화

##### mixIn 함수

- 다수의 부모 객체를 순환하여 모든 프로퍼티나 메소드를 빌려와 하나의 객체로 만들어 반환

- 객체의 프로퍼티 빌려오는 함수

  ```javascript
  function mixInProperty(obj){
      var arg, prop;
      for(arg=1;arg<arguments.length;arg++){
          for(prop in arguments[arg]){
              if(arguments[arg].hasOwnProperty(prop)){
                  obj[prop] = arguments[arg][prop];
              }
          }
      }
  }
  ```

  - 첫번째 전달인자: 프로퍼티가 가져와 저장되는 객체
  - 두번째~ 전달인자: 프로퍼티를 가져올 객체

  ```javascript
  var firstObj = {a:"I", b:"II"};
  var secondObj = {c:"III", d:"IV"};
  var childObj = {e:"V"};
  
  mixInProperty(childObj,firstObj,secondObj);
  ```

- Class에서 프로토타입 메소드 빌려오는 함수

  ```javascript
  function mixInProperty(cls){
      var arg, method;
      for(arg=0;arg<arguments.length;arg++){
          for(method in arguments[arg].prototype){
              if(arguments[arg].prototype[method] != "function"){
                  cls.prototype[method] = arguments[arg].prototype[method];
              }
          }
      }
  }
  ```

- 전달인자와 프로퍼티 이름에 주의

  - 겹치는 프로퍼티가 없어야함

