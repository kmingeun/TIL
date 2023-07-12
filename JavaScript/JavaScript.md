# JavaScript (JS) 📖

<br>

## JavaScript란 무엇인가?


JavaScript는 웹을 위한 인터프리터 언어이자 객체기반의 스크립트 프로그래밍 언어입니다.

HTML의 특정 요소(들)을 선택하여 다양한 이벤트 (마우스 클릭, 키보드 입력 등)에 따라 어떤 동작을 하도록 기능을 넣을 수 있으며 발생하는 이벤트에 따라 HTML, CSS를 조작할 수도 있고 그 외에도 여러가지를 할 수 있습니다. 

쉽게 설명하면, HTML은 사람의 신체, CSS는 사람이 입는 옷, JS는 사람이 움직이는 행동으로 
JS를 쉽게 설명할 수 있습니다. 

___
<br>

## JavaScript 언어의 대표적인 특징
1. 자바스크립트는 객체 기반의 스크립트 언어입니다.

2. 자바스크립트는 동적이며, 타입을 명시할 필요가 없는 인터프리터 언어입니다.

3. 자바스크립트는 객체 지향형 프로그래밍과 함수형 프로그래밍을 모두 표현할 수 있습니다. 

___

<br>

## JavaScript의  Console

**console 객체**는 자바스크립트가 웹 브라우저의 디버깅 콘솔에 접근할 수 있도록 하는 객체입니다. **콘솔(console) 객체**를 이용하면 자바스크립트 코드의 객체, 변수 값을 콘솔 창에 출력하거나, 필요한 메시지를 표시할 수 있습니다.

[Console에 대한 추가 설명](https://developer.mozilla.org/en-US/docs/Web/API/console) 

### 흔히 활용되는 console 기능 

```js 
console.log( ); // 웹 브라우저 개발자도구의 콘솔 창에 메시지를 출력합니다.
console.info( ); // 기능적으로는 log와 같고, 사용하기에 따라 용도 구분이 가능합니다.
console.warn( ); // 콘솔 창에 경고 메시지를 출력합니다.
console.error( ); // 콘솔 창에 에러 비시지를 출력합니다.
```

___ 
<br>

## 변수와 상수

### 변수(variable) 

변수(variable)는 데이터를 저장할 때 쓰이는 ‘이름이 붙은 저장소’ 입니다. 온라인 쇼핑몰 애플리케이션을 구축하는 경우 상품이나 방문객 등의 정보를 저장할 때 변수를 사용합니다. 



JS에선 let 키워드를 사용해 변수를 생성합니다.

```js 
let x = 1;   //변수의 선언과 동시에 초기화
console.log(x);
```

```js
let x = 1;        
let y = x;
console.log('변경 전', x, y);
// 결과창: 변경 전 1 1

x = 'Hello!';
console.log('변경 후', x, y);  
// 결과창: 변경 후 Hello 1 
// C등과 같은 언어와 달리, 메모리상 가리키는 위치가 변경되기 때문에 Hello Hello로 결과가 나오지 않습니다.
```

```js
let x = 1;
console.log('첫 선언', x);

let x = 2;
console.log('다시 선언', x);  //이미 만들어진 주머니를 다시 만들(재선언) 수 없습니다
```

```js
console.log(xyz);
let xyz = 1;  //선언하기 전 코드를 사용할 수 없습니다.
```
<br>

### 상수(constant)

변화하지 않는 변수를 선언할 땐, let 대신 const 키워드를 사용합니다. (**변수와 같이 선언하고 초기화하는 형식은 같습니다.**)

`const password = '110085';`
이렇게 변수 const로 선언한 변수를 '상수(constant)'라고 부르며, 상수는 재할당할 수 없으므로 상수를 변경하려고 하면 에러가 발생합니다.


💡변숫값이 변경되면 안되는 값이라면 다른 개발자들에게 이 변수는 상수라는 것을 알리기 위해 const를 사용해 변수를 선언하도록 해야합니다.

<br>

```js
const password = '110085';
password = '123456'; // error, can't reassign the constant! 
```

### 변수와 상수의 공통 속성 
```js
//여러 변수와 상수 동시에 선언이 가능합니다.

let a = 1, b = 2, c = 3;
const X = 4, Y = 5, Z = 6;

console.log(a, b, c);
console.log(X, Y, Z);
```