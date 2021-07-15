# HTML 요소 - 표 컨텐츠 & 양식
> Lecture 08

## 표 컨텐츠
### `<table>`, `<tr>`, `<th>`, `<td>`
- 데이터 표(`<table>`)의 행(줄 / `<tr>`)과 열(칸, 셀(Cell) / `<th>`, `<td>`)을 생성.<br>
(Table Row(tr), Table Header(th), Table Data(td))

- table이라는 display 속성의 특성은 블럭요소와 유사한 특성을 가진다. 
- table row와 cell의 속성의 특성은 칸이다.

### `<th>`
- '머리글 칸'을 지정

|속성|의미|값|기본값|
|-|-|-|-|
|abbr|열에 대한 간단한 설명| | |
|headers|관련된 하나 이상의 다른 머리글 칸 `id` 속성 값| | |
|colspan|확장하려는(병합) 열의 수| |`1`|
|rowspan|확장하려는(병합) 행의 수| |`1`|
|scope|자신이 누구의 '머리글 칸'인지 명시|`col` : 자신의 열<br> `colgroup` : 모든 열 <br> `row` : 자신의 행<br> `rowgroup` : 모든 행<br> `auto` |`auto`|

### `<td>`
- '일반 칸'을 지정

|속성|의미|값|기본값|
|-|-|-|-|
|headers|관련된 하나 이상의 다른 머리글 칸 `id` 속성 값| | |
|colspan|확장하려는(병합) 열의 수| |`1`|
|rowspan|확장하려는(병합) 행의 수| |`1`|

