
## - 20190803

##### Eslint 
##### Jest
##### github pair programming
##### underbar / recursion review
##### check point 1 scope 문제


> 린트 : 유닉스 운영 체제에서 사용되는 프로그램으로 C 언어의 원시 프로그램을 읽어들여 오류가 있는 검사하는 프로그램. 린트(lint) 또는 린터(linter)는 소스 코드를 분석하여 프로그램 오류, 버그, 스타일 오류, 의심스러운 구조체에 표시(flag)를 달아놓기 위한 도구들을 가리킨다.[1] 이 용어는 C 언어 소스 코드를 검사하는 유닉스 유틸리티에서 기원한다.[2]

<hr/>


#### 1.Data Structure & OOP
Graph, Tree, Hash Table, B-Tree Discussion
#### 2.Inheritance pattern - Dance Party
#### 3.Algorithms (N-Queens)
#### 4.Interact with Server (Chatterbox Client)
#### 5.ES6 APIs & React (Recast.ly)
#### 6.self Assesments1

<hr/>

#### 6. self Assessments - new 연산자를 통해서 생성된 인스턴스는 object 이다.
    함수 안에서 메서드를 만드는 방법
1.  Use Closure
2. 객체를 생성한뒤 , 해당 객체에 함수를 추가.
3.  Object.assign(newTree, treeMethods); 의 사용이유 => Object.assign() 메소드는 열거할 수 있는 하나 이상의 출처 객체로부터 대상 객체로 속성을 복사할 때 사용합니다. 대상 객체를 반환합니다.

1. 먼저 데이터가 담길 구조를 잡는다.
2. 프로토타입을 어떻게 이용할지 고려한다. => Object.assign(obj, method가 될 객체)

```js
'tree' { value: 2,
  children:
   [ { value: 5,
       children: [],
       addChild: [Function],
       contains: [Function],
       traverse: [Function] } ],
  addChild: [Function],
  contains: [Function],
  traverse: [Function] }
```

<hr/>

#### 4.Interact with Server (Chatterbox Client)


> fetch
>fetch (꺼냄)
> 미국·영국 [fetʃ] 발음듣기 영국식 발음듣기 중요도 별점 2개 다른 뜻(4건) 예문보기
> 1. (어디를 가서) 가지고 오다   2. (특정 가격에) 팔리다
> https://terms.naver.com/entry.nhn?docId=823204&cid=42344&categoryId=42344

fetch()를 불러들이는 경우, 취득할 리소스를 반드시 인수로 지정하지 않으면 안됩니다. 읽어들인 뒤, fetch()는 Promise객체를 반환합니다. 리퀘스트가 성공하든 실패하든 해당 리퀘스트 통신에 대한 Response객체가 취득됩니다. fetch()의 두번째 인수는 초기화에 사용되는 객체를 정의하고 있습니다. 이 인수는 기입하지 않아도 함수의 동작에 문제가 없습니다. 이 인수에 대한 상세한 정보는 Request)를 참고해주시기 바랍니다.

Response를 가져온 후에, 콜백함수의 매개변수로 담긴 response 객체에는 리스폰스에 포함되어있는 컨텐츠와 그에대한 처리방법이 담긴 메소드들이 담겨있습니다. 자세한 사항은 Body를 참고해주시기 바랍니다.

fetch('주소', 설정객체).then(콜백).catch(콜백);
.. fetch 만을 했을때는 서버에 저장된 정보를 그대로 가져온다.
then 을 통해 받아온 값을 처리 할 수 있다.

*GET*

```js
fetch("/test.json") // (/test.json) 호출 (GET)
    .then(e => e.json()) // 비동기
    .then(e => console.log(e)); // 비동기
```

*옵션으로 POST*

```js
fetch("/test.json", {
    method: "POST" // (/test.json) 호출 (POST)
})
.then(e => e.json()) // 비동기
.then(e => console.log(e)); // 비동기
```


https://www.zerocho.com/category/HTML&DOM/post/595b4bc97cafe885540c0c1c

<hr/>


### *서버*
Web Architecture 란?

    이제는 삶에서 없으면 안될만큼 아주 중요한 부분을 차지하고 있는 것이 바로 인터넷이다.    
    처음에는 인터넷에 연결이 되기만 하면 둥둥 떠있는 것처럼 원하는 곳으로 헤엄치며 다니면서 원하는 정보를 보고 듣고 가져올 수 있을 거라고 생각했다. 
    아주 추상적인 생각이다. 이번 블로그에서는 이러한 일을 가능하게 만들어 주는 구성요소에 대해 간략히 알아보자.
    Application Programming Interface(API)
    어떤 프로그램에서 사용할 수 있도록 운영체제나 프로그래밍 언어가 제공하는 기능을 제어할 수 있게 만든 인터페이스

*인터페이스: 서로 다른 두개의 시스템, 장치 사이에서 정보나 신호를 주고받는 경우의 접점이나 경계면*

Client (=== Browser)
사용자가 보기 좋게, 편하게 만들어 주는 어플리케이션

Server
클라이언트의 요청을 받아서 요청을 적합하게 처리하는 어플리케이션

HTTP
클라이언트와 서버가 소통하기 위한 규칙을 정해 놓은 것
 
HTTP 장점
클라이언트와 서버 간에 요청의 제한 없이 정보를 저장하거나 하지 않기 때문에 무한히 요청하고 응답할 수 있다.

HTTP 단점
저장을 하지 않는 다는것이 단점이다. 그래서 요청은 항상 독립적인 요청이다.
 
Client는 HTTP를 통해서 Server가 이해할 수 있는 언어로 명령을 요청하고,
Server는 HTTP를 통해서 Client가 이해할 수 있는 언어로 응답해준다.

