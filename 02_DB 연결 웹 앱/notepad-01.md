
# 1. JavaScript - FE
========================================

# 1.1 자바스크립트

## 자바스크립트 변수-연산자-타입

### 자바스크립트의 버전

자바스크립트 버전은 ECMAScript(줄여서ES)의 버전에 따라서 결정되고, 이를 자바스크립트 실행 엔진이 반영합니다.
ES5, ES6(ES2015).. 이런 식으로 버전을 일컫습니다.
2018년을 중심으로 ES6를 지원하는 브라우저가 많아서 몇 년간 ES6 문법이 표준으로 쓰이고 있습니다.
ES6는 ES5문법을 포함하고 있어 하위호환성 문제가 없습니다.
다만 feature별로 지원하지 않는 브라우저가 있을 수 있어 조심해야 합니다.

### 변수

변수는 var, let, const 로 선언할 수 있습니다.
어떤 것을 사용하는가에 의해서 scope, 즉 변수의 유효범위가 달라집니다.
ES6이전까지는 var를 사용해서 변수를 선언할 수 있습니다.

```
var a = 2;
var a = "aaa";
var a = 'aaa';
var a = true;
var a = [];
var a = {};
var a = undefined;
```

### 연산자

연산자 우선순위를 표현하기 위해서는 ()를 사용하면 됩니다. 
수학연산자는 +,-,*,/,%(나머지) 등이 있습니다.
그리고 논리 연산자, 관계연산자, 삼항연산자도 있습니다. 

```
//or 연산자 활용
const name = "crong";
const result = name || "codesquad";
console.log(result);
var name = "";
var result = name || "codesquad";
console.log(result);
```

### 연산자 - 삼항연산자

간단한 비교와 값 할당은 삼항연산자를 사용할 수 있습니다.

```
const data = 11;
const result = (data > 10) ? "ok" : "fail";
console.log(result);
```

### 연산자 - 비교연산자

비교는 == 보다는 ===를 사용한다.
==로 인한 다양한 오류 상황이 있는데 아래 결과를 참고해봅시다. 
=== 정확한 타입까지 비교한다.

```
0 == false;
"" == false;
null == false;
0 == "0";
null==undefined;
```

### 자바스크립트의 Type

자바스크립트 타입에는 다양한 것이 존재합니다.

```
> undefined, null, boolean, number, string, object, function, array, Date, RegExp
```

타입은 선언할 때가 아니고, 실행타임에 결정됩니다.
함수안에서의 파라미터나 변수는 실행될 때 그 타입이 결정됩니다. 
타입을 체크하는 또렷한 방법은 없습니다.
정확하게는 toString.call 함수를 이용해서 그 결과를 매칭하곤 하는데, 문자, 숫자와 같은 자바스크립트 기본 타입은 'typeof' 키워드를 사용해서 체크할 수 있습니다. 
배열은 타입을 체크하는 isArray함수가 표준으로 생겼습니다.
IE와 같은 구 브라우저를 사용해야 한다면 지원범위를 살펴보고 사용해야 합니다.

