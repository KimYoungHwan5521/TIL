CSS 네비게이션

- CSS 인터렉티브 이미지버튼

  - 버튼 이미지 제작
    - 일반, 마우스가 올라갔을때, 클릭 되었을 때를 하나의 파일로 작성

  ```css
  a.button{
      display: block;
      width: 160px;
      height: 19px;
      background-image: url(images/button.png);
      background-position: 0 0;
  }
  a.button:hover{
      background-position: 0 -35px;
  }
  a.button:active{
      background-bosition: 0 -70px;
  }
  ```

- 텍스트 네비게이션

  - HTML로 텍스트 네비게이션 구조 작성

    - nav 요소 안에서 작성

    - 목록형태: 링크의 목록으로 작성

      ```html
      <nav>
      	<ol>
              <li><a href="url1">탭1</a></li>
              <li><a href="url2">탭2</a></li>
              <li><a href="url3">탭3</a></li>
              <li><a href="url4">탭4</a></li>
          </ol>
      </nav>
      ```

  - CSS로 텍스트 네비게이션 스타일 적용하기

    ```css
    nav li{
        display: inline;
    }
    /* 
    display: inline 효과
    1. 목록마다 줄바꿈 없이 한 줄로 보여짐
    2. 목록의 블릿이 사라짐
    */
    ```

    1. 링크에 설정되어있는 기본 스타일 초기화
    2. 목록 요소에 배경색 및 패딩 설정
    3. 웹 브라우저 margin, padding을 0으로 설정
    4. 마우스 롤 오버 설정

  