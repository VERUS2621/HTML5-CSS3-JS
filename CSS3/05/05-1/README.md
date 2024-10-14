# CSS positioning 과 주요 속성

웹 문서에 박스 모델을 배치하는 것을 포지셔닝이라고 함.

## box-sizing 속성 - 박스 너비 기준 정하기

CSS width 속성은 콘텐츠 영역의 너비를 나타내기 때문에 해당 요소에 적용한 패딩이나 테두리 크기는 계산해서 배치해야 함.
이럴 떈 box-sizing 속성을 사용하면 콘텐츠 영역의 너비에 패딩과 테두리 크기까지 합쳐서 width 속성을 지정할 수 있음.

**기본형** `box-sizing: content-box | border-box`

content-box - width 속성 값을 콘텐츠 영역 너비 값으로 사용 (기본값)
border-box - width 속성 값을 콘텐츠 영역에 테두리까지 포함한 박스 모델 전체 너비 값으로 사용

## float - 왼쪽이나 오른쪽으로 배치하기

**기본값** `float: left | right | none`

## clear - float 속성 해제하기

**기본값** `clear: none | left | right | both`

float 속성을 일일이 기억하기 어렵다면 `clear:both` 을 이용하여 한꺼번에 해제하기도 함.

## position - 배치 방법 지정하기

**기본값** `position: static | relative | absolute | fixed`

static : 요소를 문서의 흐름에 맞추어 배치(기본값)
relative : 이전 요소에 자연스럽게 연결해 배치하되 위치를 지정할 수 있음
absolute : 원하는 위치에 지정해 배치
fixed : 지정한 위치에 고정해 배치 -> 화면에 요소가 잘릴 수도 있음 (브라우저 창 기준으로 배치)

top, left, bottom, right 속성을 사용 가능 O (static 제외) / 좌표 사용해 위치를 지정할 수 있음.

## visibility 속성 - 요소를 보이게 하거나 보이지 않게 하기

**기본형** `visibility: visible | hidden | collapse`

visible : 화면에 요소를 표시(기본값)
hidden : 화면에서 요소를 감춤(크기는 그대로 유지하기에 배치에 영향을 미침)
collapse : 표의 행, 열, 행 그룹, 열 그룹 등에서 지정하면 서로 겹치도록 조절. 그 외의 영역에서 사용하면 'hidden'처럼 처리

## z-index - 요소 쌓는 순서 정하기

**기본형** `z-index: <숫자>`

숫자가 작을수록 아래에 쌓이고, 클수록 작은 요소보다 위에 쌓임.
값을 명시하지 않을 경우 웹 문서에 맨 먼저 삽입하는 요소가 `z-index:1`을 가지며
그 후 삽입한느 요소는 `z-index`값이 점점 커짐.