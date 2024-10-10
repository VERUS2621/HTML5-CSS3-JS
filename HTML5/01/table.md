## 표 만들기 태그

### `<table>, <tr>(row), <td>(col), <th>(head)` 태그 
- 기본적인 표 만들기 

```html
<!-- 기본적인 형태 -->
 <table>
    <tr> <!--행-->
        <td> 내용 </td> <!--열-->
        <td> 내용 </td>
        ...
    </tr>
    ...
</table>
```

[2*3 표 만들기](./2x3.html)

#### rowspan, colspan 속성 - 행 또는 열 합치기

여러 열이나 행을 합치는 것은   
`<td>, <th>` 태그에 `colspan, rowspan` 속성을 이용해서 합칠 셀에 개수를 지정하면 됨   

```html
<td colspan="합칠 셀의 개수"> 내용 </td>
<th colspan="합칠 셀의 개수"> 내용 </th>

<td rowspan="합칠 셀의 개수"> 내용 </td>
<th rowspan="합칠 셀의 개수"> 내용 </th>
```
[일부 셀 합치기 예제](./Merge%20cells.html)

#### `<caption>, <figcaption>` - 표에 제목 붙이기
| 표기 | 특징 |
| --- | --- |
|`<caption> 표 제목 </caption>`| 표의 위쪽 중앙에 표시 됨 |
|`<figcaption> 표 제목 </figcaption>`| 표의 앞이나 뒤 |

`<figcaption>` -> `<figure>` 태그로 감싼 후 `<figcaption>` 태그를 이용해 제목이나 설명 글을 입력

`<table>` 앞에 / 표 위에 제목 표시   
`</table>` 다음에 / 표 아래에 제목 표시   

`<caption>` 예시
```html
<table>
    <caption>
        <strong>Modern Browser</strong>
        <p>국내에서 자주 사용하는 모던 브라우저</p>
    </caption>
    ...
<table>
```

`<figcaption>` 예시
```html
<figure>
    <figcaption>
        <p>국내에서 자주 사용하는 <b>모던 브라우저</b></p>
    </figcaption>
    <table>
        ...
    </table>
</figure>
```

----

##### aria-describedby 속성 - 표에 대한 설명 제공하기

화면 낭독기에서 표를 읽어줄 때 도움이 되도록 표 설명을 별도의 문장으로 작성한 후 <table> 태그 안에   
aria-describedby 속성을 추가해 연결하면 표를 이해하는데 도움이 됨

예제
```html
<p id="summary">다음 표는 HTML5 를 지원하는 모던(Modern Browser)를 정리한 것입니다. 최신 버진
일수록 HTML5를 좀더 많이 지원하기 때문에 최신 버전을 다운로드 하는 것이 좋습니다. </p>
    <table aria-descirbedby="summary">
        ...
    </table>
```

----

#### `<thead>, <tbody>, <tfoot>` - 표 구조 정의하기

일부 표에서는 제목이 표시된 셀과 자료가 표시된 셀 외에도 표 아래쪽에 합계나 요약 내용을 표시하기도 함.   
이런 표의 각 셀은 제목이 있는 부분과 실제 내용이 있는 본문 그리고 요약 부분이 있는 부분으로 표의 구조를 나누어 놓는 것이 좋음   
이때 사용하는 태그들은 table의 t와 합쳐져 제목 부분(head), 본문(body), 요약 부분(foot)이란 말이 합쳐져 `<thead>, <tbody>, <tfoot>`이다.   

```html
<thead>
    <tr> ... </tr>
</thead>
<tbody>
    <tr> ... </tr>
</tbody>
<tfoot>
    <tr> ... </tr>
<tfoot>
```
`<tfoot>`과 `<tbody>` 위치는 바뀌어도 상관 없음
HTML4에서는 `<tfoot>` 태그를 `<tbody>` 앞에 사용하는 것을 기본으로 하고 있음(이를 지키지 않으면 오류 발생 하기도)   

이렇게 표의 구조를 정의하면 시각장애인들도 화면 낭독기를 통해 표의 구조를 쉽게 이해할 수 있습니다.   
화면을 보여주지 않더라도 기기에서 표를 제대로 이해할 수 있는거죠.   
이뿐만 아니라 CSS를 통해 표의 제목 부분과 요약 부분, 본문에 각각 다른 스타일을 적용할 수 있습니다.   

또한, 본문이 길어 한 화면을 넘어갈 경우,    
자바스크립트를 이용해 제목부분(`<thead>`)과 요약부분(`<tfoot>`)은 표 위 아래에 고정하고 본문만 스크롤 되도록 할 수 있음   
이 방법은 내용이 긴 표를 인쇄할 때 각 장마다 표의 제목과 요약부분이 자동으로 인쇄되므로 편리하게 이용할 수 있음.   

----
#### `<col>, <colgroup>` 태그 - 여러 열 묶어 스타일 지정하기

```html
<col>

or

<colgroup>
    <col>
    ...
</colgroup>
```
`<col>` 태그는 한 열에 있는 모든 셀에 같은 스타일을 적용할 때 사용 / 닫는 태그 없음   
`<span>, <colgroup>` 태그를 이용해서 몇 개를 함께 묶을 수 있음   
**`<col>, <colgroup>`  태그 같은 경우 `<tr>, <td>` 전에 사용해야 함**.   

[표에서 열끼리 묶기](./colgroup.html)   

