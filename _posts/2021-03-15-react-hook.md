---
published: true
---
## React Hook 
- Hook은 함수 컴포넌트에서 React state와 생명주기 기능을 연동할 수 있게 해주는 함수다.
- Hook은 class 안에서는 동작하지 않는다.

>주의)
React 16.8.0은 Hook을 지원하는 첫 번째 배포입니다. 
업그레이드할 때 React DOM을 포함한 모든 패키지를 업데이트하는 것을 잊지 마세요. React Native는 v0.59부터 Hook을 지원합니다.

# useState ( State Hook )
- 현재의 state 값과 이 값을 업데이트하는 함수를 쌍으로 제공( state, setState )
- 하나의 컴포넌트 내에서 State Hook을 여러 번 사용 가능 
---javascript
const [count, setCount] = useState(0);
---

# useEffect ( Effect Hook )
> React class의 `componentDidMount`, `componentDidUpdate`, `componentWillUnmount`를 하나의 API로 사용가능하게끔 한다.
- 여러 개의 사용 가능

# Custom Hook 
> 이름이 use로 시작하고, 안에서 다른 Hook을 호출하는 함수

- 각 컴포넌트의 state는 완전히 독립적이므로 상태 관련 로직을 재사용하는 방법
- 각각의 Hook 호출은 완전히 독립된 state를 가짐
- 한 컴포넌트 안에서 같은 custom Hook을 여러 번 사용 가능

# useReducer
---javascript
const [state, dispatch] = useReducer(reducer, initialArg, init);
// state 초기화
const [state, dispatch] = useReducer(
    reducer,
    {count: initialCount}
  );
---


[참고](https://ko.reactjs.org/docs/hooks-intro.html)
