# 플렉스 박스 항목 배치를 위한 속성들

## justify-content - 주축(가로) 기준의 배치 방법 지정하기

**기본형** `justify-content: flex-start | flex-end | center | space-betweem | space-around`

| 속성 값 | 설명 |
|--------|------|
| flex-start | 주축의 시작점을 기준으로 배치 |
| flex-end | 주축의 끝점을 기준으로 배치 |
| center | 주축의 중앙을 기준으로 배치 |
| space-betweem | 첫 번째 플렉스 항목과 마지막 플레스 항목은 시작점과 끝점에 배치 후 **중앙 항목들은 같은 간격**으로 배치 |
| space-around | **모든 플렉스 항목들을 같은 간격**으로 배치 |

## align-items, align-self - 교차축(세로) 기준의 배치 방법 지정하기

**기본형** `align-items : stretch | flex-start | flex-end | center | baseline`

| 속성 값 | 설명 |
|--------|------|
| stretch | 플렉스 항목을 확장해 **교차축을 꽉 채움** (기본값) |
| flex-start | 교차축의 **시작점**을 기준으로 배치 |
| flex-end | 교차축의 **끝점**을 기준으로 배치 |
| center | 교차축의 **중앙**을 기준으로 배치 |
| baseline | 시작점과 **글자 기준선**이 **가장 먼 플렉스 항목**을 시작점에 배치 / 그 글자의 기준선과 다른 항목의 기준선을 맞추어 배치 |

baseline -> 플렉스 박스 안에 있는 텍스트의 기준선을 기준으로 정렬함.

baseline 예시 [바로가기](./baseline.html)

-----

**기본형** `align-self: auto | stretch | flex-start | flex-end | center | baseline`

auto : 플렉스 항목의 부모 속성 값을 상속받음

을 제외하고는 다 동일한 속성값

## align-content - 여러 줄일 때의 배치 방법 지정하기

**기본형** `align-content: flex-start | flex-end | center | space-between | space-around`
