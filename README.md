
## - 20190803

##### 1.Eslint 
##### 2.Jest
##### 3.github pair programming
##### 4.underbar / recursion review
##### 5.check point 1 scope 문제


> 린트 : 유닉스 운영 체제에서 사용되는 프로그램으로 C 언어의 원시 프로그램을 읽어들여 오류가 있는 검사하는 프로그램. 린트(lint) 또는 린터(linter)는 소스 코드를 분석하여 프로그램 오류, 버그, 스타일 오류, 의심스러운 구조체에 표시(flag)를 달아놓기 위한 도구들을 가리킨다.[1] 이 용어는 C 언어 소스 코드를 검사하는 유닉스 유틸리티에서 기원한다.[2]

<hr/>


#### 1.Data Structure & OOP
일정: 2019. 7. 24.부터 2019. 7. 27.까지
Graph, Tree, Hash Table, B-Tree Discussion
일정: 2019. 7. 25. 오전 10:00부터 오전 11:30까지

#### 2.Inheritance pattern - Dance Party
일정: 2019. 7. 29.부터 2019. 7. 30.까지

#### 3.Algorithms (N-Queens)
일정: 2019. 7. 31.부터 2019. 8. 1.까지

#### 4.Interact with Server (Chatterbox Client)
일정: 2019. 8. 2.부터 2019. 8. 3.까지

#### 5.ES6 APIs & React (Recast.ly)
일정: 2019. 8. 5.부터 2019. 8. 8.까지

#### 6.self Assesments1

<hr/>

### 6. self Assessments - new 연산자를 통해서 생성된 인스턴스는 object 이다.
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

*GET

```js
fetch("/test.json") // (/test.json) 호출 (GET)
    .then(e => e.json()) // 비동기
     .then(e => console.log(e)); // 비동기
```

*옵션으로 POST

```js
fetch("/test.json", {
        method: "POST" // (/test.json) 호출 (POST)
    }).then(e => e.json()) // 비동기
   .then(e => console.log(e)); // 비동기
**forEach(callback) // reference code
function logArrayElements(element, index, array) {
  console.log('a[' + index + '] = ' + element);
}


인덱스 2는 배열의 그 위치에 항목이 없기에
건너뜀을 주의하세요.
[2, 5, , 9].forEach(logArrayElements);
기록:
a[0] = 2
a[1] = 5
a[3] = 9

```


https://www.zerocho.com/category/HTML&DOM/post/595b4bc97cafe885540c0c1c

<hr/>


### *서버
Web Architecture 란?

이제는 삶에서 없으면 안될만큼 아주 중요한 부분을 차지하고 있는 것이 바로 인터넷이다. 처음에는 인터넷에 연결이 되기만 하면 둥둥 떠있는 것처럼 원하는 곳으로 헤엄치며 다니면서 원하는 정보를 보고 듣고 가져올 수 있을 거라고 생각했다. 아주 추상적인 생각이다. 이번 블로그에서는 이러한 일을 가능하게 만들어 주는 구성요소에 대해 간략히 알아보자.
Application Programming Interface(API)
어떤 프로그램에서 사용할 수 있도록 운영체제나 프로그래밍 언어가 제공하는 기능을 제어할 수 있게 만든 인터페이스
*인터페이스: 서로 다른 두개의 시스템, 장치 사이에서 정보나 신호를 주고받는 경우의 접점이나 경계면
Client (=== Browser)
사용자가 보기 좋게, 편하게 만들어 주는 어플리케이션
Server
클라이언트의 요청을 받아서 요청을 적합하게 처리하는 어플리케이션
HTTP
클라이언트와 서버가 소통하기 위한 규칙을 정해 놓은 것
 
HTTP 장점
클라이언트와 서버 간에 요청의 제한 없이 정보를 저장하거나 하지 않기 때문에 무한히 요청하고 응답할 수 있다.
eg) Siri
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

<hr />

## 20190805 MON
React 

<hr />

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
>props: 부모(상위) Component 에서 자식(하위) Component로 내려주는 데이터, 리액트 에서는 단방향 데이터이기 때문에 내려갈 수 만 있다. 즉 다시 상위로 올라갈 수 없다. ( 간접적으로 올릴 수 있다. = state )


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










