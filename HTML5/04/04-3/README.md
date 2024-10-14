# IE8 이하 버전에서는?


HTML5의 새로운 시맨틱 태그는 대부분의 웹 브라우저에서는 사용할 수 있지만
인터넷 익스플로러(IE) 8에서는 지원하지 않고 모바일용 바라우저인 오페라 미니에서는 일부만 지원함.


[can i use](http://caniuse.com)

위 사이트에서 HTML5와 CSS3 속성을 비롯한 관련 기능도 확인 가능, 시맨틱 태그 지원 여부도 살펴볼 수 있음.

### 만약 8이하에서 사용하려면?

요즘 옛날과 달리 인터넷 익스플로러를 사용하더라도

MS -> Edge로 넘어갔기 때문에
간단히 다룸

1. CSS에서 블록레벨로 정의하기.
브라우저는 자신이 인식하지 못하는 태그를 만나면 -> 인라인 태그로 취급 / 위치값을 가지지 못함.

```css
header, section, nav, article, footer {
    display:block;
}
```
처럼 블록 레벨 태그로 바꿔줘야 함.

2. 시멘틱 태그 직접 정의하기
```css
<script>
    document.createElement('article')
    ...
    ...
</script>
```

3. HTML5 Shiv 사용

위 직접 정의하는 과정을 자바스크립트 파일로 만들어 사용할 수 있도록 만든 `HTML5 Shiv` 를 사용
대부분 이 방법으로 `html5shiv.js` 파일을 사용함.

## 브라우저 사이의 차이를 매꾸어 주는 폴리필(pollyfill)

최신 브라우저라도 HTML5 표준 기능들이 어떤 브라우저에서는 되고 어떤 브라우저에서는 안됩니다.
이것을 `브라우저 파편화(browser fragmentation)` 이라고 부름

이러한 파편화를 줄이고 비슷하게라도 같은 결과를 만들기 위한 방법이 `심(shim) 또는 폴백(fallback)` 이라고 부름
아까 htmlshiv도 `shim`의 일종임.

폴리필은 파편화가 생기는 브라우저에 삽입하는 자바스크립트로 브라주어를 스스로 진단해 필요한 `shim`을 자동으로 끼워줌

[HTML5 Cross Browser Pollyfills](https://github.com/Modernizr/Modernizr/wiki/)

위 페이지를 참고하면 각 기능별로 폴리필이나 심, 폴백을 한눈에 볼 수 있음.