---
published: false
---
## React 렌더링 이해 
React 컴포넌트가 렌더링을 수행하는 시점은 다음과 같습니다.

- Props가 변경되었을 때
- State가 변경되었을 때
- forceUpdate() 를 실행하였을 때
- 부모 컴포넌트가 렌더링되었을 때

네번째의 경우에 부모 컴포넌트가 렌더링 되었을 때 자식 컴포넌트 또한 렌더링 되므로,
하위 컴포넌트가 많은 경우 불필요한 렌더링이 발생할 가능성이 높아진다.

[참고](https://ko.reactjs.org/docs/conditional-rendering.html)