Asyncronous Javascript and XML(AJAX)
비동기적으로 작동하는 자바스크립트를 이렇게 부른다. 하나의 개념이라고 생각하면 쉽다. AJAX의 장점은 전체를 새로고침 하지 않고 필요한 부분만을 업데이트 할 수 있다.

fetch
fetch는 ajax를 구현하는 여러방식 중에 하나

```js
fetch( url )
  .then(response => response.json())
  .then(result => console.log(result))
  .catch(error => console.log(error));
  
 // json 구조의 data
```

웹 서비스는 위의 구성요소를 활용하여 사용자들이 여러 정보를 주고 받는 일련의 방식/형태

## 20190805 MON
React 

## 20190809 FRI

#### 1. ToyProblem 09(deep Equal)
>재귀를 이용한 풀이. 

재귀적 사고 -> 작은것부터 해결한다.


```js
deepEquals({}, {}).should.be.true();
var a = { foo: 'bar' };
var b = { foo: 'pow' };
deepEquals({a:1, b: {c:3}},{a:1, b: {c:3}}); // true
deepEquals({a:1, b: {c:5}},{a:1, b: {c:6}}); // false
var a = { foo: 1, b: { c: { d: { e: 'potato' } } } };
var b = { foo: 1, b: { c: { d: { e: 'potato' } } } };
```

테스트 케이스에서 주어진 값에 조건을 맞춰가다 보면 base case가 잡히고,
이를 토대로 재귀가 필요한 부분에 대한 사고가 가능하다.

#### 2. React Spring Animation
 https://www.evernote.com/l/AO_1N8Wyz5REB6QHUQXgxuXYGRxUAwIS8nE

## 3. SPRINT REVIEW Reactly
>props: 부모(상위) Component 에서 자식(하위) Component로 내려주는 데이터, 리액트 에서는 단방향 데이터이기 때문에 내려갈 수 만 있다.

즉 다시 상위로 올라갈 수 없다. ( 간접적으로 올릴 수 있다. = state )


>state: class Component에 존재하며, Component가 갖고 있는 상태.
모든 Component에서 state를 갖을수 있으나, 모든 곳에서 갖고있는건 비효율적이다.
state = 변화를 감지하고, 바꿀수 있다.
어떤 Component에서 "state를 관리" 할때 가장 좋을지를 고려하면서 코딩해야 한다.
데이터 흐름을 항상 염두에 둬야한다. ( 데이터를 어디에서 가지고있을 것인가 염두할 것 )

>클래스 컴포넌트에서 사용 가능. 
컴포넌트 내부에서만 접근 가능하다(private). immutable / 변경하려면 setState() 사용
state 변화의 결과로 life cycle이 순환한다.

>Lifting state up
자식 Component의 액션으로 인해서 부모 Component의 state가 바뀌는것을 의미한다.
예) 검색구현, 검색 을 했을때 App 에 있는 State를 변경 ( 자식 Component 가 부모 Component State 를 변경 )
하지만, 데이터를 자식에서 부모로 바로 올릴수 는 없다.
setState를 이용하는 함수를 만들어서 자식 Component에게 props로 내려준다.

>즉, 부모 Component에서 먼저 자신의 state를 바꾸는 함수를 자식 Component에 Props로 넘겨준다.
그후, 자식이 위 함수를 실행시키면 부모의 state가 바뀐다. 
자식의 어떤 액션을 통해서 부모의 state를 바꾸는 일의 과정이 위와 같다.
위 함수에 매개변수를 넘기면 => 부모와 자식이 같은 매개변수를 참조? 한다.

>자식 컴포넌트가 부모 Component State를 바꾸기 위해서는
부모 Component 에서 먼저 자신의 state를 바꿀 함수를 만든다.
그리고 만든 이 함수를 자식에 props로 내려주고
자식은 이 함수를 통해 부모 Component를 바꾸는 구조.


#### bind issue

```js 
this.setState
```
A: 부모 Component(Class) 에서 setState 함수를 만들어서 B: 자식 Component(functional)를 넘겨줬을때,
(함수안에는 this.setState 라는 동작을하고 있다.)
위 this는 B가 된다.
B는 functional 이어서 상태가 없기 때문에 this는 B가 안된다. 
그리고 우리는 A를 바꾸고 싶은 상황이다.

따라서 우리는 bind를 사용한다. this가 무엇인지를 고려해야 한다. A를 바인딩 한다.

Component depth가 깊어져서 state 관리가 힘들수 있다. (drilling) 
구조를 짜는게 중요하다.

Life Cycle API 
컴포넌트의 생애주기 각 시점에 원하는 작업을 수행할 수 있게 도와주는 API


## 4. TodoList
#### 1. Component 구조 설계
(Tip. React best practice)

1. 하나의 컴포넌트 에서는 하나의 기능을 한다.
예를 들면, 단순히 보여주는 컴포넌트, 데이터를 받아와서 뿌려주는 컴포넌트 등 ..

2. 재사용 가능한 컴포넌트는 하나만 구현하여 공유하는 것이 좋다.
(반복되서 사용되는 컴포넌트 캐치하기)

3. DOM을 직접 건드리지 않는다.


## 20190810 SAT
### Sprint 
#### TodoList
1.데이터 관리.
데이터를 저장할 모양을 정하는 것이 매우 중요하다.

2.Componenet 구조
 기능별로 Component 분리
 재사용 가능한 Component 만들기


## 20190811 SUN
### 리액트 복습
컴포넌트 별로 분리 한다 => 각 기능별로 새로운 function / class 를 생성하고, 데이터를 뿌려주는 부분을 상정 structure 를 짠다.

다시 기초부터.

App.js
```js
import React, { Component } from 'react'
import TodoListTemplate from './components/TodoListTemplate';
import Form from './components/Form'
import TodoItemList from './components/TodoItemList'

export default class App extends Component {
  render() {
    return (
      <TodoListTemplate form={<Form/>}> {/* components */}
        <TodoItemList />
      </TodoListTemplate>
    )
  }
}
```
App.js 에 코드는 위와 같다. 
render()되는 부분에서 '<'TodoListTemplate'>' 같은 녀석들은 TodoListTemplate.js 파일내의 TodoListTemplate이라는 이름으로 정의된 함수 또는 클래스를 App.js로 불러온다고 생각하면 된다.

