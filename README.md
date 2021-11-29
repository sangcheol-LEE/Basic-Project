# HTML,CSS 첫걸음

## HTML

- 구조를 만드는 언어
- 마크업 언어

## CSS

- 웹의 시각적인 표현을 담당
- 예쁘게 만들어 주는 언어

## JS

- 콘텐츠를 바꾸고 움직이는 등 페이지를 동적으로 꾸며주는 역할을 하는 프로그래밍 언어로 웹의 동적 처리를 담당

## 웹 표준

- W3C의 권고안에서 나온 기술이고, 웹에서 사용되는 표준 기술이나 규칙 (HTML, CSS, JS)을 기반으로 웹 브라우저를 만듭니다.

## 크로스 브라우징

- 많은 브라우저들에서 동일한 결과물로 출력되게 만들어야 한다.

## 웹 접근성

- 누구나 쉽게 웹사이트를 이용할 수 있게 해주는 것
- 청각장애인을 위해 영상자막, 마우스를 사용할 수 없는 분들을 위해 키보드를 통해 웹사이트 사용, 이미지에 대체 텍스트 등

## 이미지에 대한 이해

- 비트맵과 벡터 이미지

* 비트맵

- 각 픽셀이 모여 만들어진 정보의 집합으로 레스터(Raster)이미지라고도 부릅니다.
- 픽셀 단위로 화면에 렌더링
- .JPG(.jpeg), .PNG, .gif 등

* 벡터

- 수학적 정보의 형태들이 만들어내는 결과물입니다.
- 이미지가 가지고 있는 점, 선, 면의 위치(좌표) 색상 등의 정보를 온전히 가지고 화면에 렌더링합니다.
- 확대 및 축소를 해도 이미지가 깨지지 않습니다.
- .svg

# HTML 기본문법

## 기본 형태

- 태그는 각자의 의미를 가지고 있으며 다음과 같은 형태를 가집니다.
- <TAG></TAG>, <TAG>something</TAG>

## 속성(Attributes)과 값 (value)

- 태그(요소)의 기능을 확장하기 위해 '속성'을 사용할 수 있습니다.
- <img src="imageUrl(이미지 경로)" alt=" 대체 텍스트 " />

## 부모와 자식요소

- <parents> <Child></Child> <parents>

## 빈 태그

- HTML에는 닫히는 개념이 없는 태그들이 있다.
- <TAG />
- ex) <img />
- html5 에서는 위 2가지 형태를 다 사용할 수 있는데 개발하는 환경에 따라 사용할 수 있는데 쓸꺼면 전부 다쓰고 안쓸꺼면 아예 쓰지말자
- 혼용만 하지말자 !

## HTML 문서의 범위

- DOCTYPE (DTD, Document Type Definition)은 마크업 언어에서 문서 형식을 정의합니다.
- <!DOCTYPE html>
- <html> 
      <head>
        문서의 정보 
      </head>
      <body>
        문서의 구조
      </body>
  </html>

## HTML 문서의 정보

- head 태그 안에서 사용되는 태그들은 문서의 정보를 가지고 있다.

1. title - 웹 페이지의 제목
2. meta - 웹 페이지의 정보 (웹 페이지에 관한 정보(표시 방식, 제작자, 내용, 키워드 등)를 검색엔진이나 브라우저에 제공, 빈 태그입니다.)
3. Link - 외부 문서를 연결할 때 사용합니다.
4. Style - css를 직접 작성하는 태그(css를 외부 문서에서 작성하여 연결하는 것이 아니라 html 문서 내부에서 작성할 때 사용)
5. Script - js 불러오거나 작성하기

- body 태그 안에서 사용되는 태그들읜 문서의 구조를 나타내고 화면에 직접 출력되는 태그들이다.

1. Div - 막 쓰는 태그
2. IMG - 이미지를 넣는 태그

# CSS

## 태그의 직접 작성하기 - 인라인 선언 방식

- <div style="color: red;"> 태그의 직접 작성 </div> 
  // 이 방법은 html 태그에 직접 작성하기 때문에 선택자가 필요하지 않습니다.
  // 자바스크립트가 html에 css를 강제삽입 할 때 사용하긴한다.

## HTML에 포함하기 - 내장 선언방식

- <head>
  <style> 
    div {
      color :red;
    }
  </style>
  </head>
  <body> 
    <div> html에 포함 </div>
  </body>

## HTML 외부에서 불러오기

- css 코드를 완전히 분리할 수 있습니다.
- 분리된 하나의 css 파일을 여러 html 파일이 불러와서 사용가능
- <link rel="stylesheet" href="./css/main.css">
- 경로 "./" => 내 주변에서 찾겠다.

## 선택자

- 선택자는 HTML의 특정한 요소를 선택하는 사인(Sign)입니다.

1. 태그로 찾기

- 선택자를 입력하는 부분에 적용하려는 태그의 이름을 입력
- h1 {
  color: red
  }
- p {
  color : blue
  }

- 클래스로 찾기 // class="title"은 글자색이 빨강색이야!
- .title {
  color: red;
  }

## 속성

- 크기,여백,색상 같은 눈에 보이는 스타일을 지정할 수 있다.

1. 크기

- width - 요소의 가로 너비
- height - 요소의 세로 너비
- font-size - 글자 크기

2. 여백

- margin - 요소의 바깥 여백
- padding - 요소의 내부 여백

3. 색상

- font-color - 요소의 글자 색상
- background-color - 요소의 배경 색상
