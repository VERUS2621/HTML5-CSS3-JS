# 애니메이션

## CSS와 애니메이션

CSS3의 animation 속성을 사용하면 자바스크립트나 플래시를 사용하지 않고도 웹 요소에 애니메이션을 추가할 수 있음.
CSS 애니메이션은어떤 면에서는 트랜지션과 비슷하고 어떤 면에서는 다름.

시작 스타일과 끝 스타일을 지정하면 CSS에서 중간 스타일을 자동으로 추가해 전체적으로 부드럽게 변하는 애니메이션 효과를 만들어 내는 것은 비슷함.

CSS 애니메이션은 시작해 끝내는 동안 원하는 곳 어디서든 스타일을 바꾸며 애니메이션을 정의할 수 있다는 점이 트랜지션과 다름.

이 때 애니메이션 중간에 스타일이 바뀌는 지점을 **키프레임(keyframe)**이라고 함.

## 애니메이션 관련 속성

| 속성 | 설명 |
| @keyframes | 애니메이션이 바뀌는 지점을 설정 |
| animation-delay | 애니메이션 지연 시간을 지정 |
| animation-direction | 애니메이션 종류 후 처음부터 시작할지, 역방향으로 진행할 지 지정
| animation-duration | 애니메이션 실행 시간 설정 |
| animation-fill-mode | 애니메이션이 종료되었거나 지연되어 애니메이션이 실행되지 않는 상태일 떄 요소의 스타일 설정 |
| animation-iteration-count | 애니메이션 반복 횟수 지정 |
| animation-name | @keyframes로 설정해 놓은 중간 상태의 이름을 지정 |
| animation-play-state | 애니메이션을 멈추거나 다시 시작함 |
| animation-timing-function | 애니메이션의 속도 곡선을 지정 |
| animation | animation 하위 속성들을 한꺼번에 묶어 지정 |

### `@keyframes` - `애니메이션 지점 설정하기`

**기본형**
```css
@keyframes <이름> {
    <tjsxorwk> { <스타일 >}
}
```
스타일 속성 값이 바뀌는 지점은 `선택자`로 입력함.
시작 위치를 0%, 끝 위치를 100%로 시작과 끝 위치만 사용하겠다면 `from과 to` 라는 키워드로 사용해도 됨.

## `animation-name` - `애니메이션 이름 정하기`

**기본형** `animation-name: <키프레임 이름> | none`

@keyframes속성을 사용할 때도 @-webkit-keyframes나 @-moz-keyframes 처럼 브라우저 접두사를 붙여야 함.

이 `animation-name` 속성을 사용하면 왼쪽  소스로 정의한 애니메이션을 오른쪽 소스 처럼 animation-name 속성에 change-bg라는 값을 적용해 사용할 수 있음

`@keyframes change-bg { .... }`

            ↓

```css
div {
    ....
    animation-name: change-bg;
    animation-duration: 3s;
}
```

## `animation-duration` - `애니메이션 실행 시간 설정`

**기본형** `animation-duration: <시간>`
```css
div {
    ...
    animation-duration: 3s;
}
```

## `animation-direction` - `애니메이션 방향 지정`

**기본형** `animation-direction: normal | alternate`

normal : 애니메이션을 끝까지 실행하면 원래 있던 위치로 돌아감(기본값)
alternative : 애니메이션을 끝까지 실행하면 왔던 방향으로 되돌아가면서 애니메이션을 실행

## `animation-iteration-count` - `반복 횟수 지정`

**기본형** `animation-iteration-count: <숫자> | infinite`

<숫자> : 입력한 숫자만큼 반복 . 기본값 1
infinite : 무한 반복

## `animation-timing-function` - `애니메이션 속도 곡선 지정`

**기본형** `animation-timing-function: linear | ease | ease-in | ease-out | ease-in-out | cubic-bezier(n,n,n,n)`

설명은 [여기](/CSS3/07/07-3/README.md) 참고

## `animation` - `애니메이션 관련 속성 한꺼번에 표기`

길고 복잡한 애니메이션 관련 속성들을 `animation` 속성을 사용하면 간단히 한 줄로 표기할 수 있음.

간략하게 표기해 기본 값을 사용하더라도 `animation-duration` 속성은 반드시 표기해야 함.

**기본형**
`animation: <animation-name> | <animation-duration> | <animation-timing-function> | <animation-delay> | <animation-iteration-count> | <animation-direction>`

예를 들어 `moving` 이라는 애니메이션을 아래처럼 정의했다면

```css
.box {
    animation-name: moving;
    animation-duration: 3s;
    animation-timing-function:ease-in;
    animation-direction: alternate;
    animation-iteration-count: infinite;
}

아래처럼 간단히 표현할 수 있음

```css
.box {
    animatiom: moving 3s alternate infinite ease-in;
}
```




