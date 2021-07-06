# 문자 컨텐츠
## `<ol>` , `<ul>`, `<li>`

- ol : ordered list
- ul : unordered list
- li : list item

<br>

- ol과 ul은 자식으로 li만 포함 가능
- li는 단독으로 사용할 수 없으며, ol이나 ul에 자식으로 포함되어야 함.
- li는 list item 요소이지만, 크게보면 블럭요소이다. 

`<ol>`
- reversed : 항목을 역순으로 설정 (IE 지원 불가) but 물리적이진 않음.
- start : 항목에 매겨지는 번호의 시작 값
- type : 항목에 매겨지는 번호의 유형 (a, A, i, I, 1)

```html
<ol type="I">
    ...
```

`<li>`
- value: 항목의 순서를 설정 | 숫자를 입력 | 입력한 숫자 이하 항목들의 순서가 다시 지정됨
```html
<li value="7">
    ...
    7, 8, 9 ...
```

## `<dl>`, `<dt>`, `<dd>`
- 용어(`<dl>`)와 정의(`<dt>`) 쌍들의 영역(`<dl>`)을 설정
- 용어의 집합을 나타내는 태그
- Description List, Definition Details, Definition Term
- `<dl>`은 `<dd>`, `<dt>`만을 포함해야함
- Key/Value 형태를 표시할 때 유용함.
- block 소요이다.
- 문법으로 인해 활용도가 많이 떨어져서 대체로 ul, li로 많이 사용한다.
```html
<dl>
    <dt>Coffee</dt>
    <dd>Coffee is a brewed drink prepared from roasted coffee beans, the seeds of berries from certain coffea species.</dd>
    <dt>Milk</dt>
    <dd>Milk is a nutrient-rich, white liquid food produced by the mommary glands of mommals.</dd>
</dl>
```