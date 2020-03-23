### JavaScript library

- 기능

  1. JavaScript 프로그래밍을 쉽고 빠르게 작성

  2. 프레임워크로서의 기능

  3. 종류

     - Prototype.js

     - YUI
       - Yahoo에서 배포하는 JavaScript library
     - Dojo
     - jQuery
       - 웹페이지 개발 시 코드 작성 방법 변경: 객체의 속성을 조작하여 쉽게 웹기능 구현
       - Plug-in 방식으로 기능 추가
       - jQuery 활용 영역 확장
         - jQuery UI
         - jQuery mobile
       - 다양한 셀렉터 지원: 복잡한 과정 한 줄로 처리 가능

  4. 특화된 기능을 제공하는 JavaScript library

     - video.js
     - soundManager2
     - paper.js
     - Raphael
     - D3
     - Box2DJS
     - Collie

##### jQuery

- jQuery의 특징
  - 메소드 체이닝

    - 하나의 DOM 객체에 여러가지 메소드를 체인처럼 연결하여 순서대로 메소드에 적용

      ```javascript
      $('selector').methodA().methodB().methodC();
      ```

  - Ajax

    ```javascript
    // javascript 코드
    function submitUsername(){...}
    function displayStatus(req){
        if(req.readyStatus==4&&req.statue==200){...}
    }
    fundtion getXMLHttpRequest(){...}
    
    // jQuery
    function submitUsername(){
        $("#status").load("StatusVerifier?username=") + escape($("#username").val());
    }
    ```

- jQuery의 선택자

  - $()와 jQuery()
    - CSS3 선택자 넣어 원하는 요소 선택 가능
    - id, class 선택 가능
    - 상대적인 위치로 요소 선택 가능
  - $()의 문제: prototype이 $()문법 사용 -> jQuery를 prototype과 함께 사용시 에러 발생
  - CSS3 선택자를 이용한 요소 선택
    - :nth-child는 1부터 시작/ jQuery 등의 프로그래밍시 0부터 시작
    - :eq(n)
      - 정확히 일치하는 요소 선택
    - :gt(n)
      - +1번째 이후의 모든 요소
    - :lt(n)
      - n+1 번째 이전의 모든 요소를 선택
    - 두 개 이상의 선택자 필요시 선택자들을 쉼표(,)로 연결
    - add 메소드 사용하여 선택 추가

- jQuery 속성의 조작

  - attr()

    - 선택된 요소의 속성을 읽어옴

    - 선택된 요소의 속성을 설정

      ```html
      <div id="id" class="class">
          <img id="id2" class="class2" title="cafe" src="images/cafe.png" alt="cafe illustrate">
      </div>
      ```

      ```javascript
      var imgTitle = $("#cafe").attr("title");
      $("#console").html(imgTitle);
      ```

    - getAttribut()와 동일한 결과

    - removeAttr(): 속성 제거

  - addClass(): 요소들의 클래스 속성 적용

  - removeClass(): 요소들의 특정 클래스 속성 삭제

  - CSS 스타일 설정

    ```javascript
    $(".pic_frame").css("border","3px solid yellowgreen");
    // class 값이 pic_frame인 요소 보더에 설정
    css('name','value');
    // 선택 요소에 특정 스타일 동적으로 적용
    ```

    - css() 에 전달인자 하나: 설정된 스타일을 읽어옴

  - html()

    - 특정 요소의 HTML 코드 읽거나 대치

      ```javascript
      $("p:first").html();
      $("#console").html($("p:first").html())
      // 첫 번째 단락의 HTML 코드를 읽어옴(텍스트 뿐만 아니라 HTML 코드를 읽어옴)
      $("p:first").html("이것은 <b>변경된</b> 문장입니다.");
      // 전달인자 사용하여 기존 HTML 대치
      ```

  - text()

    - 텍스트 콘텐츠 읽거나 대치
    - html과 달리 코드는 읽지 않고 텍스트만

  - append(), appendTo()

    - 기존 코드 뒤에 추가

  - bind()

    - jQuery의 이벤트 적용 메소트

      ```javascript
      .bind(eventType,eventData,handler(eventObject))
      /*
      첫 번째 전달인자: 이벤트 타입(예: click, mouseover)
      두 번째 전달인자: 핸들러 함수에서 사용할 data 프로퍼티 값(대부분 생략)
      세 번째 전달인자: 이벤트 발생 시 호출 함수
      */
      ```

  - unbind()

    - 이벤트 핸들러 제거
    - 인자 없으면 요소에 적용된 모든 핸들러 제거
    - 단 한 번 사용되고 unbind 될 이벤트의 경우 <b>one()</b> 메소드 사용



