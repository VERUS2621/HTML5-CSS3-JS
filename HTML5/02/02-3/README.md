# SVG 이미지

## SVG 파일 형식이란?

웹 사이트를 표시할 화면은 다양하기 때문에 같은 이미지라도 작게, 크게 표현해야할 때가 있음

gif, jpg/jpeg, png -> 크게 확대하면 이미지 테두리 부분이 울퉁불퉁해짐 
이러한 이미지를 **비트맵 이미지(bitmap image)** 라고 함.

반면, 이미지를 아무리 확대하거나 축소해도 원래의 깨끗한 상태로 유지되는 이미지를 **벡터 이미지(vector image)** 라고 함.

그런 이미지가 바로 SVG 이미지(Scalable Vector Graphics)임.
SVG는 크기를 조정해도 이미지가 깨지지 않고 깨끗이 유지되기 때문에
로고나 아이콘, 데이터 시각화에서 차트나 다이어그램, 지도를 구현할 때 많이 사용함.

복잡한 데이터를 구현해 주는


- [d3.js](http://d3js.org)
- [Raphael.js](http://dmitrybaranovskiy.github.io/raphael)


같은 자바 스크립트 라이브러리에서 차트나 그래프를 표현하는 방식이 SVG 이미지임.

----

SVG 이미지는 태그를 이용해서 삽입할 수도 있지만 태그를 이용해 직접 만들 수 있음.

대부분의 모던 브라우저에서는 svg 파일을 지원
**인터넷 익스플로러 8이하 안드로이드 2.3 이하 버전에서는 svg 파일을 표시할 수 없음.**

이럴 때 사용자의 브라우저가 svg 파일을 지원하는지 테스트해보고 지원하지 않는다면
`<img>` 태그의 src 속성에 png 파일 경로를 지정해 주는 식으로 사용

### Modernizr

브라우저에서 특정 기능을 지원하는지 여부를 테스트해 주는 툴 [Modernizr](https://Modernizr.com/)

관련 파일을 다운로드 후
`<script src="modernizr-custom.js"></script>` 를 `<head>` 사이에 삽입

후 `<script> 안에 if (!Modernizr.svg)` 작성 
또는 if, else 문을 작성해서 SVG 기능을 지원하지 않는다면 png로 대체하는 문을 작성하면 된다.
