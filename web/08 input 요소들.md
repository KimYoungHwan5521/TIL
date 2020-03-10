input 요소들

- 입력 서식 중요 공통 속성들
  - name 속성(반드시 필요)
    - 서버에 전달될 서식 값의 이름
  - required 속성
    - 서식 값이 반드시 입력되어야 함을 의미
    - 회원가입 시 회원 이름과 아이디 등과 같은 필수적인 서식 필드에 필요
    - 서식이 제출되기 직전 유효성 검사에서 처리
  - placeholder 속성
    - 입력 폼에 짧은 힌트를 보여줌
  - maxlength 속성
    - 서식 요소에 입력되는  값의 최대 길이 설정
    - maxlength 속성이 설정된 입력 폼은 maxlength 값 이상 입력이 안됨
  - autofocus 속성
    - 폼이 로딩되면 커서가 autofocus 속성이 있는 폼 요소로 이동
- fieldset 요소
  - 정의: 폼 요소들의 공통된 이름으로 그룹화 할 때 사용
  - 웹 브라우저에서 fieldset은 선으로 테두리가 표시되어 구분
  - 내부에 legend요소를 이용하여 fieldset 그룹에 이름 지정

- 텍스트와 패스워드 입력 서식

  - input type="text"
    - 일반적인 줄바꿈이 없는 텍스트 입력
    - type 지정하지 않으면 text 타입으로 인식
  - input type="password"
    - 패스워드 입력
    - 화면에 입력된 텍스트가 보이지 않음
  - input type="radio"
    - 나열된 여러 보기 중 하나만 선택하게 할 때 사용하는 폼 콘트롤러
    - checked 속성: 디폴트 선택값 지정 가능
  - input type"checkbox"
    - 여러 보기 중 복수 선택이 가능한 입력 타입

- 'input' 이외의 input 요소

  - select

    - 메뉴로 선택할 내용을 제시하고 하나를 선택하게함(드롭다운)
    - option
      - select의 자식요소로 선택 가능한 내용들을 지정
      - value: 메뉴가 선택 되었을 때 서버로 전달되는 내용
      - selected 속성으로 디폴트 값 지정 가능

    ```html
    <p><label>휴대전화</label>
    <select name="telCode">
        <option value="010">010</option>
        <option value="011">011</option>
        <option value="016">016</option>
        <option value="017">017</option>
        <option value="019">019</option>
        </select>
    <input type="tel" name="telNum" placeholder="1234-5678"></p>
    ```

  - textarea

    - 여러줄의 평범한 텍스트를 변집할 수 있는 폼 요소
    - textarea의 속성들
      - cols: 한 줄당 입력할 수 있는 글자수를 제한
      - rows:  textarea가 브라우저상에서 몇줄을 차지할지 결정
      - wrap
        - soft: 텍스트가 제줄될 때 줄바꿈이 되지 않음
        - hard: 텍스트가 제출될 때 줄바꿈이 되도록 줄바꿈 문자를 삽입함

  - button

    - 버튼을 만드는 요소
    - type 속성에 따른 button 요소
      - type="summit": 서식을 제출하는 단추를 만듦
      - type="reset": 서식을 초기화하는 단추를 만듦

  

