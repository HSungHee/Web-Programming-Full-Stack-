# HTML

===============================

# 2.1 HTML tags

HTML 태그는 많은 종류를 가지고 있고 각각의 쓰임새에 대한 정확한 의미가 있습니다.
'각각의 의미를 지닌다'는 것을 'Semantic한 태그' 혹은 'Semantic하다'라는 표현을 하곤 합니다.

## HTML tag의 종류

태그는 그 의미에 맞춰서 사용해야 합니다.

* 링크
* 이미지
* 목록
* 제목

anchor 태그, img 태그, ul/li 태그, heading 태그, p 태그 등이 자주 사용됩니다.

그 밖에 가장 많이 사용하는 div태그가 있습니다.

div 태그는 block 엘리먼트라고 하는데 일반적인 영역을 표현할 때 가장 많이 사용합니다. 

많은 태그를 모두 외울 필요는 없으며, 필요한 태그를 찾아서 적절한 의미에 맞는 태그를 사용하는 것이 중요합니다.


### 실습코드
```
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>JS Bin</title>
</head>
<body>
  <div>
    <h1>반갑습니다</h1>
    여기 여러분들이 좋아하는 과일이 있어요.
    <ul>
      <li><a href="http://www.apple.com">사과</a></li>
      <li>사과</li>
      <li>메론</li>
      <li>귤</li>
    </ul>
  </div>
</body>
</html>
```

### 참고자료
HTML Element Reference - https://www.w3schools.com/tags/ref_byfunc.asp


# 2.2 HTML Layout tags

## 레이아웃을 위한 태그

레이아웃을 구성하는 태그도 역시 그 의미에 맞춰서 사용됩니다. 

* header
* section
* nav
* footer
* aside

html태그는 레이아웃을 할 때도 그 의미에 맞는 것을 찾아 사용해야 검색도 더 잘되고, 가독성 있는 코드를 만들 수 있게 됩니다. 

### 실습코드
```
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>JS Bin</title>
</head>
<body>
  <header>header</header>
  <div id="container"> 
    <nav><ul>
      <li>home</li>
      <li>news</li>
      <li>sports</li>
    </ul></nav>
    <aside><ul>
      <li>logout</li>
      <li>weather</li>
      <li>luck</li>
    </ul></aside>
  </div>
  <footer>footer</footer>
</body>
</html>
```


### 참고자료
Standard HTML5 Semantic Layout - https://gist.github.com/thomd/9220049
