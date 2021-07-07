# HTML 요소 - 인라인 텍스트 & 수정

## `<a>`
- 다른 페이지, 같은 페이지 위치(#, 해시 태그), 파일, 이메일 주소, 전화번호 등 다른 URL로 연결할 수 있는 하이퍼링크를 설정.
- Anchor(링크를 건다), 외부로 내보내기
- href, target을 가장 많이 사용함
- inline 요소

| 속성 | 의미 | 값 | 기본값 | 특징|
|----|-----|----|------|--------|
| download | 이 요소가 리소스를 다운로드하는 용도로 사용됨을 의미 | Boolean | | |
| href | 링크 URL | URL | | 생략가능 |
| hreflang | 링크 URL(페이지) 언어(ISO 639-1) | ko, en, ... | | |
| rel | 현재 문서와 링크 URL의 관계(Link TYpes) | license, prev, next, ... | | |
| target | 링크 URL의 표시(브라우저 탭) 위치 | _self, _blank | _self | |
| type | 링크 URL의 MIME 타입 | text/html ... | | |

## `<abbr>`
> Lecture 04
- 약어를 지정
- Abbreviation
- 보통 title(전역속성) 속성을 사용하여 전체 글자나 설명을 제공
- inline 요소
- 예시
```html
Using <abbr title="HyperText Markup Language">HTML</abbr> is fun and easy!
```

## `<b>`
> Lecture 05
- 문체가 다른 글자의 범위를 설정 
- Bring Attention
- (주의사항) 특별한 의미를 가지지 않음.
- (주의사항) 읽기 흐름에 도움을 주는 용도로 사용
- (주의사항) 다른 태그가 적합하지 않은 경우 마지막 수단으로 사용
- (주의사항) 기본적으로 글자가 두껍게 표시됨.
- inline 요소


## `<mark>`
> Lecture 05
- 사용자의 관심을 끌기 위해 하이라이팅할 때 사용
- 기본적으로 형광펜을 사용한 것처럼 글자 배경이 노란색으로 표시됨
- inline 요소

## `<em>`
> Lecture 05
- 단순한 의미 강조를 표시
- emphasis
- 중첩이 가능
- 중첩될수록 강조 의미가 강해짐
- 정보통신보조기기 등에서 구두 강조로 발음됨
- 기본적으로 이탤릭체로 표시됨
- inline 요소

## `<strong>`
> Lecture 05
- 의미의 중요성을 나타내기 위해 사용
- 기본적으로 글자가 두껍게 표시됨
- inline 요소

## `<i>`
> Lecture 05
- `<em>`, `<strong>`, `<mark>`, `<cite>`, `<dfn>` 등에서 표현할 수 있는 적합한 의미가 아닌 경우 사용
- 평범한 글자와 구분(아이콘이나 특수기호 같은)하기 위해 사용
- 기본적으로 이탤릭체로 표시됨
- inline 요소

## `<dfn>`
> Lecture 06
- 용어를 정의할 때 사용
- Definition
- inline 요소

## `<cite>`
> Lecture 06
- 창작물에 대한 참조를 설정
- 기본적으로 이탤릭체로 표시됨
- inline 요소
```html
<cite>The Scream</cite> by Edward Munch. Painted in 1893.
```

## `<q>`
> Lecture 06
- 짧은 인용문을 설정
- 긴 인용문을 설정할 경우 `<blockquote>`를 사용 
- inline 요소

| 속성 | 의미 | 값 |
|---|--|---|
| cite | 인용된 정보의 URL | URL |

## `<u>`
> Lecture 06
- 밑줄이 있는 글자를 설정
- css를 활용하여 밑줄을 표현 하는게 정석임 (css 적용 불가능 한 부분에서만 사용하는걸 추천)
- Underline
- 순수하게 꾸미는 용도의 요소로 사용
- `<a>`와 햇갈릴 수 있는 위치에서 사용하지 않도록 주의
- `<span style="text-decoration: underline;">`을 활용할 수 있을 경우에는 사용을 권장하지 않음
- inline 요소

## `<code>`
> Lecture 06
- 컴퓨터 코드 범위를 설정
- 기본적으로 고정폭(Monospace) 글꼴 계열로 표시됨.
- 독자에게 어디까지가 코드인지 알려주기 위해 사용함.
- inline 요소

```html
<code>document.getElementById('id-value')</code> is a piece of computer code.
```

## `<kdb>`
> Lecture 06
- 텍스트 입력 장치에서 사용자 입력을 나타내는 텍스트 범위를 설정
- inline 요소
```html
<p>
    <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>K</kbd>
</p>

<kbd>ESC</kbd>
```
- 일반 텍스트랑 섞이면 독자입장에서는 명확히 볼 수 없기 때문에 css에서 꾸며주는게 좋다.
```css
kbd {
    padding: 0 3px;
    border-radius: 3px;
    border-top: 2px solid rgb(240, 240, 240);
    border-bottom: 2px solid rgb(205, 205, 205);
    border-left: 2px solid rgb(240, 240, 240);
    border-right: 2px solid rgb(225, 225, 225);
}
```

## `<sup>`, `<sub>`
> Lecture 06
- 위 첨자(`<sup>`)와 아래 첨자(`<sub>`)를 설정.
- Superscripted text, Subscript text
- inline 요소
- 효과 : 위 첨자 지수, 아래첨자는 H2O에서 원자수

## `<time>`
> Lecture 06
- 날짜나 시간을 나타내기 위한 목적으로 사용
- IE 지원 불가
- inline 요소

| 속성 | 의미 | 값 |
|-|-|-|
| datetime | 유효한 날짜 문자 | date |

## `<span>`
> Lecture 06
- 본질적으로 아무것도 나타내지 않는 컨텐츠 영역을 설정
- js에서 많이 활용됨.
- inline 요소

## `<br/>`
> Lecture 06
- 줄바꿈
- inline 요소

## `<del>`
> Lecture 06
- 삭제된(변경된) 텍스트의 범위를 지정
- inline 요소

|속성|의미|값|
|-|-|-|
|cite|변경을 설명하는 리소스의 URI|URI|
|datetime|변경이 일어난 유요한 날짜 문자|Date|



## `<ins>`
> Lecture 06
- 새로 추가된(변경된) 텍스트이 범위를 지정.
- inline 요소

|속성|의미|값|
|-|-|-|
|cite|변경을 설명하는 리소스의 URI|URI|
|datetime|변경이 일어난 유요한 날짜 문자|Date|
