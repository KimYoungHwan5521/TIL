표(table) 만들기

1. table
2. tr
   - table 요소 내부에 정의, 표의 row
   - 요소는 테이블 셀(th 또는 td 요소) 포함
3. td, th
   - td: 테이블 셀을 의미
   - th: 헤더셀을 의미
   - 셀을 정하기 전에 테이블이 몇개의 칼럼으로 구성되어있는지 확인
4. 셀 병합
   - 가로 셀 병합 / 세로 셀 병합
     - colspan / rowspan 사용

Table 구조화

1. thead, tbody, tfoot

   - 표의 가장 큰 구조적 분리

   - thead: 표 머리 부분으로 제목으로 구성된 row 집합

     - 하나 이상의 row로 구성
     - 표마다 하나의 thead 요소만 사용 가능

   - tbody: 일반적인 row의 집합

     - 하나 이상의 row로 구성
     - 하나의 표에 여러개의 tbody 사용 가능
     - 표의 내용 분리가 있을 때 사용

   - tfoot: row의 요약들로 구성된 row 집합

     - 하나 이상의 row로 구성
     - 표마다 하나의 tfoot 요소만 사용 가능
     - table요소 내 위치와 상관없이 tfoot요소는 표 마지막에 표시됨

     ```html
     <table>
         <thead>
             <tr><th>성명</th><th>국어</th><th>영어</th><th>수학</th></tr>
         </thead>
         <tfoot>
         	<tr><td>과목별 합계</td><td>240</td><td>215</td><td>260</td></tr>
             <tr><td>과목별 평균</td><td>80</td><td>72</td><td>87</td></tr>
         </tfoot>
         <tbody>
             <tr><td>김철수</td><td>85</td><td>60</td><td>75</td></tr>
             <tr><td>이영희</td><td>90</td><td>95</td><td>85</td></tr>
             <tr><td>박민순</td><td>65</td><td>60</td><td>100</td></tr>
         </tbody>
     </table>
     ```

     - thead에 꼭 th만 있을 필요는 없다.

2. col, colgroup

   - col: 하나의 column을 의미

     - span 속성을 이용하여 하나 이상의 column을 가리킬 수 있음

   - colgroup: col요소의 그룹

     - table 요소 내부에 위치
     - caption 요소보다 뒤에 있어야 하며 thead, tbody, tfoot요소 보다는 앞에 있어야 함

     ```html
     <table>
         <colgroup id="students"><col></colgroup>
         <colgroup id="subject"><col id="korean"><col id="english"><col id="math"></colgroup>
         
         <thead>
             <tr><th>성명</th><th>국어</th><th>영어</th><th>수학</th></tr>
         </thead>
         <tfoot>
         	<tr><td>과목별 합계</td><td>240</td><td>215</td><td>260</td></tr>
             <tr><td>과목별 평균</td><td>80</td><td>72</td><td>87</td></tr>
         </tfoot>
         <tbody>
             <tr><td>김철수</td><td>85</td><td>60</td><td>75</td></tr>
             <tr><td>이영희</td><td>90</td><td>95</td><td>85</td></tr>
             <tr><td>박민순</td><td>65</td><td>60</td><td>100</td></tr>
         </tbody>
     </table>
     ```

3. scope 속성

   - 정의: th 요소에 사용되는 속성, th의 영향력이 어느쪽으로 향하는지  지정
   - scope 속성 미설정시 scope="auto"로 설정

4. caption 요소

   - 정의: table의 제목을 나타냄, table요소의 첫 번째 자식요소로 가장 먼저 설정
   - 만약 table요소가 figure 요소의 유일한 자식이면 table요소 내부에서 caption요소 대신 figcaption요소로 타이틀 지정

