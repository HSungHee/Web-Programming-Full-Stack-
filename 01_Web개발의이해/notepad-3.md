# 3. CSS - FE
========================================

# 3.1 CSS 

## CSS 구성
```
span {
  color : red;
}
```

* span : selector (선택자)
* color : property
* red: value

### style을 HTML페이지에 적용하는 3가지 방법

1. inline

HTML태그 안에다가 적용합니다.

다른 CSS파일에 적용한 것 보다 가장 먼저 적용합니다.

```
<p style="border:1px solid gray;color:red;font-size:2em;">
```

2. internal

style 태그로 지정합니다.

구조와 스타일이 섞이게 되므로 유지보수가 어렵습니다.

별도의 CSS파일을 관리하지 않아도 되며 서버에 CSS파일을 부르기 위해 별도의 브라우저가 요청을 보낼 필요가 없습니다.

```
<head>
<style>
p  {
  font-size : 2em;
  border:1px solid gray;
  color: red;
}
</style>
```

3. external

외부파일(.css)로 지정하는 방식입니다.

CSS 코드가 아주 짧지 않다면 가급적 이 방법으로 구현하는 것이 가장 좋습니다.

현업에서는 여러개의 CSS 파일로 분리하고 이를 합쳐서 서비스에서 사용하기도 합니다.

internal 코드와 같은 css코드를 구현하고, style.css와 같은 별도 파일로 만듭니다. 

이후에 아래처럼 link태그로 추가하면 됩니다.

```
<html>
	<head>
		<link rel="stylesheet" href="style.css">
	</head>
	<body>
		<div>
			<p>
				<ul>
					<li></li>
					<li></li>
					<li></li>
					<li></li>
				</ul>
			</p>
		</div>
	</body>
</html>
```

4. 우선순위 

inline은 별도의 우선순위를 갖지만, internal 과 external은 우선순위가 동등합니다. 따라서 겹치는 선언이 있을 경우 나중에 선언된 속성이 반영됩니다.

### 참고자료
Difference Between Inline, External and Internal CSS Styles - https://www.hostinger.com/tutorials/difference-between-inline-external-and-internal-css


# 3.2 상속과 우선순위 결정

상위에서 적용한 스타일은 하위에도 반영됩니다.

이로 인해 여러 단계로 중첩된 엘리먼트마다 매번 같은 색상과 글자 크기를 부여하지 않아도 됩니다.

하지만 모든 CSS 속성이 이런 특징을 갖게 되면, 몇 가지 문제가 생깁니다.

예를 들어 width 속성이 상속되면 하위 엘리먼트가 모든 같은 크기의 넓잇값을 가질 수 있습니다.

이런 것은 원하는 것이 아니죠.

그래서 box-model이라고 불리는 속성들(width, height, margin, padding, border)과 같이 크기와 배치 관련된 속성들은 하위엘리먼트로 상속이 되지 않습니다.

이렇게 CSS는 꽤 똑똑한 방식으로 동작합니다.  

아직 혼란스러운 부분이 있다면, 여러분들이 중첩된 엘리먼트를 만들고, CSS 속성을 부여하면서 이 특징을 잘 이해해보면 좋습니다.

```
<head>
<style>div { color:red; }</style>
<link rel="stylesheet" href="css.css">
</head>
```
만약 css.css에서 div color를 blue로 주었다면, 뒤에 선언된 external방식의 css내용이 반영됩니다. 따라서 blue색깔로 나오겠죠. 

즉 internal과 external은 같은 우선순위로 결정된다고 아셔야 합니다.

CSS는 여러가지 스타일정보를 기반으로 최종적으로 '경쟁'에 의해서 적절한 스타일이 반영된다는 점을 잘 기억해야 합니다.

```
<div id="a" class="b">
	text....
</div>
```

```
#a{
 color : red;
}

.b{
 color : blue;
}

div{
 color : green;
}
```
위 코드에서 id, class, 엘리먼트 순으로 우선순위를 가집니다.

id는 클래스보다 우선되고 클래스는 엘리먼트보다 우선됩니다.

위 코드에서는 id인 a의 색상이 적용되게 됩니다.

CSS의 이런 성질을 캐스캐이딩이라고 합니다.


## 선언방식에 따른 차이

같은 선택자(selector)라면 나중에 선언한 것이 반영됩니다.

선택자의 표현이 구체적인 것이 있다면 먼저 적용됩니다.

body > span (O)
span (X)

## ID > CLASS > ELEMENT 순으로 반영

만약 h1태그가 div > p > h1 구조로 HTML으로 짜여있다고 가정하면, 아래에 색깔 중 h1이 가진 색깔은 어떤 것일까요?

여러분들이 실험을 통해서 그 결과를 확인해보세요.

jsbin과 유사한 사이트 하나 더 알려드릴게요.

이번에는 codepen.io 라는 사이트를 이용해서 테스트해보세요.

### 참고자료
Specificity - https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity


# 3.3 CSS Selector
특정 엘리먼트에 스타일을 적용하기 위해서는 해당 엘리먼트를 잘 찾아야 합니다.

특정 엘리먼트뿐 아니라 여러 개의 엘리먼트일 수도 있습니다.

