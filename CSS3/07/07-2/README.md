# 변형과 관련된 속성

## `transform-origin` - 변형 기준점 설정하기
위 속성을 사용하면 축이 아닌 특정 지점을 변형의 기준으로 설정할 수 있음.
2차원, 3차원 변형 모두 사용 가능함.

**기본형** `transform-origin: <x축> <y축> <z축> | initial(브라우저 기본값) | inherit(상속);`

| 속성 값 | 설명 |
| ------ | ---- |
| <x축> | 원점 기준의 x 좌푯값으로 길이 값이나 <백분율>, left, center, right 중에서 사용할 수 있음 |
| <y축> | 원저 기준의 y 좌푯값으로 길이 값이나 <백분율>, top, center, bottom 중에서 사용할 수 있음 |
| <z축> | 원점 기준의 z 좌푯값으로 길이 값만 사용할 수 있음 |

## `perspective, perspective-origin` - 원근감 표현

**기본값**: `perspective <크기> | none(기본값);`

3차원 변형에서 사용하는 속성 
원래 위치에서 사용자가 있는 방향이나 반대 방향으로 잡아당기거나 밀어내 원근감을 갖게 함.

속성 값은 0보다 커야 하며 / 값이 클수록 사용자로부터 멀어짐.

**기본형** `perspective-origin : <x축 값> | <y축 값>`
위 속성을 사용하면 좀 더 높은 곳에서 원근을 조절하는 듯한 느낌을 받을 수 있음.
- 입체적으로 표현할 요소의 아랫부분(bottom) 위치를 지정할 수 있기 때문
 이 속성을 사용하려면 perspective 속성이 함께 지정되어 있어야 함.

| 속성 값 | 설명 |
| ------ | ---- |
| <x축 값> | 웹 요소가 x축에서 어디에 위치하는지를 지정함. 사용할 수 있는 값은 길이 값이나 백분율, left, right, center / 기본 값은 50% |
| <y축 값> | 웹 요소가 y축에서 어디에 위치하는지를 지정함. 사용할 수 있는 값은 길이 값이나 백분율, top, center, bottom / 기본 값은 50% |

## `transform-style` - 3D 변형 적용하기

**기본형** `transform-style: flat | preserve-3d`

flat : 하위 요소를 평면으로 처리
preserve-3d : 하위 요소들에 3D효과를 적용

## `backface-visibility - 요소의 뒷면 표시하기

**기본형** `backface-visibility : visible | hidden`

visible :  뒷면을 표시 (기본값)
hidden : 뒷면을 표시하지 않음


