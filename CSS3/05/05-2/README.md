# 다단으로 편집하기

## column-width - 단의 넓이 고정하고 다단 구성하기

**기본형** `column-width: <크기> | auto`

<크기> : 단 너비를 직접 지정
auto : 단의 개수(column-count) 같은 다른 속성에 따라 단의 너비가 자동으로 계산

단의 너비를 고정하는 것이 기본이지만 여러 단을 표시하기도 하고 
지정한 너비보다 더 넓게 표시될 수도 있으며, 
한 개의 단 너비보다 공간이 좁다면 지정한 너비보다 좁게 표시될 수 있음.

## column-count - 단의 개수 고정하고 다단 구성하기

**기본형** `column-count: <숫자> | auto`

<숫자> : 콘텐츠가 들어갈 단의 개수를 지정. 0보다 큰 수를 사용함.
auto : 단의 너비(column-width) 같은 다른 속성에 따라 단의 개수가 자동으로 계산됨.

## column-gap - 단과 단 사이 여백 지정

**기본형** `column-gap: <크기> | normal`

<크기> : 단과 단 사이의 여백을 숫자로 지정
normal : 여백을 자동으로 지정. W3C에서 권장하는 여백은 **1em**

## column-rule - 구분선의 색상, 스타일, 너비 지정

**기본형**
```css
column-rule-color: <색상>
column-rule-style: none | hidden | ditted | dashed | solid | double | groove | ridge | inset | ouset
column-rule-width: <크기> | thin | medium | thick
column-rule : <너비> <스타일> <색상>
```

## break-after - 다단 위치 지정하기
```css
break-after : column | avoid-column 
break-before : column | avoid-column
break-inside : column | avoid-column
```
column : 단 나눔
avoid-column : 단 나누지 않음

단 나눌 위치
before(특정 요소 앞), after(뒤), inside(안)

> 크롬과 파이어폭스 브라우저 경우 완벽히 지원하지 않음
지원상황은 계속 바뀌므로 브라우저별 지원 사항을 참고할 것
[브라우저별 지원 사항](http://caniuse.com/#feat=multicolumn)

## column-span - 여러 단을 하나로 합치기

**기본형** `column-span: 1 | all`

1 : 단을 하나로 합치는 것이므로 합치지 않는 것과 같음 (기본 값)
all : 전체 단을 하나로 합쳐 표현 함. 단의 일부만 합칠 수는 없음