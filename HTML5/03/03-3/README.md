# `<input>` 태그의 다양한 속성

## autofocus - 입력 커서 표시하기

이전에는 이 기능을 구현하기 위해서는 자바스크립으를 이용해야했지만 
HTML5에서는 autofocus 속성을 이용해서 쉽게 해결할 수 있다.

[예제](./example/autofocus.html)

## placeholder - 힌트표시하기

사용자가 텍스트를 입력할 때 도움이 되도록 입력란에는 적당한 힌트 내용이 표시하고 있다가
그 필드를 클릭하면 내용이 사라지도록 만들 수 있다.

- 앞에 텍스트를 사용하지 않고 어떤 내용을 입력해야 할지 알려줄 수 있음

[예제](./example/placeholder.html)

## readonly - 읽기 전용 필드 만들기

간단히 readonly라고 쓰거나
```
readonly="readonly" 라고 써도
readonly="true" 인식 됨.
```

## required - 필수 필드 지정하기.

내용을 폼에 입력한 후 submit 버튼을 클릭하면 폼을 서버로 전송하는데 
이때 필수 필드에 필요한 내용이 모두 채워져 있는지 검사해야 함.

required 속성은 boolean value임 따라서
간단히 required라고 쓰거나
required="required" 라고 써도 됨.

## 기타

| 속성 | 설명 | 사용할 타입 |
| ---- | ---- | ---- |
| min | 숫자 최솟값 |
| max | 숫자 최댓값 |
| step | 숫자의 일정한 간격 설정 |
| size | 텍스트 길이 |
| minlength | 텍스트 최소 길이 |
| maxlength | 텍스트 최대 길이 |
| formaction | 실행할 프로그램 연결 | type = "submit or image" |
| formenctype | 서버로 폼을 전송했을 때 어떤 방식으로 해석할 지 | type = "submit or image" |
| formmethod | 서버로 폼을 전송하는 방식(get, post 등) <form> 태그 안에서 지정한 방식 있어도 무시 |
| formnovalidate | <input> 태그에서도 속성을 이용해 유효성 검사 가능 |
| formtarget | 폼 데이터를 서버로 전송한 후 서버의 응답을 어디에 표시할 것인지 타깃 설정 |
| height, width | 이미지의 너비와 높이 지정 | type ="image" |
| list | `<datalist>`에 미리 정의해 놓은 옵션 값을 <input> 안에 나열해 보여줌
| multiple | 두 개 이상의 값을 입력, `<input>` 태그 안 속성 이름만 표시 | type = "email or file" |

`<form>` 태그안에 novalidate 라는 속성이 있어 서버로 전송할 때 폼 데이터가 유효한지 여부를 표시할 수 있으나
formnovalidate 속성을 이용해 `<input>` 태그에서도 유효성 검사 가능