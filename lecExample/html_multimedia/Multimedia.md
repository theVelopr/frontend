# HTML 요소 - 멀티미티어 & 내장 컨텐츠 & 스크립트

## 멀티미디어
### `<img/>`
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

### `<audio>`
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

### `<video>`
> Lecture 07
- 동영상 컨텐츠(MP4)를 삽입
- inline 요소
- 속성이 autoplay가 지정된 경우, preload는 무시됨.

|속성|	의미|	값|	기본값|
|-|-|-|-|
|autoplay|	준비되면 바로 재생|	불린(Boolean)| |	
|controls|	제어 메뉴를 표시|	불린(Boolean)| |	
|loop|	재생이 끝나면 다시 처음부터 재생|	불린(Boolean)| |	
|muted| 음소거 여부 | 불린(Boolean) | |
|poster| 동영상 썸네일 이미지 URL | URL | |
|preload|	페이지가 로드될 때 파일을 로드할지의 지정(힌트 제공)|	none: 로드하지 않음, metadata: 메타데이터만 로드, auto: 전체 파일 로드|	metadata|
|src|콘텐츠 URL|	URL	| |
|width| 동영상 가로 너비| | |
|height| 동영상 세로 너비| | |

### `<figure>`, `<figcaption>`
- `<figure>` 는 이미지나 삽화, 도표 등의 영역을 설정
  - block 요소
- `<figcaption>`은 `<figure>`에 포함되어 이미지나 삽화 등의 설명을 표시
  - inline 요소
- 브라우저는 분리가 되어 있다는걸 알 수없기 때문에 이 태그를 통해 서로 연결 되어 있다는 것을 알려줌
  - 사용자보다는 브라우저에게 이 요소들이 연결되어 있다고 알려줌  
  
```html
  <figure>
    <img src="./images/heropy.png" alt="HEROPY">
    <!-- <p>HEROPY 이미지이다.</p> -->
    <figcaption>HEROPY 이미지이다.</figcaption>
  </figure>
```

## 내장 컨텐츠

### `<iframe>`
- 다른 HTML 페이지를 현재 페이지에 삽입. (중첩된 브라우저 컨텍스트(프레임)를 표시)
- inline 요소

|속성|의미|값|기본값|
|-|-|-|-|
|name|프레임의 이름| | |
|src|포함될 문서의 URL|URL| |
|width|프레임의 가로 너비| | |
|height|프레임의 세로 너비| | |
|allowfullscreen|전체 화면 모드 사용 여부|Boolean| |
|frameborder|프레임 테두리 사용 여부|`0`, `1`|`1`|
|sandbox|보안을 위한 읽기 전용으로 삽입|allow-form : 양식 제출 가능, allow-scripts : 스크립트 실행 가능, allow-same-origin : 같은 출처(모데인)의 리소스 사용 가능| |

```html
    <iframe src="https://www.danawa.com" 
    frameborder="0"
    width="70%"
    height="400px"
    style="border:4px solid red">
    </iframe>
```


### `<canvas>`
- Canvas API나 WebGL API를 사용하여 그래픽이나 애니메이션을 랜더링
- JavaScript를 모르면 사용 할 수 없는 태그
- inline 요소

|속성|의미|
|width|캔버스의 가로 너비|
|height|캔버스의 세로 너비|

```html
  <canvas id="canvas" width="200" height="150"></canvas>
  <script>
    const canvas = document.getElementById('canvas');
    const ctx = canvas.getContext('2d');
    ctx.fillStyle = 'rgb(200, 0, 0)';
    ctx.fillRect(10, 10, 50, 50); 
    ctx.fillStyle = 'rgb(0, 0, 200, 0.5)';
    ctx.fillRect(30, 30, 50, 50); 
  </script>
```

## 스크립트

### `<script>`
- 스크립트 코드를 문서에 포함하거나 참조(외부 스크립트)

|속성|의미|값|특징|
|-|-|-|-|
|async|스크립트의 비동기적(Asynchronously) 실행 여부 | Boolean | `src` 속성 필수|
|defer|문서 파싱(구분 분석) 후 작동 여부|Boolean| `src` 속성 필수|
|src|참조할 외부 스크립트 URL| URL| 포함된 스크립트 코드는 무시됨|
|type|<a href="https://developer.mozilla.org/ko/docs/Web/HTTP/Basics_of_HTTP/MIME_types">MIME 타입</a>|`text/javascript`(기본값)| |

- 동기 (순차적) 비동기 (비순차적) 이라고 가볍게 표현할 수 있다
- HTML이 작동을 할때 위에서 아래로 절차적으로 읽어들이는데, 그러다보니 실행이 안되는 요소들이 발생한다. 
  - ```html
    <head>
    <meta charset="UTF-8">
        <title>HTML Elements</title>
        <link rel="stylesheet" href="./css/main.css">
        <script src="./js/main.js"></script>
    </head>
    <body>
        <div id="my-name">theVelpr</div>
    </body>
    ```
    ```javascript
    const myName = document.getElementById('my-name');
    console.log(myName.innerText);
    ```
  - 위의 코드를 실행해보면, div부분이 console에서 실행이 되지 않는 것을 볼 수 있는데, 절차적으로 읽다보니 실행이 되지 않는다. 이를 해결하는 방법으로는
    - 1. 물리적으로 위치를 설정
      - ```html
        <head>
        <meta charset="UTF-8">
            <title>HTML Elements</title>
            <link rel="stylesheet" href="./css/main.css">
        </head>
        <body>
            <div id="my-name">theVelpr</div>

            <script src="./js/main.js"></script>
        </body>
        ```
    - 2. defer 속성을 추가 
      - ```html
        <head>
            <meta charset="UTF-8">
            <title>HTML Elements</title>
            <link rel="stylesheet" href="./css/main.css">
            <script src="./js/main.js" defer></script>
        </head>
        <body>
            <div id="my-name">theVelpr</div>
        </body>
        ```

