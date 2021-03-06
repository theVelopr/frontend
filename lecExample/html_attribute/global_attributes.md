# 전역 속성(Global Attributes)
- 모든 HTML 요소에서 공통적으로 사용 가능한 속성

## class
- 공백으로 구분된 요소의 별칭을 지정
- CSS, JS 요소 선택기를 통해서 요소를 선택하거나 접근
- 별명, 중복가능

## id
- 문서에서 고유한 식별자를 정의
- CSS, JS 요소 선택기를 통해서 요소를 선택하거나 접근
- 이름(고유함), 중복값 불가

## style
- 요소에 적용할 CSS를 선언

## title
- 요소의 정보(설명)을 지정
- mouse over 했을때 설명을 보여줌

## lang
- 요소의 언어를 지정

## data-*
- 사용자 정의 데이터 속성을 지정
- HTML에 JS에서 이용할 수 있는 데이터(정보)를 저장하는 용도로 사용
- data- 뒤에 사용자가 원하는 이름을 입력하면됨. ex) data-my-name="Slim Shaddy"

## draggable
- 요소가 Drag and Drop API를 사용 가능한지 여부를 결정

## hidden
- 요소를 숨김

## tabindex
- `tab` 키를 이용해 요소를 순차적으로 포커스 탐색할 순서를 지정
  - 대화형 콘텐츠(Interactive Content)는 기본적으로 코드 순서대로 탭 순서가 지정됨.
  - 비대화형 콘텐츠에 `tabindex="0"`을 지정하여 대화형 콘텐츠와 같이 탭 순서를 사용.
  - `tabindex="-1"`을 통해 포커스는 가능하지만 탭 순서에서 제외 가능.
  - `tabindex="1"` 이상의 양수 값은 논리적 흐름을 방해하기 때문에 사용을 추천하지 않음.
  - 왠만하면 HTML이 작성된 순서대로 진행되도록 그대로 두는 것을 추천함

## 절대경로와 상대경로
- 상대경로
  - ./(생략가능)  
    - 기준경로에서 주변에 있으면 들어가기
    - ex) `<img src="./images/abc.jpg>` or `<img src="images/abc.jpg>`
  - ../ - 기준경로에서 나가기
    - ex) 'background: url("../assets/images/abc.jpg");'
  

- 절대경로
  - http
  - /
  - ex) `https://google.com`

## 특수기호
- `&nbsp;` 
  - 띄어쓰기
- `&lt;` ... `&gt;`
  - <...>