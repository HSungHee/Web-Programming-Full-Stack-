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


# 2.3 HTML Structure Design

웹페이지를 만드는 것은 문서의 구조를 잡는 것과 같습니다.

제목, 단락 등이 있는 것과 같습니다.

그런 관점으로 웹사이트의 문서구조를 만드는 것이 가장 먼저 할 일 입니다.

## HTML 구조설계

구조화 설계는 마치 문서를 쓴다고 생각하면 쉽습니다.

현업에서는 Presentation 문서형태의 기획서나 디자인 파일을 받아서 그것을 기반으로 HTML개발을 시작합니다.

즉 어떠한 화면을 보면서 그대로 구현하는 것이죠. 

그 화면을 보면서 구조를 분석해야 합니다. 

먼저 영역을 나눠서 상단/본문/네비게이션 이런 식으로 큰 부분부터 분리합니다.

그 뒤에 각 영역 안에 내용의 구조를 잡는 것이 일반적입니다.

각 영역 안의 내용 역시 여러 가지 형태일 겁니다.

목록을 나타내거나, 이미지를 나타내거나, 문단을 나타낼 수 있습니다.

이때마다 적절한 태그를 쓰면 됩니다.

그러면서 영역 안에 또 다른 영역이 있다면 점점 안으로 좁혀가면서 HTML tag를 사용하면서 완성해나가는 겁니다.

이때 CSS코드를 같이 구현하지 않고 HTML로 먼저 문서의 구조를 잡아나가는 것이 개발 단계에서 유리합니다.

그래야 전체 뼈대가 튼튼하게 되는 것이죠.

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
  <header>
  <h1>Company Name</h1>
  <img src="..." alt="logo">
  </header>
  
  <div>  <!-- section태그를 사용했었지만, 별 의미없는 container에는 section태그가 적절하지 않아서 수정합니다 -->
    <nav><ul>
      <li>Home</li>
      <li>Home</li>
      <li>About</li>
      <li>Map</li>
      </ul></nav>
    
    <div>  
      <button></button>
      <div><img src="dd" alt=""></div>
      <div><img src="dd" alt=""></div>
      <div><img src="dd" alt=""></div>
      <button></button>
    </div>
    <div>
      <ul>
        <li>
          <h3>What we do</h3>
          <div>Lorem ipsum dolor sit amet, consectetur adipisicing</div>
        </li>
        <li>
          <h3>What we do</h3>
          <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Similique accusamus, corporis, dolorum fugiat tenetur porro. Aspernatur commodi, ea suscipit non? Molestiae nulla explicabo debitis provident nostrum dolorem minima reiciendis suscipit?</div>
        </li>
        <li>
          <h3>What we do</h3>
          <div>Lorem ipsum dolor sit amet, consectetur adipisicing</div>
        </li>
      </ul>
    </div>
  </div>
  <footer>
    <span>Copyright @codesquad</span>
  </footer>
```

lorem... 은 별의미없는 글자들을 채우기 위해서 보통 사용하는 문장입니다. 

# 2.4 Class와 ID 속성

## ID

고유한 속성으로 한 HTML 문서에 하나만 사용 가능합니다.
고유한 ID 값이 있으면 하나하나에 특별한 제어를 할 수 있으며 검색에도 용이합니다.


## Class

하나의 HTML문서 안에 중복해서 사용 가능합니다.
하나의 태그에 여러 개의 다른 class 이름을 공백을 기준으로 나열할 수가 있습니다.
홈페이지 전체적인 스타일을 일관성 있게 지정하기 위해서는 class의 사용이 필수적입니다.
이렇게 구분할 수 있지만, 많은 회사마다 개발단계에서 어떠한 약속(convention)을 만들어서 자신들만의 규칙을 사용하기도 합니다.

예를 들어 ID사용을 금하는 곳도 있습니다.

class로만 사용하는 곳도 있습니다.

그건 팀이 결정하기 나름입니다.

하지만 반대의 경우 즉 모든 것을 id만으로 사용하는 것은 없겠죠?  

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
  <header>
  <h1>Company Name</h1>
  <img src="..." alt="logo">
  </header>
  
  <section id="nav-section">
    <nav><ul>
      <li>Home</li>
      <li>Home</li>
      <li>About</li>
      <li>Map</li>
      </ul>
    </nav>
    
    <section id="roll-section">
      <button></button>
      <div><img src="dd" alt=""></div>
      <div><img src="dd" alt=""></div>
      <div><img src="dd" alt=""></div>
      <button></button>
    </section>
    <section>
      <ul>
        <li class="our_diescriptipn">
          <h3>What we do</h3>
          <div>Lorem ipsum dolor sit amet, consectetur adipisicing</div>
        </li>
        <li class="our_diescriptipn">
          <h3>What we do</h3>
          <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Similique accusamus, corporis, dolorum fugiat tenetur porro. Aspernatur commodi, ea suscipit non? Molestiae nulla explicabo debitis provident nostrum dolorem minima reiciendis suscipit?</div>
        </li>
        <li class="our_diescriptipn">
          <h3>What we do</h3>
          <div>Lorem ipsum dolor sit amet, consectetur adipisicing</div>
        </li>
      </ul>
    </section>
  </section>
  <footer>
    <span>Copyright @codesquad</span>
  </footer>
</body>
```
