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
- 약어를 지정
- Abbreviation
- 보통 title(전역속성) 속성을 사용하여 전체 글자나 설명을 제공
- inline 요소
- 예시
```html
Using <abbr title="HyperText Markup Language">HTML</abbr> is fun and easy!
```

