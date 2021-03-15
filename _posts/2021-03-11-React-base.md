---
published: true
---
## props / state

>props 는 부모 컴포넌트가 자식 컴포넌트에게 주는 값입니다. 
자식 컴포넌트에서는 props 를 받아오기만하고, 받아온 props 를 직접 수정 할 수 는 없습니다.
반면에 state 는 컴포넌트 내부에서 선언하며 내부에서 값을 변경 할 수 있습니다.


## 마운트

아래 메서드들은 컴포넌트의 인스턴스가 생성되어 DOM 상에 삽입될 때에 순서대로 호출됩니다.

- `constructor()`
- `static getDerivedStateFromProps()`
- `getderivedstatefromprops)`
- `render()`
- `componentDidMount()`


## 업데이트
> props 또는 state가 변경되면 갱신이 발생합니다. 

아래 메서드들은 컴포넌트가 다시 렌더링될 때 순서대로 호출됩니다.

- `static getDerivedStateFromProps()`
- `shouldComponentUpdate()`
- `render()`
- `getSnapshotBeforeUpdate()`
- `componentDidUpdate()`

## React 렌더링 이해 
React 컴포넌트가 렌더링을 수행하는 시점은 다음과 같습니다.

- Props가 변경되었을 때
- State가 변경되었을 때
- forceUpdate() 를 실행하였을 때
- 부모 컴포넌트가 렌더링되었을 때

네번째의 경우에 부모 컴포넌트가 렌더링 되었을 때 자식 컴포넌트 또한 렌더링 되므로,
하위 컴포넌트가 많은 경우 불필요한 렌더링이 발생할 가능성이 높아진다.


참고1 [리액트 공식문서](https://ko.reactjs.org/tutorial/tutorial.html)

참고2 [벨로퍼트](https://react.vlpt.us/basic/)
