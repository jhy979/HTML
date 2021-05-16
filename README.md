# HTML
### html 문법에 대하여 알아봅시다.

## 1. 빈 태그
```html 
<div> </div>
```
- 원래 이게 기본인데
```html
<meta charset="UTF-8">
<link rel="stylesheet" href="./main.css">
```
- 같이 끝 태그가 없는 경우를 빈 태그라고 합니다.
```
<태그> vs <태그/>
```
<태그> : HTML 1/2/3/4/5 버젼 <br/>
<태그/> : XHTML, HTML5 버젼 (더 안전해요~)

## 2. attribute 기능의 확장
> <태그 속성="값"> 내용 </태그>
```html
<img src= "~~~~" alt="nope"/>
```
- 위의 img태그 같은 경우에는 src, alt같은 것들이 attribute
## 3. 글자(inline)와 상자(block)
- 요소가 화면에 출력되는 특성<br>
> **inline : 글자를 만들기 위한 요소들**
```html
<span>Hello</span>
<span>World</span>

```
- 대표적 인라인 요소
- 콘텐츠 영역을 설정하는 용도일뿐, 아무 의미 없어요.
- 인라인 요소는 ***글자 취급***이라서 위의 Hello World는 띄어쓰기 되어서 출력됩니다. 
- 줄바꿈을 안하면 띄어쓰기 없이 HelloWorld 이런 식으로 출렵됩니다.
- **기로, 세로가 최대한 줄어들려고 하는 특성이 있어요.**
```html
<span style= "margin :20px 20px">Hello</span>
<span style= "padding :20px 20px">Hello</span>
```
- inline(글자 요소)는 위아래 여백은 안 되고 좌우만 됩니다.<br><br>
**❌불가능👇**
```html
<span><div></div></span>
```

- inline(글자 요소) 안에는 block(블록 요소)을 넣을 수 없습니다.
> **block : 레이아웃을 만들기 위한 요소들**
```html
<div>Hello</div>
<div>World</div>
```
- 위에서 아래로 수직으로 쌓여서 Hello \n World 이런식으로 출력됩니다.
-  **기로는 최대한 늘어나려고 하는 특성이 있어요, 세로는 줄어들려고 해요.**
-  inline은 안되지만, block 요소들은 width, height를 지정해줄 수 있어요.
-  inline은 안되지만, 상하 여백도 가능합니다.<br>
 ***👉 즉, block요소들이 시각적으로 제어하기 더 쉽습니다.***
 
 ## 4. 핵심 요소 정리
 |핵심 요소|기능|요소|
 |:---:|:---:|:---:|
 |`<div>`|구분 위해 사용|block요소|
 |`<h1>`|제목 1~6까지 있음|block요소|
 |`<p>`|paragraph, 문장 구분|block요소|
 |`<img>`|이미지 삽입<br>`src="~"` `alt="wait"`|inline요소|
 |`<ul>`|unordered list <br>`<li>`를 무조건 같이 써야함|block요소|
 |`<ol>`|ordered list|block요소|
 |`<a>`|ahchor,링크<br>`href` `target="_blank"`|inline요소|
 |`<span>`|No 의미, just 구분|inline요소|
 |`<br>`|줄바꿈|inline요소|
 |`<input>`|데이터 입력 받기<br> `type="text,checkbox,radio(택1),"` `value="미리 입력된 값"`<br> `placeholder="이름을입력하세요"` `disabled `|inline+block요소|
 |`<label>`|라벨링(묶음) 가능한 요소의 제목|inline요소|
 |`<table>`|표<br> 행 : `<tr>` <br>열: `<td>`|block|
