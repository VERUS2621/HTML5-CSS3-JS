# 문단 스타일

## directon - 글자 쓰기 방향

**기본형** `direction: ltr | rtl`

ltr : 왼쪽에서 오른쪽으로 (left-to-right) / 기본값
rtl : 오른쪽에서 왼쪽으로 (right-to-left)

아랍어 같은 경우 -> 오른쪽에서 왼쪽으로 씀

다만, 한글이나 영어처럼 왼쪽에서 오른쪽으로 쓰는 언어일 경우, 속성 값을 rtl로 입력해도
텍스트 표시 순서는 바뀌지 않고 왼쪽에서 오른쪽을 정렬되어 나타남.

## text-align - 텍스트 정렬

문단의 텍스트 정렬 방법

**기본형** `text-align: start | end | left | right | center | justify | match-parent`

| 속성 값 | 설명 |
| ---- | ---- |
| start | 현재 텍스트 줄의 시작 위치에 맞추어 문단을 정렬(언어 쓰는 방향에 맞추어) |
| end | 현재 텍스트 줄의 끝 위치에 맞추어 문단을 정렬(언어 쓰는 방향에 맞추어) |
| left | 왼쪽에 맞추어 정렬 |
| right | 오른쪽에 맞추어 정렬 |
| center | 가운데 맞추어 정렬 |
| justify | 양쪽에 맞추어 정렬 |
| match-parent | 부모 요소에 따라 문단을 정렬 / 부모 요소의 속성값이 start나 end일 경우 부모의 요소의 (언어 쓰는 방향에 맞추어) left나 right 값으로 계산해 적용 |

## text-justify - 정렬 시 공백 조절

바로 앞에서 한 `text-align` 속성 값이 justify일 경우, 양쪽 끝에 맞추기 때문에 글자와 문자 사이 간격이 어색하게 벌어질 수 있음.
이때 간격을 어떻게 조절해 정렬할 것인지 지정하기 위해 사용하는 것이 위 속성임.

**기본형** `text-justify: auto | none | inter-word | distribute`

| 속성 값 | 설명 |
| ---- | ---- |
| auto | 웹 브라우저에서 자동으로 지정 |
| none | 정렬하지 않음 |
| inter-word | 단어 사이의 공백을 조절해 정렬 |
| distribute | 인접한 글자 사이의 공백을 똑같이 맞추어 정렬 |

## text-indent - 텍스트 들여 쓰기

문단의 첫 글자를 얼마나 들여쓸지 지정
**기본형** `text-indent : <크기> | <백분율>`

크기 : 단위와 함께 들여 쓸 크기를 지정 (음수 값도 사용 갸능)
백분율 : 부모 요소의 너비를 기준으로 상대적 크기를 지정

## line-height - 줄 간격

**기본형** `line-heigth : normal | <숫자> | <크기> | <백분율> | inherit`

<숫자>나 <백분율> -> 글자 크기를 기준으로
예로 들어 (글자 크기) = 12px 일 때 줄 간격을 2.0으로 했을 때 줄 간격은 2.0배인 24px 백분율도 같은 비율로 계산
- 보퉁 줄 간격은 글자 크기의 1.5~2배가 적당

아래는 모두 줄 간격 30px을 나타냄

```css
{font-size: 15px; line-height:30px;}
{font-size: 15px; line-height:2.0;}
{font-size: 15px; line-height:200%;}
```

## text-overflow - 넘치는 텍스트 표기

`white-space: nowrap`으로 지정해 줄 바꿈을 하지 않을 떄는 텍스트가 기준선을 벗어나 넘칠 수도 있다.

**기본형** `text-over-flow: clip | ellipsis`

clip : 넘치는 텍스트를 자름 (기본형)
ellipsis : 말 줄임표(...) 로 잘린 텍스트가 있다고 표시함.

단, text-overflow 속성은 해당 요소에서 overflow 속성값이

위 조건을 모두 만족해야함.

`hidden(표시되지 않고 숨김)` 이거나 `scroll(넘치는 콘텐츠 스크롤바를 통해 확인)` 또는 `auto(콘텐츠가 넘칠 때에만 스크롤바가 자동으로)`
white-space:nowrap 속성을 함께 사용했을때만 적용