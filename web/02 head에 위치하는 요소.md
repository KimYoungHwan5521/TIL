head에 위치하는 요소

1. 타이틀

   - HTML 파일의 제목
   - 웹브라우저 타이틀바에 타이틀이 나타남
   - 즐겨찾기나 북마크를 저장 할때도 사용되므로 적절한 제목을 선택해야함

2. 문자 인코딩

   - 문자나 기호들의 집합을 컴퓨터에서 저장하거나 통신에 사용할 목적으로 부호화 하는 방법
   - 텍스트 에디터의 문자 인코딩 설정 = html 헤더 부분에 설정한 문자 인코딩

3. 메타 요소

   - 메타데이터: 파일에 관한 정보를 가지고 있는 데이터

     예)  MP3 음원: 노래 제목, 앨범 정보, 아티스트 등

   - HTML의 메타요소의 필요성
     - 구글 등 검색로봇에 의해 수집되는 정보: 사이트 홍보에 유리
     - HTML 파일에 대한 정보를 기록

4. 외부 파일 연결

   - 웹페이지는 HTML, CSS, JavaScript 3가지로 이루어짐
     - HTML: 콘텐츠의 구조 정의
     - CSS: 콘텐츠의 레이아웃과 표현 등 외향을 정의
     - JavaScript: 콘텐츠의 작동을 정의
     - HTML, CSS, JavaScript를 HTML 페이지에 같이 넣을 수 있지만 다른 파일로 분리하는 것이 유지 보수에 유리



```html
<head>
    <title> 타이틀 </title> <!-- 타이틀 -->
    <meta charset="UTF-8"> <!-- 문자 인코딩 -->
    <meta name="description" content="HTML5와 Javascript 학습 콘텐츠">
    <meta name="keywords" content="HTML5, CSS, JavaScript"> <!-- 메타요소들 -->
    <link rel="stylesheet" href="css/style.css"> <!-- 외부 CSS 파일 연결 -->
    <script src="js/script.js"></script> <!-- 외부 JavaScript 파일 연결 -->
</head>
```

