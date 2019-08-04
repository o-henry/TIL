TIL (2주차 까지)

##### 1.Eslint 
##### 2.Jest
##### 3.github pair programming
##### 4.underbar / recursion review
##### 5.check point 1 scope 문제


*린트 : 유닉스 운영 체제에서 사용되는 프로그램으로 C 언어의 원시 프로그램을 읽어들여 오류가 있는 검사하는 프로그램. 린트(lint) 또는 린터(linter)는 소스 코드를 분석하여 프로그램 오류, 버그, 스타일 오류, 의심스러운 구조체에 표시(flag)를 달아놓기 위한 도구들을 가리킨다.[1] 이 용어는 C 언어 소스 코드를 검사하는 유닉스 유틸리티에서 기원한다.[2]

<hr/>


1.Data Structure & OOP
일정: 2019. 7. 24.부터 2019. 7. 27.까지
Graph, Tree, Hash Table, B-Tree Discussion
일정: 2019. 7. 25. 오전 10:00부터 오전 11:30까지

2.Inheritance pattern - Dance Party
일정: 2019. 7. 29.부터 2019. 7. 30.까지

3.Algorithms (N-Queens)
일정: 2019. 7. 31.부터 2019. 8. 1.까지

4.Interact with Server (Chatterbox Client)
일정: 2019. 8. 2.부터 2019. 8. 3.까지

5.ES6 APIs & React (Recast.ly)
일정: 2019. 8. 5.부터 2019. 8. 8.까지

6.self Assesments1

블로깅
문제 정리
TIL 정리
리액트 정리

*6. self Assessments - new 연산자를 통해서 생성된 인스턴스는 object 이다.
    함수 안에서 메서드를 만드는 방법
1.  Use Closure
2. 객체를 생성한뒤 , 해당 객체에 함수를 추가.
3.  Object.assign(newTree, treeMethods); 의 사용이유 => Object.assign() 메소드는 열거할 수 있는 하나 이상의 출처 객체로부터 대상 객체로 속성을 복사할 때 사용합니다. 대상 객체를 반환합니다.

1. 먼저 데이터가 담길 구조를 잡는다.
2. 프로토타입을 어떻게 이용할지 고려한다. => Object.assign(obj, method가 될 객체)

```
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

*4.Interact with Server (Chatterbox Client)


*fetch

fetch (꺼냄)
미국·영국 [fetʃ] 발음듣기 영국식 발음듣기 중요도 별점 2개 다른 뜻(4건) 예문보기
1. (어디를 가서) 가지고 오다   2. (특정 가격에) 팔리다
https://terms.naver.com/entry.nhn?docId=823204&cid=42344&categoryId=42344

fetch()를 불러들이는 경우, 취득할 리소스를 반드시 인수로 지정하지 않으면 안됩니다. 읽어들인 뒤,  fetch()는 Promise객체를 반환합니다. 리퀘스트가 성공하든 실패하든 해당 리퀘스트 통신에 대한 Response객체가 취득됩니다. fetch()의 두번째 인수는 초기화에 사용되는 객체를 정의하고 있습니다. 이 인수는 기입하지 않아도 함수의 동작에 문제가 없습니다. 이 인수에 대한 상세한 정보는 Request)를 참고해주시기 바랍니다.

Response를 가져온 후에, 콜백함수의 매개변수로 담긴 response 객체에는 리스폰스에 포함되어있는 컨텐츠와 그에대한 처리방법이 담긴 메소드들이 담겨있습니다. 자세한 사항은 Body를 참고해주시기 바랍니다.

fetch('주소', 설정객체).then(콜백).catch(콜백);
.. fetch 만을 했을때는 서버에 저장된 정보를 그대로 가져온다.
then 을 통해 받아온 값을 처리 할 수 있다.

// GET
```
fetch("/test.json") // (/test.json) 호출 (GET)
    .then(e => e.json()) // 비동기
     .then(e => console.log(e)); // 비동기
```
// 옵션으로 POST
```
fetch("/test.json", {
        method: "POST" // (/test.json) 호출 (POST)
    }).then(e => e.json()) // 비동기
   .then(e => console.log(e)); // 비동기
**forEach(callback) // reference code
function logArrayElements(element, index, array) {
  console.log('a[' + index + '] = ' + element);
}
```

// 인덱스 2는 배열의 그 위치에 항목이 없기에
// 건너뜀을 주의하세요.
[2, 5, , 9].forEach(logArrayElements);
// 기록:
// a[0] = 2
// a[1] = 5
// a[3] = 9


https://www.zerocho.com/category/HTML&DOM/post/595b4bc97cafe885540c0c1c


*서버
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
```
fetch( url )
  .then(response => response.json())
  .then(result => console.log(result))
  .catch(error => console.log(error));
  
 // json 구조의 data
```

웹 서비스는 위의 구성요소를 활용하여 사용자들이 여러 정보를 주고 받는 일련의 방식/형태
 
*5.ES6 APIs & React (Recast.ly)

React

















