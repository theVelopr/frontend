# HTML 요소 - 표 컨텐츠 & 양식
> Lecture 08 



## 표 컨텐츠
### `<table>`, `<tr>`, `<th>`, `<td>`
---
- 데이터 표(`<table>`)의 행(줄 / `<tr>`)과 열(칸, 셀(Cell) / `<th>`, `<td>`)을 생성.<br>
(Table Row(tr), Table Header(th), Table Data(td))

- table이라는 display 속성의 특성은 블럭요소와 유사한 특성을 가진다. 
- table row와 cell의 속성의 특성은 칸이다.
- 이걸로 레이아웃을 잡으면 안되고 정말 테이블을 사용할때 사용해야함. 
- 

### `<th>`
---
- '머리글 칸'을 지정
- colspan, rowspan : 자신이 있는 셀을 기준으로 몇칸을 사용 할 것인지
- headers : id의 값에 종속된 속성으로 지정함

|속성|의미|값|기본값|
|-|-|-|-|
|abbr|열에 대한 간단한 설명| | |
|headers|관련된 하나 이상의 다른 머리글 칸 `id` 속성 값| | |
|colspan|확장하려는(병합) 열의 수| |`1`|
|rowspan|확장하려는(병합) 행의 수| |`1`|
|scope|자신이 누구의 '머리글 칸'인지 명시|`col` : 자신의 열<br> `colgroup` : 모든 열 <br> `row` : 자신의 행<br> `rowgroup` : 모든 행<br> `auto` |`auto`|

### `<td>`
---
- '일반 칸'을 지정

|속성|의미|값|기본값|
|-|-|-|-|
|headers|관련된 하나 이상의 다른 머리글 칸 `id` 속성 값| | |
|colspan|확장하려는(병합) 열의 수| |`1`|
|rowspan|확장하려는(병합) 행의 수| |`1`|

### `<caption>`
---
- 표의 제목을 설정
  - 열리는  table 태그 바로 다음에 작성해야 함
  - `<table>`당 하나의 `<caption>`만 사용 가능
- table-caption이라는 display 속성을 가짐

### `<colgroup>`, `<col/>`
---
- 표의 열들을 공통적으로 정의하는 컬럼(`<col>`)과 집합(`<colgroup>`)<br>
  (Column, Column Group)

|속성|의미|값|기본값|
|-|-|-|-|
|span|연결되는 열 수|숫자|`1`|

### `<thead>`, `<tbody>`, `<tfoot>`
- 표의 머리글(`<thead>`), 본문(`<tbody>`), 바닥글(`<tfoot>`)을 지정.
  - 기본적으로 테이블의 레이아웃에 영향을 주지 않음


## 양식


### `<form>`
---
- 웹 서버에 정보를 제출하기 위한 양식 범위를 정의
  - `<form>`이 다른 `<form>`을 자식요소로 포함할 수 없음
- block 요소
  
|속성|의미|값|기본값|
|-|-|-|-|
|action|전송한 정보를 처리할 웹페이지 URL|URL| |
|autocomplete|사용자가 이전에 입력한 값으로 자동 완성 기능을 사용할 것인지 여부|`on`, `off`|`on`|
|method|서버로 전송할 HTTP 방식|`GET`,`POST`|`GET`|
|name|고유한 양식의 이름| | |
|novalidate|서버로 전송시 양식 데이터의 유효성을 검사하지 않도록 지정| | |
|target|서버로 전송 후 응답받을 방식을 지정|`_self`, `_blank`|`_self`|

