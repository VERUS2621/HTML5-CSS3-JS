# 목록 스타일

## list-style-type - 목록의 불릿과 번호 스타일 지정하기

**기본형** `list-style-type : none | <순서 없는 목록의 불릿> | <순서 목록의 번호>`

### 순서 없는 목록에서 불릿 모양 바꾸기

| 속성 값 | 설명 |
| ---- | ---- |
| Disc (●) | 채운 원(기본값) |
| Circle (○) | 빈 원 |
| Square (■) | 채운 사각형 |
| none | 불릿 없애기 |

### 순서 목록에서 숫자 바꾸기

| 속성 값 | 설명 | 예시 |
| ---- | ---- | ---- |
| decimal | 1로 시작하는 십진수(기본값) | 1, 2, 3, 4 |
| decimal-leading-zero | 앞에 0이 붙는 십진수 | 01, 02, 03, 04 |
| lower-roman | 소문자 로마 숫자 | i, ii, iii, iv |
| upper-roman | 대문자 로마 숫자 | I, II, III, IV |
| lower-alpha 또는 lower-latin | 소문자 알파벳 | a, b, c, d |
| upper-alpha 또는 upper-latin | 대문자 알파벳 | A, B, C, D |
| armenian | 아르메니아 숫자 | ա, բ, գ, դ |
| georgian | 조지 왕조시대의 문자속성 | ა, ბ, გ, დ |

## list-style-image - 불릿 대신 이미지 넣기

**기본형** 
```css
list-style-image : <이미지> | none
<이미지> = url(이미지 파일 경로)
```
none : 이미지를 사용하지 않고 list-style-type 속성에서 지정한 형태로 표시(기본값)
<이미지> : url() 키워드 안에 이미지 파일 경로를 지정

## list-style-position - 목록에 들여 쓰는 효과

**기본형** `list-style-position : inside | outside`

inside : 불릿이나 숫자를 **안쪽**으로 들여 씀
-> 좀 더 안쪽으로 들여 써진 듯한 효과 / 문단들 사이의 목록을 더 쉽게 구분
outside : 기본 값으로 불릿이나 숫자를 밖으로 내어 씀(기본값)

## list-style 속성 - 목록 속성 한꺼번에 표시하기

font 속성과 비슷하게 list-style 속성으로 앞에서 설명한 list-style-type과 list-style-position, list-style-image 속성을 한꺼번에 표시할 수 있음

```css
ol {list-style-type:none;}
↓
ol {list-style:none;}
```

```css
ol {
    list-style-type:lower-alpha;
    list-style-position:inside;
}
↓
ol {
    list-style: lower-alpha, inside;
}
```
