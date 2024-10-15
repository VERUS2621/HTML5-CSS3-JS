# 트랜지션

트랜지션이란 웹 요소의 **배경 색**이 바뀌거나 **도형의 테두리가 원형으로 바뀌는 것**처럼 **스타일 속성이 바뀌는 것**을 말함

> 트랜지션은 마이크로소프트 엣지와 인터넷 익스플로러(IE) 10 이상에서 지원되며 크롬을 비롯한 파이어폭스, 오페라 사파리 등 대부분의 최신 브라우저에서 모두 지원 됨

하지만 초기의 모던  브라우저에서도 사용할 수 있게 하려면 브라우저 접두사를 붙여야 함. 후 IE10 이후부터 -ms- 접두사 없이 지원하므로 붙이지 않음.

| 속성 | 설명 |
| ---- | ---- |
| transition-property | 트랜지션 대상을 설정 |
| transition-duration | 트랜지션 진행 시간을 설정 |
| transition-timing-function | 트랜지션 속도 곡선을 설정 |
| transition-delay | 트랜지션 지연 시간을 설정 |
| transition | 위 속성을 한꺼번에 설정 함.

## transition-property - `적용할 속성 지정`

**기본형** `transition-property: all(기본값) | none | <속성 이름>`

트랜지션을 어느 속성에 적용할지를 결정함.
사용하지 않을 경우, 모든 속성이 트랜지션 대상이 되고 특정 소속 이름을 말하면 그 속성에 트랜지션이 적용됨.

<속성 이름>이 여러 개일 경우 쉼표(,)로 구분함.

```css
transition-property:all; /*모든 속성에 적용 */
transition-property:background-color; /* 해당 요소의 배경 색에 트랜지션 적용 */
transition-property:width, height; /* 너비와 높이에 적용 */
```

## transition-duration - `트랜지션 진행 시간 지정`

**기본형** `transition-duration: <시간>` (기본 진행 시간은 0초)

시간 단위는 초(seconds) 또는 밀리초(milliseconds)
트랜지션이 대상이 되는 속성이 여러 개라면 트랜지션 진행 시 **시간도 쉼표(,)** 로 구분해 여러 개를 지정할 수 있음.

만약 `transition-property`에서 지정한 값의 개수가 `transition-duration`이랑 일치하지 않으면?

이럴 때는 처음의 지정한 갯수만큼 반복하여 적용됨. 

4개 인데 2개라면 (2s, 3s 로 설정했다면) -> (2s, 3s, 2s, 3s)

## transition-timing-function - `트랜지션 속도 곡선 지정`

속도 곡선은 미리 정해진 키워드나 '베지에 곡선'을 이용해 표현함

**기본형** `transition-timing-function: linear | ease | ease-in | ease-out | ease-in-out | cubic-bezier(n,n,n,n)`

| 속성 값 | 설명 |
| ------ | ---- |
| linear | 시작부터 끝까지 똑같은 속도로 트랜지션을 진행 |
| ease | 처음에는 천천히 점점 빨라지다가 마지막에는 천천히 끝냄(기본값) |
| ease-in | 시작을 느리게 함 |
| ease-out | 느리게 끝냄 |
| ease-in-out | 느리게 시작하고 느리게 끝냄 |
| cubic-bezier(n,n,n,n) | 베지에 함수를 직접 정의해 사용. n에서 사용할 수 있는 값은 0~1 |

## transition-delay -`지연 시간 설정`

**기본값** `transition-dealy: <시간>`

지정하는 시간만큼 기다렸다가 트랜지션이 시작됨.
사용할 수 있는 값은 초(seconds)나 밀리초(milliseconds) / 기본값은 0s임.

## transition - 트랜지션 속성 한꺼번에 표기하기

앞에서 본것 처럼 트랜지션과 관련된 속성은 여러 가지이고 각 브라우저에 맞게 속성 이름 앞에 접두사를 붙여야 함. 

-webkit-, -moz-, -o- 접두사를 붙이고 표준 속성까지 모두 사용하면 각 속성 당 여러 줄의 소스를 사용하게 되고
트랜지션의 속성을 모두 표기해야 할 경우 소스가 매우 길어짐

-> 가독성이 떨어짐.

소스가 아무리 길어지더라도 트랜지션 적용 대상을 2~3개씩 일부만 지정할 경우 transition-property 속성을 이용해 대상을 알려주고
각 대상별로 진행 시간이 다르다면 transition-duration 속성을 이용해 시간도 따로 지정해야 함.

-----

**기본값** `transition: <transition-property 값> | <transition-duration 값> | <transition-timing-function> | <transtion-delay 값>`
