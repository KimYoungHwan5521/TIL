CSS 기술 방식

```css
h1{
    width: 300px;
    height: 50px;
    font-size: 1.5em;
    color: red;
    font-weight: bold;
}
```



HTML문서에 CSS 적용과 연결

1. HTML 요소 속성으로 CSS 적용

   - 선택자를 통하여 직접 요소에 CSS 스타일 추가

     ```html
     <h1 style="width:300px; height:50px; font-size:1.5em; color:red; font-weight:bold;">이것은 첫 번째 제목 입니다.</h1>
     ```

   - 단점

     - 동일 요소 공통으로 적용 불가
     - 수정 및 변경시 모든 HTML 코드 검토
     - 체계적인 관리와 변경 불가능
     - ∴ 스타일 속성은 테스트용으로만 사용

2. HTML 문서에 CSS 적용과 연결

   - Style 요소를 사용한 CSS 적용

     - 방법: head 부분에 선택자를 이용하여 style요소 정의

     - CSS 코드가 위치한 HTML 파일에만 적용

     - 단점: 전체 수정시 모든 HTML 파일을 수저해야 함

     - style 요소의 속성

       1. type: style 언어가 어떤 MIME 타입인지 지정

          ​		CSS파일의 경우: text/css 지정

          ​		HTML5의 경우: 생략 가능

       2. media: 현재 CSS코드가 어떤 매체일 경우 지정되는지 지정

          ​		"all"지정: 모든 매체에서 현재 CSS 적용, 미디어쿼리

   ```html
   <!DOCTYPE html>
   <html>
       <head>
           <meta charset="UTF-8">
           <title>Title</title>
           <style type="text/css" media="all">
               h1{
                   width: 300px;
                   height: 50px;
                   font-size: 1.5em;
                   color: red;
                   font-weight: bold;
               }
           </style>
       </head>
       <body>
           <h1>이것은 첫 번째 제목입니다.</h1>
           <h2>이것은 두 번째 제목입니다.</h2>
           <h1>이것도 첫 번째 제목입니다.</h1>
       </body>
   </html>
   ```

3. 외부 CSS 파일을 HTML 문서에 연결

   - 장점
     - 여러 HTML 파일에 공통으로 사용
     - 수정시 HTML 파일을 전체 수정할 필요 없음
     - 체계적이고 구조적인 스타일 관리 가능
     - 전체 전송량이 줄어듦
   - 외부 스타일시트 파일: .css를 가지는 파일, 텍스트로 이루어짐
   - HTML에서 외부 CSS 파일의 연결
     - HTML 코드 작성
     - 비어있는 파일을 작성하고 확장자 .css로 저장
     - CSS파일 경로 지정(head(head부분에 link요소 사용)
     - CSS 파일 열어 CSS 스타일 지정
   - link: HTML 문서와 외부 리소스 연결을 위해 사용, 대부분 CSS파일 연결
   - link 요소의 속성
     - rel
       - 생략 불가능
       - 현재 HTML과 연결할 파일간의 관계를 나타냄
       - 다양한 값을 가짐
       - CSS 파일 연결: rel="stylesheet"
     - href
       - 연결하고자 하는 리소스 파일 경로 지정
     - 하나의 HTML파일에 여러개의 link요소 사용하여 각기 다른 여러 CSS 파일 링크 가능