# HTML 요소 - 멀티미티어 & 내장 컨텐츠 & 스크립트

## `<img/>`
> Lecture 07
- 이미지 삽입

|속성|의미|값|특징|
|-|-|-|-|
|src|(필수)이미지 URL|URL|
|alt|(필수)이미지의 대체텍스트|
|width|이미지의 가로 너비|
|height|이미지의 세로 너비|
|srcset|브라우저에게 제시할 이미지 URL과 크기의 목록을 정의|w,x|
|sizes|미디어 조건과 해당 조건일 때의 이미지 크기를 정의|
|crossorigin|가져 오기가 CORS를 사용하여 수행되어야하는지 여부|anonymous, use_credentials|
|ismap|서버 측 이미지 맵으로 지정해 클릭하여 좌표를 쿼리스트링으로 서버에 전송할지 여부|Boolean|`<img/>`가 유요한 href 속성을 가진 `<a>`의 하위 요소인 경우에만 허용|
|usemap|클라이언트 측 이미지 맵으로 지정|`<map>`의 ID 속성 값|`<a>`, `<buttom>`의 하위 요소인 경우 사용 불가|

> srcset
> - 주로 반응형에서 많이 사용됨.
> - srcset 속성은 '이미지 소스의 세트'라는 의미를 가짐. <b>같은 비율의 다양한 크기를 가지는 동일 이미지들</b>을 최소 2개 이상 명시하는 속성이다.
> - serset 속성은 <b>브라우저에 이미지 선택권을 위임하는 속성</b>이다.
> - 다른 비율의 다양한 크기의 다른 이미지들을 사용하고 싶다면, IMG 요소의 srcset 속성이 아닌 CSS의 @media 사용을 권장한다. 

w 의 단위 = descriptor 
x 의 단위 = Device pixel ratio description 

w 단위를 쓰는것을 추천


> sizes
> - 미디어조건과 그 조건에 해당하는 이미지의 '회적화 출력 크기'를 지정한다. 

출처 : https://heropy.blog/2019/06/16/html-img-srcset-and-sizes/

## `<audio>`
> Lecture 07
- 소리 컨텐츠를 삽입
- inline 요소
- autoplay가 지정된 경우, preload는 무시됨.

|속성|	의미|	값|	기본값|
|-|-|-|-|
|autoplay|	준비되면 바로 재생|	불린(Boolean)| |	
|controls|	제어 메뉴를 표시|	불린(Boolean)| |	
|loop|	재생이 끝나면 다시 처음부터 재생|	불린(Boolean)| |	
|preload|	페이지가 로드될 때 파일을 로드할지의 지정(힌트 제공)|	none: 로드하지 않음, metadata: 메타데이터만 로드, auto: 전체 파일 로드|	metadata|
|src|콘텐츠 URL|	URL	| |
|muted|	음소거 여부|	불린(Boolean)| |

