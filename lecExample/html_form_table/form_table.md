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

### `<input/>`
---
- 사용자에게 입력 받을 데이터 양식

|속성|의미|값|기본값|특징|
|-|-|-|-|-|
|autocomplete|사용자가 이전에 입력한 값으로 자동 완성 기능을 사용할 것인지 여부|`on`, `off`|`on`||
|autofocus|페이지가 로드될 때 자동으로 포커스|Boolean| |문서 내 고유해야 함|
|checked|양식이 선택되었음을 표시|Boolean| |`type` 속성 값이 `radio`, `checkbox`일 경우만|
|disabled|양식을 비활성화|Boolean|||
|form|`<form>`의 `id` 속성 값| ||	해당 `<form>`의 후손이 아닐 경우만|
|list|참조할 `<datalist>`의 `id` 속성 값| |||
|max|지정 가능한 최대 값|숫자||`type` 속성 값이 `number`일 경우만,<br> `min`속성보다 큰 값만 허용|
|min|지정 가능한 최소 값|숫자||`type` 속성 값이 `number`일 경우만,<br> `max`속성보다 큰 값만 허용|
|maxlength|입력 가능한 최대 문자 수|숫자|`524288`|`type` 속성 값이 `text`, `email`,<br> `password`, `tel`, `url`일 경우만|
|multiple|둘 이상의 값을 입력 할 수 있는지 여부|Boolean||`type` 속성 값이 `email`, `file`일 경우만,<br> `email`일 경우 ,로 구분|
|name|양식의 이름| |||
|placeholder|사용자가 입력할 값의 힌트| ||`type` 속성 값이 `text`, `email`,<br> `password`, `tel`, `url`일 경우만|
|readonly|수정 불가한 읽기 전용|Boolean| ||
|step|유효한 증감 숫자의 간격|숫자|`1`|`type` 속성 값이 `number`, `range`일 경우만|
|src|이미지의 URL|URL| |`type` 속성 값이 `image`일 경우만|
|alt|이미지의 대체 텍스트| ||`type` 속성 값이 `image`일 경우만|
|type|입력 받을 데이터의 종류|아래참조|`text`||
|value|양식의 초기 값| |||

#### 데이터 종류(Type)의 값(Value)
- `type` 속성에 입력할 수 있는 값의 목록
  
|값|데이터 종류|특징|
|-|-|-|
|button|일반버튼|`<button>` 처럼 사용|
|checkbox|체크박스| |
|color|색상|IE 지원 불가|
|email|이메일| |
|file|파일| |
|hidden|보이지 않지만 전송할 양식|`value` 속성으로 값을 지정|
|imgae|이미지 제출 버튼|`<img/>` 처럼 사용|
|number|숫자||
|password|비밀|가려지는 양식|
|radio|라디오 버튼|같은 `name` 속성 그룹 내 하나만 선택 가능|
|range|범위 컨트롤|`min`,`max`, `step`, `value`(기본값) 속성 사용|
|reset|초기화|해당 `<form>` 범위 내 모든 양식|
|search|검색||
|submit|제출버튼|해당 `<form>` 범위 내 모든 양식|
|tel|전화번호||
|text|일반 텍스트||
|url|절대 URL||

### `<label>`
---
- labelable의 제목(Caption)
  - `for` 속성으로 라벨 가능 요소를 참조하거나 컨텐츠로 포함
  - labelable elements : `<button>`, `<input>`, `<progress>`, `<select>`, `<textarea>`
- inline 요소

|속성|의미|
|for|참조할 레벨 가능 요소의 `id`속성 값|

- 예시
  ```html
  <!-- 라벨 가능 요소를 참조 -->
  <input type="checkbox" id="user-agreement" />
  <label for="user-agreement">동의하십니까?</label>

  <!-- 라벨 가능 요소를 포함 -->
  <label><input type="checkbox" />동의하십니까?</label>
  ```

### `<button>`
---
- 선택 가능한 버튼을 지정
- inline-block 요소

|속성|의미|값|특징|
|-|-|-|-|
|autogocus|페이지가 로드될 때 자동으로 포커스|Boolean|문서 내 고유해야 함|
|disabled|버튼을 비활성화|Boolean||
|form|`<form>`의 `id` 속성 값| |해당 `<form>`의 후손이 아닐 경우만|
|name|폼 데이터와 함께 전송되는 버튼의 이름|||
|type|버튼 타입|`button`, `reset`, `submit`||

### `<textarea>`
---
- 여러 줄의 일반 텍스트 양식