https://i.imgur.com/nnYKPBo.png


## 20190812 MON
### Sprint Review

Component 단위로 생각하기.
1. 기능별로 / 
2. 재사용 가능한 /

기능별로 나누기. 

*CSS
Ant Design -> React Component  
Semantic Ui React
https://www.styled-components.com/

### Server and Node

1.Event loop && call stack
JavaScript 는 Single Thread 언어로 한번에 하나의 일만 처리할 수 있다.

https://www.youtube.com/watch?time_continue=467&v=8aGhZQkoFbQ
#### 블로킹 
네트워크 요청이나 이미지 프로세싱 같이 느린동작이 스택에 남아있는 것을 보통 블로킹 이라고 합니다.
위 동작들이 스택에 남아있는 동안에는 브라우저에서 다른 작동을 할수 없습니다.

#### 비동기 콜백
어떤 코드를 실행하면 콜백을 받고 이걸 나중에 실행한다.
이벤트 루프와 동시성.
setTimeout 과 같은 비동기적 함수를 실행시에, 스택에서 쌓여있는 채로 있는것이 아닌 스택에 쌓인후 사라진뒤에, 다시 호출된다?

### Node.js
이벤트 기반 논블로킹 I/O 모델
유저의 클릭이나 네트워크에 리소스를 요청하는 이벤트가 논블로킹으로 이루어지는 Input Output model


## 20190813 TUE
#### Toy11
sorted-rotated array에서의 BinarySearch 의 활용.

http://blog.gainlo.co/index.php/2017/01/12/rotated-array-binary-search/

#### NodeJS
서버와의 연동.


## 20190814 WED

#### Toy12
순열 조합 문제

```js
var powerSet = function(str){
let newStr=''
for(let x=0;x<str.length;x++){
    if(x===str.indexOf(str[x])){
     newStr+=str[x]
    }
}
let result=[""]
 function combi(prefix,str){
   for(let i=0;i<str.length;i++){
       result.push(prefix+str[i])
       combi(prefix+str[i],str.slice(i+1))
   }

 }
 combi("",newStr)


return result
}
```

#### JavaScript Event Loop
node.js 와 server side -> v8 엔진의 사용

V8 엔진의 구성
Call Stack, Task Queue(Event queue), Heap

Call Stack, 자바스크립트는 단 하나의 콜 스택을 갖고 있다.
Task Queue, Call stack 이루어졌을때, 먼저 대기열에 온 순서대로 실행 된다.
SetTimeout같은 비동기로 호출되는 함수들은 Task Queue에 enqueue된다.
자바스크립트에서는 이벤트에 의해 실행되는 함수(핸들러)들이 비동기로 실행된다. 자바스크립트 엔진이 아닌 Web PI 영역에 따로 정의되어 있는 함수들은 비동기로 실행된다.



https://asfirstalways.tistory.com/362


## 20190815 THU

Node.js 프로그래밍 복습 ( Do It! Node.js 책 )

## 20190816 FRI

#### Toy13
BFS

Node.js 

### Promise 

**'Promise는 자바스크립트 비동기 처리에 사용되는 객체'**

*비동기와 콜백
비동기 처리? 그게 뭔가요? (Non- blocking)
자바스크립트의 비동기 처리란 특정 코드의 연산이 끝날 때까지 코드의 실행을 멈추지 않고 다음 코드를 먼저 실행하는 자바스크립트의 특성을 의미합니다. 

**특정 로직의 실행이 끝날 때까지 기다려주지 않고 나머지 코드를 먼저 실행하는 것이 비동기 처리입니다.**

#### 프로미스의 3가지 상태 (states)
프로미스의 처리 과정.

Pending(대기) : 비동기 처리 로직이 완료되지 않은 상태
```js
new Promise();
new Promise(function(resolve, reject){

});
```

Fulfilled(이행(완료)) : resolve를 아래와 같이 실행하면  비동기 처리가 완료되어 프로미스가 결과 값을 반환해준 상태

*프로미스로 처리하기를 원하는 데이터를 Promise를 통해 resolve(data) 와 같이 받는다. 이후 then을 통해 결과값을 받는다.*

```js
new Promise(function(resolve, reject){
    resolve();
});

function getData(){
    return new Promise(function(resolve, reject){
        var data = 100;
        resolve(data);
    })
}

// then()을 이용하여 처리 결과 값을 받는다.
getData().then(function(resolveData){
    console.log(resolvedData);
});
```

Rejected(실패) : 비동기 처리가 실패하거나 오류가 발생한 상태
```js
function getData(){
    return new Promise(function(resolve, reject){
        var data = 100;
        resolve(data);
    })
}

// then()을 이용하여 처리 결과 값을 받는다.
getData()
.then()
.catch(function(err){
    console.log(err);
});
```

