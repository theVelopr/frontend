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


