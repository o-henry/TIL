### React Component

<hr/>

“컴포넌트” 라는 개념에 집중이 되어있는 라이브러리입니다. 컴포넌트는 우리가 추후 더 자세히 배워보겠지만, 미리 간단히 설명하자면, 데이터를 넣으면 우리가 지정한 유저 인터페이스를 조립해서 보여줍니다. 페이스북 개발자들이 라이브러리의 성능과 개발자 경험을 개선하기 위해 많은 연구를 합니다. 리액트를 한번 해본 개발자들은 대부분 맘에 들어합니다. 생태계가 엄청 넓고, 사용하는 곳도 많습니다. HTTP 클라이언트, 라우터, 심화적 상태 관리 등의 기능들은 내장되어있지 않습니다. 따로 공식 라이브러리가 있는 것도 아니여서, 개발자가 원하는 스택을 맘대로 골라서 사용 할 수 있습니다 (혹은 직접 라이브러리를 만들어서 쓸 수도 있겠죠.)

We built React to solve one problem: building large applications with data that changes over time.
번역: 우리는 지속해서 데이터가 변화하는 대규모 애플리케이션을 구축하기 위해 React를 만들었습니다

기존의 프레임워크 = 여기서 공통점은 바로 모델입니다. 방금 언급했던 프레임워크들의 모델은, 대부분 어떻게 작동하냐면, 양방향 바인딩을 통하여 모델에 있는 값이 변하면, 뷰에서도 이를 변화시켜줍니다. 여기서 핵심적인 부분은 변화시켜준다는 부분입니다. 일단 첫 화면을 보여주고, 변화에 따라 필요한곳을 바꿔주는거죠. 

그냥 Mutation 을 하지 말자. 그 대신에, 데이터가 바뀌면 그냥 뷰를 날려버리고 새로 만들어버리면 어떨까?

그렇게 하면 진짜 간단하겠죠? 그런데 브라우저가 무슨 게임 엔진도 아니고, DOM 기반으로 작동하는 이 페이지는 그때 그때 새로 뷰를 만들어버리라고 하면 성능적으로 엄청난 문제가 있을 것입니다.

그래서 사용하는게 바로, Virtual DOM 입니다.

Virtual DOM 은 가상의 DOM 입니다. 변화가 일어나면, 실제로 브라우저의 DOM 에 새로운걸 넣는것이 아니라, 자바스크립트로 이뤄진 가상 DOM 에 한번 렌더링을 하고, 기존의 DOM 과 비교를 한 다음에 정말 변화가 필요한 곳에만 업데이트를 해주는 것이죠.

이 Virtual DOM 을 사용함으로서, 데이터가 바뀌었을 때 더 이상 어떻게 업데이트 할 지를 고려하는게 아니라, 그냥 일단 바뀐 데이터로 일단 그려놓고 비교를 한다음에, 바뀐 부분만 찾아서 바꿔주는거죠.

React로 구현된 애플리케이션은 일반적으로 하나의 루트 DOM 노드가 있습니다. React를 기존 앱에 통합하려는 경우 원하는 만큼 많은 수의 독립된 루트 DOM 노드가 있을 수 있습니다.

React 엘리먼트를 루트 DOM 노드에 렌더링하려면 둘 다 ReactDOM.render()로 전달하면 됩니다.
<hr/>

### 함수 컴포넌트와 클래스 컴포넌트( Components and Props )
컴포넌트를 통해 UI를 재사용 가능한 개별적인 여러 조각으로 나누고, 각 조각을 개별적으로 살펴볼 수 있습니다.

**개념적으로 컴포넌트는 JavScript 함수와 유사합니다. "props" 라고 하는 임의의 입력을 받은 후, 화면에 어떻게 표시되는지를 기술하는 React 엘리먼트를 반환합니다.**

함수 컴포넌트
```
function Welcome(props){
  return <h1>Hello, {props.name}</h1>
}
```

**이 함수는 데이터를 가진 하나의 'props'(props는 속성을 나타내는 데이터) 객체 인자를 받은 후 React 엘리멘트를 반환하므로 유효한 React 컴포넌트 입니다.

ES6 class 컴포넌트

```
class Welcome extends React.Component {
  render(){
    return <h1>Hello, {this.props.name}</h1>
    }
}
```

### 컴포넌트 렌더링
<hr/>

### State and Lifecycle

```
function tick() {
  const element = (
    <div>
      <h1>Hello, world!</h1>
      <h2>It is {new Date().toLocaleTimeString()}.</h2>
    </div>
  );
  ReactDOM.render(
    element,
    document.getElementById('root')
  );
}

setInterval(tick, 1000);
```