![promise](https://joshua1988.github.io/images/posts/web/javascript/promise.svg)

## 20190817 SAT
### async & await

## 20190818 SUN
날씨 맑음.
### tree-map

## 20190819 MON
### fetch 
(https://developer.mozilla.org/ko/docs/Web/API/Fetch_API/Fetch%EC%9D%98_%EC%82%AC%EC%9A%A9%EB%B2%95)

```js
var myImage = document.querySelector('img');

fetch('flowers.jpg')
.then(function(response) {
  return response.blob();
})
.then(function(myBlob) {
  var objectURL = URL.createObjectURL(myBlob);
  myImage.src = objectURL;
});
```
이것은 네트워크를 통해 사진을 취득하여 <img>요소에  삽입하는 스크립트입니다. fetch()의 가장 간단한 사용법으로 단 하나의 파라미터를 전달합니다. 여기서 전달하는 파라미터는 fetch()에서 취득하고 싶은 리소스나 그에대한 주소입니다. 이 코드는 promise로 감싸고 있는 Response 오브젝트를 반환합니다.

### DataBases
데이터베이스 저장방식

*목표*
>1.database 가 무엇인지 이해한다

>2.database management system (DBMS)가 무엇인지 이해한다

>3.SQL 기본 query문을 사용할 줄 안다

>4.Schema의 설계 방법과 나은 방향성을 고안한다

>5.서버와 클라이언트 사이에서 데이터를 주고 받은 데이터를 database에 저장하여 영속성있게 저장할 수있다

프로그램에서 다루는 데이터가 많아질수록, 그 데이터를 동시에 사용하는 사람이 많아질수록 데이터의 관리는 어려워집니다.
이러한 데이터를 쉽고 편리하게 다룰 수 있도록 하기 위해서 등장한 것이 데이터베이스 메니지먼트 시스템입니다.


## 20190825 SUN

#### CheckPoint review
*Keyword : 호이스팅 : var 는 function 에서 / let 과 const는 block 에서 / 스코프 체인
#### Tree Map review

#### fetch review

#### inheritance-pseudo-classical review
```js
Object.create(proto[, propertiesObject])
proto = 새로 만든 객체의 프로토타입이어야 할 객체.
```    

#### react review
https://ko.reactjs.org/

<img width="962" alt="스크린샷 2019-08-25 오후 2 33 40" src="https://user-images.githubusercontent.com/48753593/63645998-61439280-c745-11e9-84b5-bfbf5426f9e0.png">

<img width="962" alt="스크린샷 2019-08-27 오전 11 25 04" src="https://user-images.githubusercontent.com/48753593/63739841-b8727000-c8c9-11e9-992a-239114f86fb1.png">

<img width="962" alt="스크린샷 2019-08-27 오후 1 14 37" src="https://user-images.githubusercontent.com/48753593/63740645-dc838080-c8cc-11e9-9836-2c866f4c0ebf.png">

## 20190829 THU

### Redux

<img width="1006" alt="스크린샷 2019-08-29 오후 11 28 46" src="https://user-images.githubusercontent.com/48753593/63994016-038cbd00-cb2e-11e9-9b24-09da678e078f.png">





## 20190830 FRI
### merge sort
<img width="538" alt="스크린샷 2019-08-30 오전 9 40 11" src="https://user-images.githubusercontent.com/48753593/63985400-8b60d000-cb0a-11e9-8163-2bc18a291d7a.png">

algorithm : divide and conquer 
>divide and conquer to sort a list of elements. Meaning, it will divide the bigger problem into smaller problems and then solve each of the small problems in order to solve the bigger problem that we started out with.

```js
// Merge Sort Implentation (Recursion)
function mergeSort (unsortedArray) {
  // No need to sort the array if the array only has one element or empty 
  if (unsortedArray.length <= 1) {
    return unsortedArray;
  }
  // In order to divide the array in half, we need to figure out the middle
  const middle = Math.floor(unsortedArray.length / 2);

  // This is where we will be dividing the array into left and right
  const left = unsortedArray.slice(0, middle);
  const right = unsortedArray.slice(middle);

  // Using recursion to combine the left and right
  return merge(
    mergeSort(left), mergeSort(right)
  );
}
```

setup basecase

```js
if (unsortedArray.length <= 1) { 
    return unsortedArray; 
}
```

```js
// Merge the two arrays: left and right
function merge (left, right) {
  let resultArray = [], leftIndex = 0, rightIndex = 0;

  // We will concatenate values into the resultArray in order
  while (leftIndex < left.length && rightIndex < right.length) {
    if (left[leftIndex] < right[rightIndex]) {
      resultArray.push(left[leftIndex]);
      leftIndex++; // move left array cursor
    } else {
      resultArray.push(right[rightIndex]);
      rightIndex++; // move right array cursor
    }
  }

  // We need to concat here because there will be one element remaining
  // from either left OR the right
  return resultArray
          .concat(left.slice(leftIndex))
          .concat(right.slice(rightIndex));
```

## 20190903 TUE

### Front : React Nested Routes
### Cookie 를 이용한 id 로그인 구현 ( 서버 - 클라이언트 )

## 20190904 THU

### axios

```js
axios.post('http://pokeapi.co/api/v2/pokemon/', {
  pokemon: 'Pikachu',
  })
  .then((response) => {
    return response;
  })
  .catch((error) => {
    console.log(error);
  });
```

## 20190907 SAT
### 1.정적인 웹 페이지 vs 동적인 웹 페이지
정적 웹페이지 : 항상 같은 내용을 보여주는 웹페이지

동적 웹페이지 : 사용자의 인터랙션에 따라 웹페이지가 바뀌어가는 것

### 2.REDUX
<img width="985" alt="스크린샷 2019-09-08 오후 7 40 20" src="https://user-images.githubusercontent.com/48753593/64487065-9802c800-d270-11e9-99f4-a606a915a808.png">

<img width="1384" alt="스크린샷 2019-09-09 오전 9 44 26" src="https://user-images.githubusercontent.com/48753593/64497125-6debed00-d2e6-11e9-9e35-e171db2c55f5.png">

<hr />

>앱의 상태 전부는 하나의 스토어(store)안에 있는 객체트리에 저장된다.

>상태 트리를 변경하는 유일한 방법은 무엇이 일어날지 서술하는 객체인 액션(action)을 보내는 것 뿐입니다. 

>액션이 상태 트리를 어떻게 변경할지 명시하기 위해 여러분은 리듀서(reducers)를 작성해야 합니다

#### Store
하나의 객체를 직렬화(serialize) 해서 서버와 클라이언트가 프로그램의 전체 상태값을 주고 받을 수 있습니다. 하나의 객체에 프로그램의 전체 상태값을 저장합니다.

상태값은 오직 액션 객체에 의해서만 변경됩니다. ( state에 직접 접근 / 이용은 절대 불가능 합니다. )
reducer 함수를 통해서 공급해야 합니다.

#### action
상태에 어떠한 변화가 필요하게 될 땐, 우리는 action이란 것을 발생 시킵니다.

#### reducer
reducer는 이전 상태값과, 액션 객체를 입력으로 받아서 새로운 상태값을 만드는 순수 함수.
(state, action) => nextState // 현재 state값과 액션을 이용해서 nextState 즉 state를 변경 시킵니다.

#### dispatch
store에 있는 data를 업데이트, 상태값을 수정 할 때 사용되는 메소드로 인수로는 action을 받습니다.

#### subscribe
연결되어 있는 해당 컴포넌트에서 스토어의 데이터의 변경이 있을시 바로 반영 시킵니다.
state를 변경시키기 위해선 action이 dispatch 되야 합니다.

<hr />

#### 코드 구현

일련의 순서가 존재하지는 않지만, 
action -> reducer -> store -> components 순서로 생성

*Folder 구성*

*action
    변화를 원하는 부분..
    type 설정
    
*components

*containers
    dispatch에서 action을 사용한다.

*reducers

*index.js
    store 생성
    const store = createStore(reducer)


## 20190908 SUN
### 1.NODE.js 정리

<img width="776" alt="스크린샷 2019-09-08 오후 8 42 00" src="https://user-images.githubusercontent.com/48753593/64489740-87167e80-d291-11e9-8579-944467a5f017.png">

## 20190909 MON

### AWS
<hr />

### Deploy의 늪

<img width="815" alt="스크린샷 2019-09-12 오전 11 04 28" src="https://user-images.githubusercontent.com/48753593/64748448-287d2900-d54d-11e9-8b3f-c9c7e0ef0d75.png">

#### E3

#### local balance

#### cloud front

## 20190910 TUE

### Python basic

### Django Setting



<center>

# 2019.11.16 토요일

</center>

**😇TIL**

1. BLOG & RESUME SITE

> ☑️ ~~RESUME SITE 번호 / 문구 및 이미지 (png to svg convert) 추가 and 수정 중~~ <br>
> 🆇 BLOG box-shadow / transition / margin / z-index 설정 and 수정 중<br>
> flex 설정 / md={12}, lg 페이지를 나눈다 비율 별로<br>
> 포지션 / CSS 겹쳤을 때 우선순위 (Inline 코드냐.. 등)

> [CSS_1](https://www.youtube.com/watch?v=jV8B24rSN5o)<br>[CSS_2](https://www.youtube.com/watch?v=k4xA_Olo_Uo)<br> [CSS_3](https://www.codingfactory.net/10529)

2. DJANGO

> Django 모델 생성은 곧 DB를 생성하는 건데, 이는 곧 스키마를 정의 하는 것으로 생각하면 되는지 ? <br>
> | <br>
> Django 에서 model을 먼저 구현하여 admin 페이지를 구성하는데, admin 페이지의 정확한 역할은 ? <br>
> |

---

**😭TODO**

1. BLOG 기능 추가

> BLOG 추가해야할 기능 - 검색기능 작동하도록 / 내비게이션 바 / 드롭박스 Resume 완성후 추가 / Font Setting <br>
> ✖︎ Resume 페이지 완성하기

---

**🥰COMMENT**

<b>아이패드 사야겠다.<b>

---

<center>

# 2019.11.17 일요일

</center>

**😇TIL**

1. ⭐️ IDEA

> 아이디어 : 구글 캘린더를 쓰는데, 캘린더에 오늘 할일을 계획 하고, 그걸 다시 TIL에 정리하는건 비효율적이지 않나 싶다. <br>
> 구글 캘린더 연동 페이지를 만들어 보고 싶다. 먼저 가능한지 부터 고려해보기.
> 구체적으로 생각해보면 구글 캘린더에 작성한 내용을 블로그에 옮길 수 있는지 가능성 체크
> 먼저 입력받은 구글 캘린더 데이터 export를 해서 내 개츠비 서버로 받아와야 하는데 개츠비는 graphQL이고 ..

2. BLOG FONT SETTING

<del>Blog Font Setting

> 블로그 font css setting 을 했다. Google Font site에서 원하는 폰트를 가져와서 갯츠비에 이식하는데, html 태그로 적용하는건 힘이 드는 과정. 따라서 `gatsby-config`의 `gatsby-plugin-prefetch-google-fonts` 를 활용하여 세팅했다. font-family의 적용방법을 보다 상세하가 알게되었다.<br> 순서 에 따라서 또 언어에 따라서..

---

**😭TODO**

✖︎ 1. 블로그에 알고리즘 페이지 만들기

---

**🥰COMMENT**

<b> 주말 이라서 인지, 비 때문인지 코딩이 잘 안되는 기분..<b>

---

<center>

# 2019.11.18 월요일

</center>

**😇TIL**

BLOG 기능 추가 (navbar)

> ☑️BLOG React Bootstrap 을 설치해서 navbar 세팅을 새로함 / React Bootstrap package의 경우 Navbar(header) 자체를 임의로 컨트롤하여 수정하기에는 불편함이 존재. 이후로는 안쓸듯<br> ☑️ <del>Favicon Setting</del> <br> ☑️<del>Notion Resume Fin https://www.notion.so/elt1992/Lee-Chan-Haeng-074a6e1fabd244ff830ae862a200dd5f</del>

---

**😭TODO**

포트폴리오 / 깃헙 / Favicon 세팅

> ☑️~~포트폴리오 만들기 ( Resume 를 노션으로 할지 / 사이트로 할지 정하기 ) 노션으로 작성 완료<br>~~
> GITHUB 정리<br>
> ☑️Favicon 설정 Gatsby의 경우 `gatsby-config.js`에서 `gatsby-plugin-manifest` 의 `icon`을 통해 favicon 설정이 가능하다.

---

**🥰COMMENT**

드디어 <b>[레쥬메](https://www.notion.so/elt1992/Lee-Chan-Haeng-074a6e1fabd244ff830ae862a200dd5f)</b> 완성

---

<center>

# 2019.11.19 화요일

</center>

**😇TIL**

---

**😭TODO**

BLOG 기능 추가 ( 태그 위치, Search bar )

> 🆇 ~~페이지 상단 태그 위치 변화 기능 구현( gatsby config )~~<br> - 우측 또는 좌측으로 빼서 스크롤 같이 되고, 페이지 이동되게 구현 해야함 => TOC 이었음<br>
> Search Bar 구현

장고

> 🆇 장고 강의 15강 까지 듣기

Resume Site

> 🆇 Resume site 완성은 시켜놓기 (노션 내용으로)

면접 준비

> 🆇 퀵소트

블로그 내용 채우기

>

앞으로 해야할 녀석들

> 🆇 Redis / GraphQL / TypeScript / Data Structure

---

**🥰COMMENT**

과유불급

<center>

# 2019.11.20 수요일

</center>

이사

<center>

# 2019.11.21 목요일

</center>

**😇TIL**

---

**😭TODO**

MySQL

도서관 DB 스케마 작성해보기

> ~~[DB_diagram](https://dbdiagram.io/d)~~

---

**🥰COMMENT**

도서관 DB를 짜긴 했는데(버전 1) 사실 나혼자 한거라서 정확하지도 않고, 자문이 필요하다.

<center>

# 2019.11.22 금요일

</center>

**😇TIL**

Django

> Django View단 돌입. 프론트 작업도 장고로 하는데.. 문제는 장고는 html 파일 자체에서 장고 문법을 활용해서 프론트를 구성한다. 나름 편하긴 한데 리액트만 못한 느낌 적인 느낌

---

**😭TODO**

> Models.py / admin.py 에서 list_display 가 도저히 이해가 가지 않는다. field도 없는 녀석이 어째서 DB에 추가된단 말인가.. 모델에서 정의해준 녀석도 아니면서 ㅠㅠ

---

**🥰COMMENT**

모르는 문제 / 막히는 문제를 만났을 때 접근 방법을 체크해가며 소거하여 같은 일을 반복하지 않도록 하자.

---

<center>

# 2019.11.23 토요일

</center>

**😇TIL**

> ~~번역 완료~~<br>
> Serialize 개념 정리 <br>
> React + Koa 블로그 만들기 진행 중 <br>
> mongoose 진행 중<br>
> 코드 자체보다 로직이 어떻게 되는지를 이해하는데에 힘쓰는 중<br>
> 코드 스플리팅 학습<br>
> 블로그 코드 스플리팅 필요 (블로그 첫 페이지 대기 시간이 긴 이유 / 리액트 특성인점도 있지만)

---

**😭TODO**

BUFFER

> Buffer 정리하기

번역

> ~~[REST](https://medium.com/@BennettGarner/build-your-first-rest-api-with-django-rest-framework-e394e39a482c) 번역하기~~

블로그 CSS

> TOC를 a 태그로 처리할 수 있다는 소식을 들었다. 도전 해야지

리액트 책

---

**🥰COMMENT**

Koa 서버 만들기 중 / 장고가 편하긴 한 것 같기도 하고

---

<center>

# 2019.11.24 일요일

</center>

**😇TIL**

---

**😭TODO**

리액트 노마드!

> [리액트 노마드](https://academy.nomadcoders.co/courses/216871/lectures/10881270)

---

**🥰COMMENT**

TOC 해보겠다고 새벽 3시까지 블로그 코드 뜯고 에러나서 커밋 리셋하고 ... ㅠ.ㅠ

---

<center>

# 2019.11.25 월요일

</center>

**😇TIL**

TOC

> TOC 결국 해냈다. gatsby remark 의 table of contents를 구현하기 위해서 `gatsby-plugin-catch-links` 이 녀석을 활용했다. <br>slug를 넘겨줘서 해결 했는데,
> 이 블로그 템플릿 자체가 내가 초기부터 구현한 코드가 아니다 보니까 URL에 'ko/' 같이 언어 선택 부분에 대한 경로가 추가되는데 이녀석들을 다 지워버려서 해결했다. ㅠㅠ 너무힘들었다..
> 마크다운으로도 링크를 만들 수 있는데 `[마크다운](#헤더네임)`이런 식이다.<br> 근데 이 건 내가 헤더를 사용할때마다 상단이나 다른부분에 계속 추가를 해줘야하는 불편함이 있는데, `gatsby-transformer-remark` 를 활용하면 내가 작성한 헤더가 자동으로 TOC로 생성된다!!

> 이제 사이드에 TOC추가 완료! ~~바로 해당 컴포넌트를 옮기고 CSS 먹여야지~~ CSS로 처리했다.

---

**😭TODO**

> ~~TOC 기능구현이 되었으니 이제 사이드 바로 해당 컴포넌트를 옮기고 CSS 먹여야지~~<br>
> Gatsby를 효율적으로 사용하기 위해서는 GraqphQL 공부가 절실하다. <br>
> AIRBNB 진행 중

---

**🥰COMMENT**
성공의 기쁨! 아이디어를 설계 해봐야하는데 ..

---

<center>

# 2019.11.26 화요일

</center>

**😇TIL**

> Movie_app 를 리액트로 만들기(노마드) : 리액트 복습 겸 실시. http://yts.am/ 에서 MovieAPI 받아서 했다.<br>
> Airbnb 복습 -> <b>listdisplay</b>, 외래키 , 필드 개념 확립!<br>
> AIRBNB 진행 중

---

**😭TODO**

> Movie_app 블로깅 하기

---

**🥰COMMENT**<br>
Movie_app 은 손쉽게 만들 수 있다. 이를 보다 고도화 해보자 어떻게?

---

<center>

# 2019.11.27 수요일

</center>

**😇TIL**

> Express passport<br>
> AIRBNB 진행 중 (~ 12강 까지)

---

**😭TODO**

> - 18 강 까지 Airbnb 하기

> - 아이디어 구체화 해보기<br>
>   아이디어 : 구글 캘린더를 쓰는데, 캘린더에 오늘 할일을 계획 하고, 그걸 다시 TIL에 정리하는건 비효율적이지 않나 싶다. <br>
>   구글 캘린더 연동 페이지를 만들어 보고 싶다. 먼저 가능한지 부터 고려해보기.
>   구체적으로 생각해보면 구글 캘린더에 작성한 내용을 블로그에 옮길 수 있는지 가능성 체크
>   먼저 입력받은 구글 캘린더 데이터 export를 해서 내 개츠비 서버로 받아와야 하는데 개츠비는 graphQL이고 ..<br>
>   였는데, 알아보니까 <b>구글 캘린더 API</b>가 존재한다!! <br>

---

**🥰COMMENT**<br>
Airbnb 클론 을 통해 얻어가야 할 것 들을 얻기 / 업그레이드 하기

---

<center>

# 2019.11.28 목요일

</center>

**😇TIL**

> 아이디어 다시 구체화 중

---

**😭TODO**

---

**🥰COMMENT**<br>
한게 없다

---

<center>

# 2019.12.01 일요일

</center>

**😇TIL**

> GraphQL 복습중 <br>
> Docker 복습중 <br>
> CORS 복습중 - HTTP에 정리.

---

**😭TODO**

---

**🥰COMMENT**<br>
비 오고 .. 춥고..

---

<center>

# 2019.12.02 월요일

</center>

**😇TIL**

> [노션](https://www.notion.so/elt1992/Local-SNS-635c595cc78a47f2bee0421f87c33cf4) 에 프로젝트 추가함<br> > ~~인스타그램 크롤링 완료(해시태그)~~

---

**😭TODO**

> 인스타그램 크롤링 완료해야함

---

**🥰COMMENT**<br>
손대는 프로젝트가 많아진다.

---

<center>

# 2019.12.03 화요일

</center>

**😇TIL**

> 개인 프로젝트 중<br> [노션](https://www.notion.so/elt1992/Local-SNS-635c595cc78a47f2bee0421f87c33cf4)<br>
> 인스타그램 해시태그 크롤링 초기 세팅 완료 / 프로젝트 목표 재정립

---

**😭TODO**

> 해시태그 데이터 가공하기<br>
> 프로젝트 블링커 블로그 정리(여유있게 하기)

---

**🥰COMMENT**<br>
수많은 에러를 만났다.. 그래도 아직까진 순항중?

---

<center>

# 2019.12.04 수요일

</center>

**😇TIL**

> 개인 프로젝트 중<br> [노션](https://www.notion.so/elt1992/Local-SNS-635c595cc78a47f2bee0421f87c33cf4)<br>
> 인스타그램 해시태그 + Date + Place 크롤링 완료

---

**😭TODO**

> 프로젝트 블링커 블로그 정리(여유있게 하기)

---

**🥰COMMENT**<br>
크롤링할 데이터 추가

---

<center>

# 2019.12.05 목요일

</center>

**😇TIL**

> 개인 프로젝트 중<br> [노션](https://www.notion.so/elt1992/Local-SNS-635c595cc78a47f2bee0421f87c33cf4)<br>
> DB 설계 <br>
> UI/UX Sketch + Zeplin 유튜브 강의 시청

---

**😭TODO**

> 프로젝트 블링커 블로그 정리(여유있게 하기)<br>
> DB 스키마 설계<br>
> UI/UX Sketch + Zeplin 유튜브 강의 시청

---

**🥰COMMENT**<br>
DB를 몽구스로 초기 선택했는데, 몽구스는 관계형성이 어렵지 않나 싶다.. SQL로 갈아타야 할지 고민중<br>
클라이언트 입장에서 생각하며 프로그램 구성하기. 어떻게 접근할지에 따라서 어떤 DB를 사용하고 / 어떻게 데이터를 쌓느냐 부터가 다른것 같다.<br>
내 데이터를 고려하면서 DB를 설계하자

---

<center>

# 2019.12.06 금요일

</center>

**😇TIL**

> 개인 프로젝트 중<br> [노션](https://www.notion.so/elt1992/Local-SNS-635c595cc78a47f2bee0421f87c33cf4)<br>
> DB 설계 <br>

---

**😭TODO**

> 프로젝트 블링커 블로그 정리(여유있게 하기)<br>
> DB 스키마 설계<br>
> UI/UX Sketch + Zeplin 유튜브 강의 시청<br>
> D3를 위한 CSV파일 생성 필요..

---

**🥰COMMENT**<br>
해시태그가 내 생각보다 의미있는 데이터 같지 않다.. 쩝..

---

<center>

# 2019.12.07 토요일

</center>

**😇TIL**

> CSV 파일 생성을 위한 해시태그 데이터 JSON 타입으로 만들기.
> D3를 위한 CSV파일 완료
> D3로 워드클라우드 생성 완료

---

**😭TODO**

> 프로젝트 블링커 블로그 정리(여유있게 하기)<br>
> DB 스키마 설계<br>
> UI/UX Sketch + Zeplin 유튜브 강의 시청<br>
> 크롤링 데이터 다시 고도화 필요 ( 댓글 1에 태그를 숨기는 케이스 존재)

---

**🥰COMMENT**<br>
눈이다 눈

---

<center>

# 2019.12.08 일요일

</center>

**😇TIL**

> Sketch 조금 구현
> 엑스포 초기 세팅 구현

---

**😭TODO**

> 프로젝트 블링커 블로그 정리(여유있게 하기)<br>
> DB 스키마 설계<br>
> UI/UX Sketch + Zeplin 유튜브 강의 시청<br>
> 크롤링 데이터 다시 고도화 필요 ( 댓글 1에 태그를 숨기는 케이스 존재)<br>
> 엑스포 학습

---

**🥰COMMENT**<br>
이상하다 분명히 하루에 일과 하나씩은 마무리 하는데 TODO가 늘어간다?

---

<center>

# 2019.12.09 월요일

</center>

**😇TIL**

> 코드 모듈화

---

**😭TODO**

> 프로젝트 블링커 블로그 정리(여유있게 하기)<br>
> UI/UX Sketch + Zeplin 유튜브 강의 시청<br>
> 크롤링 데이터 다시 고도화 필요 ( 댓글 1에 태그를 숨기는 케이스 존재)<br>
> 엑스포 학습

---

**🥰COMMENT**<br>
반복되는 부분을 나중에 모듈화 하면 되겠지 라고 생각했지만, 반대로 했어야 했다. 반복적으로 사용할 부분을 미리 고려하여 모듈화를 해서 코드를 구성해야 나중에 편하다.
코드가 길어질수록 지저분하고 보기가 힘들어 모듈화도 힘들다..

---

<center>

# 2019.12.10 화요일

</center>

**😇TIL**

> 서버 구축 및 크롤링 코드 삽입

---

**😭TODO**

> 프로젝트 블링커 블로그 정리(여유있게 하기)<br>
> UI/UX Sketch + Zeplin 유튜브 강의 시청<br>
> 크롤링 데이터 다시 고도화 필요 ( 댓글 1에 태그를 숨기는 케이스 존재)<br>
> 엑스포 학습

---

**🥰COMMENT**<br>

---

<center>

# 2019.12.12 목요일

</center>

**😇TIL**

> 서버 구축 및 크롤링 코드 삽입
> 라우터 세팅 / RESTful API

---

**😭TODO**

> 프로젝트 블링커 블로그 정리(여유있게 하기)<br>
> UI/UX Sketch + Zeplin 유튜브 강의 시청<br>

---

**🥰COMMENT**<br>
서버 구축

---

<center>

# 2019.12.15 일요일

</center>

**😇TIL**<br>

> 블로그 정리 중 안 사실.
> ![header](./h.png)

> 네트워크 연결이 없을때, 로컬로 접속하게 되면 헤더부분이 위 스크린샷 처럼 되는데, 블로그의 경우,<br>해당 헤더를
> `import NavDropdown from 'react-bootstrap/NavDropdown` 처럼 import 해와서 사용 합니다. 재밌는 점은 react-bootstrap/NavDropdown이 네트워크 연결 상태에서만 구동 된다는 점 입니다.
> 이 경우, 렌더링 속도에 영향을 줄 수 있는 부분인지 궁금합니다.

---

**😭TODO**

---

**🥰COMMENT**<br>

---

<center>

# 2019.12.16 월요일

</center>

**😇TIL**

---

**😭TODO**

> EXPO / RN 학습

---

**🥰COMMENT**<br>
프론트 작업 시작

---

<center>

# 2019.12.18 수요일

</center>

**😇TIL**

> 클릭 이벤트시 get요청 되도록 구성하기.
> 현재 크롤링 데이터가 db-tag 하나의 테이블에만 저장되는데, 이를 지역별 테이블을 생성해서 get 해오는 식으로 구성하기.

---

**😭TODO**

> Expo / Server 데이터 렌더링
> 현재 크롤링 데이터가 db-tag 하나의 테이블에만 저장되는데, 이를 지역별 테이블을 생성해서 get 해오는 식으로 구성하기.
> 클릭 이벤트시 get요청 되도록 구성하기.

---

**🥰COMMENT**<br>
엑스포 / 리액트 네이티브 어렵다.. 디비 구조를 좀더 고려해보자

---

<center>

# 2019.12.19 목요일

</center>

**😇TIL**

---

**😭TODO**

> Expo Router Setting

---

**🥰COMMENT**<br>

---

<center>

# 2019.12.24 화요일

</center>

**😇TIL**

> TypeScript 개념 학습

---

**😭TODO**

---

**🥰COMMENT**<br>

---

<center>

# 2020.01.16 목요일

</center>

**😇TIL**

> Typescript 정리 <br>
> 모델링 <br>
> 개인 프로젝트 서버 비동기 문제 처리

---

**😭TODO**

---

**🥰COMMENT**<br>
요즘 프로젝트한다 뭐한다 하느라 TIL을 소홀히 했다. 집중하자

---

<center>

# 2020.01.17 금요일

</center>

**😇TIL**

> JEST 테스트 블로깅
> React Hook basic

---

**😭TODO**

---

**🥰COMMENT**<br>
모델링하는게 스트레스 풀기에 좋다.. 코드는 ..코드는..

---

<center>

# 2020.01.19 일요일

</center>

**😇TIL**

> Passport 를 통한 Kakao 로그인 구현 이론 학습

---

**😭TODO**

---

**🥰COMMENT**<br>

---

<center>

# 2020.01.21 화요일

</center>

**😇TIL**

> REST API 재정리 <br>
> Redux 재정리 <br>
> TypeScript 내용 추가

---

**🥰COMMENT**<br>
감기 무섭다.. 온몸이 아프다 ㅠㅠ

---

<center>

# 2020.01.26 일요일

</center>

**😇TIL**

> MVC 패턴 복습

---

**🥰COMMENT**<br>
설날 마지막 ~

---

<center>

# 2020.01.28 화요일

</center>

**😇TIL**

> AWS Beanstalk

---

**🥰COMMENT**<br>
감기 조심

---

