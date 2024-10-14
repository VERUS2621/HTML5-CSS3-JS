# 배경 색과 배경 이미지

## background-color - 배경 색

**기본형** `background-color: <색상>`
아까 앞에서 설명한 16진수 rgb 또는 색상 이름 등을 지정해서 사용 함.

ex
```css
background-color:#00ff00;
background-color:rgb(0,255,0);
background-color:green;
```

background-color 값은 상속되지 않음

모든 웹 문서 요소의 배경은 투명하기 때문에 지정하면 비쳐보일 뿐임.
따라서 -> 각 요소(표나 목록) 등에 배경 요소를 지정하고 싶으면 각 요소에 직접 background-color 속성을 설정해야 함.

## background-clip - 배경 적용 범위 조절하기

**기본형** `background-clip: border-box | padding-box | content-box`

| 속성 값 | 설명 |
| ---- | ---- |
| border-box | 박스 모델의 가장 외곽인 테두리(border)까지 적용함 |
| padding-box | 박스 모델의 테두리를 뺀 패딩(padding) 범위 까지 적용함. |
| content-box | 박스 모델에서 내용 부분에만 적용 |

![border_padding](./border_padding.png)

## background-image - 웹 요소에 배경 이미지 넣기

**기본형** `background-image: url(파일 경로)`

문서 전체의 배경 이미지 지정 -> `<body>`
특정 영역 -> 클래스 선택자, id 선택자

파일 경로는 -> 현재 웹 문서를 기준으로 상대 경로
           -> 'http://'로 시작하는 절대 경로 사용 가능
작은따옴표(또는 큰따옴표) 를 붙여도, 안붙여도 상관 X

배경 이미지는 여러 개 사용 가능 -> 첫 번째 이미지부터 순서대로 표시
채우려는 요소크기 > 이미지 라면 해당 요소를 가득 채울 정도로 **가로와 세로 반복**

## background-repeat - 배경 이미지 반복 방법 지정

**기본형** `background-repeat: repeat | repeat-x | repeat-y | no-repeat`

repeat : 가득 찰 때까지 가로와 세로를 반복 (기본값)
repeat-x : 배경 이미지를 가로로 반복
repeat-y : 배경 이미지를 세로로 반복
no-repeat : 배경 이미지를 한 번만 표시하고 반복하지 않음

## background-size - 배경 이미지 크기 조절

**기본형** `background-size : auto | contain | cover | <크기 값> | <백분율>`
| 속성 값 | 설명 |
| ---- | ---- |
| auto | 원래 배경 이미지 크기 표시(기본값) |
| contain | 요소 안에 다 들어오도록 이미지를 확대/축소 함. |
| cover | 요소를 모두 덮도록 이미지를 확대/축소 함. |
| <크기 값> | 너비 값과 높이값을 지정 / 너비 값만 지정할 경우, 원래 배경 이미지 크기를 기준으로 축소/확대 비율을 자동으로 계산해 높이 지정 |
| <백분율> | 배경 이미지가 들어갈 요소의 크기를 기준으로 백분율 값을 지정 그 크기에 맞게 배경 이미지를 축소/확대 |

## background-position - 배경 이미지 위치 조절

**기본형**
```css
background-position: <수평 위치> <수직 위치>;

수평 위치 : left | center | right | <백분율> | <길이 값>
수직 위치 : top | center | bottom | <백분율> | <길이 값>
```
백분율 -> 요소를 기준으로

## background-origin - 배경 이미지 배치할 기준 조절하기

**기본형** `background-origin: border-box | padding-box | content-box`

| 속성 값 | 설명 |
| ---- | ---- |
| border-box | 박스 모델의 가장 외곽인 테두리(border)가 기준 |
| padding-box | 박스 모델의 테두리를 뺀 패딩(padding)이 기준 |
| content-box | 박스 모델에서 내용 부분이 기준 |

## background-attachment - 배경 이미지 고정

**기본형** `background-attachment : scroll | fixed`

scroll : 화면 스크롤과 함께 배경 이미지도 스크롤 (기본값)
fixed : 화면이 스크롤되더라도 이미지는 고정

## background - 속성 하나로 배경 이미지 제어하기

예시
`background:url(이미지경로) no-repeat fixed right bottom`

별다른 속성 값을 지정하지 않으면 **기본값**
| 속성 값 | 설명 |
| ---- | ---- |
| background-image | url(이미지경로) |
| background-repeat | no-repeat |
| background-attachment | fixed |
| background-position | right bottom |
| background-clip | border-box |
| background-origin | padding-box |
| background-size | auto |