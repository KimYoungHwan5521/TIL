form, input, label

- form 요소

  - 정의: HTML의 서식을 정의하는 요소

    ```html
    <!-- 예: 고객 이름 입력 서식 -->
    <form>
        <p><label>고객이름:<input></label></p>
    </form>
    ```

  - form 요소 내부의 서식요소는 대부분 p요소 안에서 정의

  - form 요소의 속성: 서식의 내용을 어느 곳으로 어떤 방식으로 전송 할 것인지 속성 지정

    - action: 서식에서 전송단추를 눌럿을 때 내용이 전송되는 서버파일의 URL
    - method: 폼이 전송되는 방식을 결정
      - method="get"
        - action 속성의 URL 뒤에 붙어 URL 생성
        - 데이터의 이름과 값: '&'문자를 이용하여 연결
        - 웹 브라우저에서 직접 입력해서 접근 가능, 북마크도 가능
        - 전송 내용이 그대로 노출됨
      - method="post"
        - 클라이언트와 서버간 약속도니 형식으로 인코딩하여 서버로 전송
        - 전송내용은 가려지지만, 북마크나 직접접근 불가

- input 요소

  - 정의: 다양한 타입을 가지는 입력 데이터 필드
  - input 요소의 type속성: input 요소를 통해 받아들이는 데이터의 속성 정의로 type속성에 따라 input 요소 다르게 표현(예: text, password, hide, radio 등)
  - HTML5에서 input요소의 type 속성값: url, tel, email과 같은 구체적인 타입 추가

- label 요소

  - 정의: 서식 입력 요소의 캡션

  - label 요소의 사용

    - for 속성의 사용

      ```html
      <label for="name">이름: </label><input id="name" type="text">
      ```

    - label 요소 내부에 서식 요소 넣기

      ```html
      <label>이름: <input type="text"></label>
      <!-- label 요소 내부에 서식 요소를 넣을 때는 두 개 이상의 서식 요소를 넣지 않는다. -->
      ```

      