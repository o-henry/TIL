### Stack / Queue / Linked List

<hr />

목표:

각 자료구조가 무엇인지, 각 자료구조가 가지고 있어야 할 methods들은 무엇이 있을지 검색하여 파악
각 자료구조와 그 자료구조의 method 들을 pseudo code 로 작성하기

<hr />

*모든 자료구조는 [삽입] , [삭제] , [읽기] 를 기본으로 갖습니다.*

### Queue

Queue(큐) 는 먼저 들어온 것이 먼저 나가는 구조로써, 선입섭출(FIFO, First In First Out) 의 구조를 갖는다.

그림으로 설명하면, 파이프에 한쪽으로는 넣기만 하고, 다른 한쪽으로는 빠지기만 하는 구조다.

예를 들자면, SNS에서 핫한 카페나 음식점을 가면 줄을 길게 섭니다. 오픈 시간 되기도 전에 일찍 와서 줄을 섰는데, 중간에 누가 새치기를 하면 화가 나겠죠? Queue도 동일합니다. 이처럼 원소를 도착한 시간의 순서에 따라 순차적으로 저장한 리스트를 Queue라고 합니다. 원소의 삭제를 앞쪽에서, 새로운 원소 삽입을 뒤쪽에서 합니다.(First In First Out)

<hr />

#### 배열로 큐 구현하기.

```js
names = [];
names.push('Chan');
names.push('Lee');
console.log(names);
 
names.shift();
console.log(names);
 
let data = []; || class Queue(){}
 
function enqueue(){ 
    data.shift() 
}
 
function dequeue(){
    data.push() 
} 
```

처음 데이터를 담을 배열(또는 클래스) 을 생성한다.

앞에서 빼내는 함수(메서드)를 생성한다.

뒤에서 집어넣는 함수(메서드)를 생성한다

#### * 다른 구현

Enqueue() : 큐 맨 뒤에 새로운 원소 삽입 (마지막으로 온 손님에게 번호표 발부) => push()

Dequeue() : 큐 맨 앞쪽에서 원소를 삭제 (처음으로 온 손님의 번호표를 삭제) => shift()

createQueue() : 지정된 크기의 원소를 저장하는 큐를 할당 (데이터 사이즈)

isEmpty() : 큐가 비어있는지 체크한다. (큐에 원소가 없으면 true 리턴)

isFull() : 큐에 원소를 더 넣을수 없으면 true 리턴

```js
function enqueue(element){
	this.dataStore.push(elemejnt);
}

function dequeue(){
	this.dataStore.shift();
}
```