|속성|의미|값|기본값|특징|
|-|-|-|-|-|
|autocomplete|자동완성기능|`on`,`off`|`on`||
|autofocus|페이지가 로드될 때 자동으로 포커스|Boolean| |문서 내 고유해야 함|
|disabled|비활성화|Booealn||
|form|`<form>`의 `id` 속성 값| |해당 `<form>`의 후손이 아닐 경우만|
|maxlength|입력 가능한 최대 문자 수|숫자|무한||
|name|양식의 이름||||
|placeholder|사용자가 입력할 값의 힌트||||
|readonly|읽기전용|Boolean|||
|rows|양식의 줄 수|숫자|`2`||

### `<fieldset>`, `<legend>`
---
- 같은 목적의 양식을 그룹화(`<fieldset>`)하여 제목(`<legend>`)을 지정
- block 요소

- 예시
  ```html
  <form>
    <fieldset>
      <legend>Coffee Size</legend>
      <label>
          <input type="radio" name="size" value="tall" />
          Tall
      </label>
      <label>
          <input type="radio" name="size" value="grande" />
          Grande
      </label>
      <label>
         <input type="radio" name="size" value="venti" />
          Venti
      </label>
    </fieldset>
  </form>
  ```

#### `<fieldset>`
---
- 같은 목적의 양식을 그룹화

|속성|의미|값|
|-|-|-|
|disabled|그룹 내 모든 양식 요소를 비활성화|Boolean|
|form|그룹이 속할 하나 이상의 `<form>`의 `id` 속성 값||
|name|그룹의 이름||

### `<select>`, `<datalist>`, `<optgroup>`, `<option>`
---
- 옵션(`<option>`,`<optgroup>`) 의 선택 메뉴(`<select>`)나 자동완성(`<datalist>`)을 제공
- 예시
  ```html
  <select>
    <optgroup label="Coffee">
      <option>Americano</option>
      <option>Caffe Mocha</option>
      <option label="Cappuccino" value="Cappuccino"></option>
    </optgroup>
    <optgroup label="Latte" disabled>
      <option>Caffe Latte</option>
      <option>Vanilla Latte</option>
    </optgroup>
    <optgroup label="Smoothie">
      <option>Plain</option>
      <option>Strawberry</option>
      <option>Banana</option>
      <option>Mango</option>
    </optgroup>
  </select>
  ```

#### `<select>`
---
- 옵션을 선택하는 메뉴

|속성|의미|값|기본값|
|-|-|-|-|
|autocomplete|자동완성기능|`on`,`off`|`on`|
|disabled|비활성화|Boolean||
|form|`<form>`의 `id` 속성 값|||
|multiple|다중 선택 여부|Boolean||
|name|양식의 이름|||
|size|한 번에 볼 수 있는 행의 개수|숫자|`0`|

#### `<datalist>`
---
- `<input>`에 미리 정의된 옵션을 지정하여 자동완성 기능을 제공하는 데 사용
  - `<input>`의 `list` 속성 바인딩
  - `<option>`을 포함하여 정의된 옵션을 지정

- 예시
  ```html
  <input type="text" list="fruits">

  <datalist id="fruits">
    <option>Apple</option>
    <option>Orange</option>
    <option>Banana</option>
    <option>Mango</option>
    <option>Fineapple</option>
  </datalist>
  ```

#### `<optgroup>`
---
- `<option>`을 그룹화

|속성|의미|값|
|-|-|-|
|label|(필수)옵션 그룹의 이름||
|disabled|옵션 그룹의 비활성화|Boolean|

#### `<option>`
---
- 선택 메뉴(`<select>`)나 자동완성(`<datalist>`)에서 사용될 옵션
  - 선택적 Empty tag로 사용 가능

|속성|의미|값|특성|
|-|-|-|-|
|label|표시될 옵션의 제목||생략되면 포함된 텍스트를 표시|
|disabled|옵션 비활성화|Boolean||
|value|양식으로 제출될 값||생략되면 포함된 텍스트를 표시|
|selected|옵션이 선택되었음을 표시|Boolean||

### `<progress>`
- 작업의 완료 진행률을 표시
- inline-block 요소
- 예시
  ```html
  <progress value="70" max="100">70 % </progress>
  ```


|속성|의미|값|특징|
|-|-|-|-|
|max|작업의 총량|숫자||
|value|작업의 진행량|숫자|`max`속성을 생략할 경우 `0`~`1`사이의 숫자여야 함