엘리먼트를 쉽고 빠르게 찾을 수 있는 것이 CSS Selector 문법입니다. 

## CSS selector

HTML의 요소를 tag, id, html 태그 속성 등을 통해 쉽게 찾아주는 방법입니다.

element에 style 지정을 위한 3가지 기본 선택자

* tag로 지정하기
```
<style>
     span {
       color : red;
     }
</style>
```

* id로 지정하기
```
<style>
     #spantag {
       color : red;
     }
</style>

<body>
     <span id="spantag"> HELLO World! </span>
</body>
```

* class로 지정하기
```
<style>
     .spanClass {
     color : red
     }
</style>

<body>
     <span class="spanClass"> HELLO World! </span>
</body>
```

## CSS Selector의 다양한 활용
* id, class 요소 선택자와 함께 활용
```
#myid { color : red }
div.myclassname { color : red }
```

* 그룹 선택 (여러 개 셀렉터에 같은 style을 적용해야 한다면)
```
h1, span, div { color : red }
h1, span, div#id { color : red }
h1.span, div.classname { color : red }
```

* 요소 선택 (공백) : 자손요소
* 아래 모든 span태그에 red색상이 적용됨
```
<div id="jisu">
  <div>
    <span> span tag </span>
  </div>
  <span> span tag 2 </span>
</div>
```
```
#jisu span { color : red }
```

* 자식 선택 (>) : 자식은 바로 하위엘리먼트를 가리킵니다.
* 아래는 span tag 2만 red 색상이 적용됩니다.
```
<div id="jisu">
  <div>
    <span> span tag </span>
  </div>
  <span> span tag 2 </span>
</div>
```
```
#jisu > span { color : red }
```

* n번째 자식요소를 선택합니다. (nth-child)
* 첫번째 단락에 red 색상이 적용됩니다.
```
<div id="jisu">
  <h2>단락 선택</h2>
  <p>첫번째 단락입니다</p>
  <p>두번째 단락입니다</p>
  <p>세번째 단락입니다</p>
  <p>네번째 단락입니다</p>
</div>
```
```
#jisu > p:nth-child(2) { color : red }
```

### 참고자료
CSS Selectors Cheatsheet - https://gist.github.com/magicznyleszek/809a69dd05e1d5f12d01


# 3.4 CSS 기본 Style 변경하기

CSS style 적용은 글자색, 배경색 등이 가장 자주 사용되는 것들입니다.

이런 속성은 위치 값과 크기를 지정하는 것과 달리, 색상 위주로 값을 부여합니다.

색상 관련 값은 다양한 색을 일관된 방법으로 표현하기 위해 주로 16진수 표기법을 사용합니다.
 
## font 색상 변경

* color : red;
* color : rgba(255, 0, 0, 0.5);
* color : #ff0000;   //16진수 표기법으로 가장 많이 사용되는 방법이죠.

## font 사이즈 변경

* font-size : 16px;
* font-size : 1em;
 
## 배경색 

* background-color : #ff0;
* background-image, position, repeat 등의 속성이 있습니다.
* background : #0000ff url(“.../gif”) no-repeat center top; //한 줄로 정의도 가능
 

## 글씨체/글꼴

* font-family:"Gulim";
* font-family : monospace;

```
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>JS Bin</title>
  <style>
    body > div {
      font-size:16px;
      background-color: #ff0;
      font-family:"Gulim";
    }
    
    .myspan {
      color : #f00;
      font-size:2em;
    }
  </style>
</head>
<body>
  <div>
    <span class="myspan">my text is upper!</span>
  </div>
</body>
</html>
```

## 웹 폰트

웹폰트는 브라우저에서 기본으로 지원하지 않는 폰트를 웹으로부터 다운로드 받아 사용할 수 있는 방법입니다.

다양하고 예쁜 폰트들을 웹폰트로 사용할 수 있긴 하지만 다운로드를 받아야 한다는 단점이 있습니다.

다운로드 시간이 오래 걸리게 되면 화면에 노출되는 시간이 느려져 오히려 사용자에게 불편함을 느끼게 할 수 있는 것 입니다.

또한 다양한 해상도에서 깨지는 문제도 발생할 수 있습니다.

웹폰트는 수많은 종류가 있습니다.

대표적으로 구글 웹폰트가 있으며 최근에는 다양한 크기에서 품질을 유지하는 벡터 방식의 아이콘 웹폰트도 등장했습니다.

(unicode영역 중 Private Use Area (PUA) 영역을 활용해서 제작)

또한 웹폰트 방식말고, 기본 unicode를 사용해서 간단한 아이콘을 표현하는 것도 가능합니다.

아래 unicode를 사용한 HTML 코드를 참고하세요.

```
<div> 안녕하세요 &#x263a;</div> //☺  웹 화면에는 웃음 표시가 표현되는 코드입니다.
```

### 참고자료
bootstrap - https://getbootstrap.com/components/


# 3.5 Element가 배치되는 방법(CSS Layout)

### 참고자료

# 3.6 Float 기반 샘플 화면 레이아웃 구성

### 참고자료

# 디버깅 - HTML, CSS

### 참고자료

