# 기타 다양한 폼 요소들

## `<button>` - 버튼 넣기

`<button>` 태그를 이용해도 폼을 전송하거나 리셋하기 위한 버튼을 삽입할 수 있음

**기본형** `<button [type="submit | reset | button"]> 내용 </button>
- 지정하지 않으면 submit으로 간주 됨.

| 속성값 | 설명 |
| ----- | --- |
| submit | 폼을 서버로 전송
| reset | 폼에 입력된 모든 내용을 초기화 |
| button | 버튼 형태만 만들 뿐 자체 기능은 없음 |

웹 문서에서 버튼은
`<input type="submit | reset | button">` 처럼 `<input>` 태그를 이용해서 삽입할 수도 있고
`<button>` 태그를 이용해서도 삽입할 수 잇음

```
<input type="submit" value="전송하기">
<button type="submit">전송하기</button>
```

차이점이라면 `<button>` 태그는 태그 이름에서 그 역할을 알 수 있기 때문에 -> 화면 낭독기에서 버튼이 있다고 알려줌
또, 버튼에 콘텐츠를 포함할 수 있기 떄문에 **아이콘을 추가**할 수도 있고 **CSS를 이용해 원하는 형태**로도 꾸밀 수 있음

- CSS를 이용해 버튼에 마우스 포인터를 올려놓았을 때의 스타일도 지정할 수 있음
- 또 이미지 파일로 만들어 넣었을 때보다 서버에서 훨씬 빨리 읽어옴

## `<output>` - 계산 결과

`<output>` 태그는 입력하는 값이 계산 결과라는 것을 브라우저에게 알려줌

**기본형** `<output [속성="속성값"]> 내용 </output>

계산의 결과 값이라는 점을 브라우저가 **정확하게** 인식할 수 있음

[결과값 예제](./output.html)

## `<progress>` - 진행 상태 보여주기

**기본형** `<progress value="값" [max="값"]></progress>`

태그에서 사용할 수 있는 속성

value
- 작업 진행 상태를 나타내며 **부동 소수점**으로 표현함.
- 이 값은 0보다 크거나 같고 max 값보다 작거나 같음
- 만약 max 값이 지정되지 않았다면 이 값은 1.0보다 작아야 함.

max
- 작업이 완료되려면 얼마나 많은 작업을 해야하는지 부동 소수점으로 표현
- 이 값은 0보다 커야 함.

## `<meter>` - 값이 차지하는 크기
- `<meter>` 태그는 progress와 결과 화면이 같음
하지만 progress와 달리 전체 크기 중에서 얼마나 차지하는지를 표현할 때 사용함.

작업이 진행된다는 의미보다는

하드 디스크 용량 중 얼마나 차지하는지
전체 유권자 중에서 몇 명이 투표했는지 -> 투표율 과 같이
지정된 범위 내에서 해당 값이 어느 정도 차지하는 지를 표현함.

| 속성 | 설명 |
| --- | --- |
| min, max | 범위의 최솟값 최댓값을 나타냄 / 값을 정하지 않으면 0과 1로 간주 |
| value | 범위 내에서 차지하는 값을 나타냄 |
| low | "이 정도면 낮다."라고 할 정도의 값을 지정 |
| high | "이 정도면 높다." 라고 할 정도의 값을 지정 |
| optimum | "이 정도면 적당하다."라고 할 정도의 범위를 지정 |

- optimum 값이 high 값보다 크다면 value 값이 클수록 좋음
- optimum 값이 low 값보다 작다면 value 값이 작을수록 좋음

