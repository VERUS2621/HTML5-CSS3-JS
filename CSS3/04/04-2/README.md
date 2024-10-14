# 테두리 관련 속성

**기본형** `border-styleL none | hidden | dashed | dotted | double | groove | inset | outset | ridge | solid`

| 속성 값 | 설명 |
| ---- | ---- |
| none | 나타나지 않음(기본값) |
| hidden | 없음 / border-collapse:sollapse일 경우, 다른 테두리도 표시되지 않음 |
| dashed |  짦은 선(직선으로 된 점) |
| dotted | 테두리 점선 |
| double | 이중선(겹선) / border-width로 두 선 사이 간격 조절 |
| groove | 창에 조각 / 홈이 파인 듯 입체적 |
| inset | border-collapse에서 separate : 창에 박혀 있는 것 처럼 / collapse : groove와 동일 |
| outset | separate : 테두리가 창에서 튀어 나온 것 처럼 / collapse : ridge와 동일 |
| ridge | 테두리를 창에서 튀어나온 것처럼 표시 |
| solid | 테두리를 실선 |

## border-width - 테두리 두께

**기본형** `border-(top/right/left/bottom/)-width: <크기> | thin | medium | thick`

## border-color - 테두리  색상

**기본형** `border-(top/right/left/bottom/)-color: <색상>`

## border 테두리 스타일 묶어 지정

**기본형** `border-(top/right/left/bottom/)-color: <두께> <색상> <스타일>`

## border-radius - 박스 모서리 둥글게

**기본형** `border-[top-(right/left) | bottom-(right/left)]-radius: <크기> | <백분율>`

타원 형태로 둥글게 만들기

`border-[top-(right/left) | bottom-(right/left)]-radius: <가로 크기> <세로 크기>`

## box-shadow - 선택한 요소에 그림자 효과

**기본형** 
```css
box-shadow : nonw | <그림자 값> [, <그림자 값>]*;
<그림자 값> = <수평 거리> <수직 거리> <흐림 정도>
<번짐 정도> <색상> inset
```

수평, 수직 거리 -> 양수는 오른쪽 / 음수는 왼쪽 필수 속성
흐림 -> 음수 X
inset - 키워드 표시하면 안쪽 그림자로 그림 / 필요한 경우에만 사용하는 옵션 값


