# Redux
> 진실은 하나의 소스로부터 : 모든 상태는 하나의 스토어안에 하나의 캑체트리 구조

## React와 연결
- [참고문서](https://lunit.gitbook.io/redux-in-korean/basics/usagewithreact)
- mapDispatchToProps()
  * Redux 상태를 (store)받아서 component에게 넘길 props를 만들어서 넘겨준다.
- 그 후, connect()를 통해 호출
---
- Redux 개발도구로 상태변화를 다 기록해두고 시간여행이 가능하다.
---
- 단점 : Redux 상태변화를 값으로 나타내기 때문에 관례로 해결하는 부분이 많다. 상태관리 라이브러리
- `MobX`(Redux의 자동화) : 사람이 관례적으로 했던 부분을 자동으로 해줌
  * 상태의 전역변수 : 모든 상태가 하나의 통에 심지어 외부의 통에 => 장점일 수도 있지만 단점이 될 수 있다,
    + 1. 관리하기가 어렵다.
    + 2. 큰 상태트리 : 리액트는 상태가 바뀔때마다 화면을 다시 그리는데, 한 곳에 큰 상태트리를 가지고 있으므로 `모든 상태트리를 다시 그리게 된다.` => default가 전부 다시그림
      - 그래서 `connect`를 통해 받는 props만 변경되었을 때 다시 그리는 `최적화`가 미리 적용이 되어 있다. => 받는 props이 변경 되었을 때만! => 그래서 크게 신경쓰지 않아도됨!
      - action 이 dispatch() 됐을때는, 다 다시 실행됨 => action이 자주 dispatch되지 않게 코딩해야함, 자주 변경될 상태라면 그냥 React 상태에 저장! 예를들어 마우스의 좌표
      - pure component 와 `불변성`은 항상 엮어서 써야함 => dedux는 최적화가 미리 적용되어있기때문에 `반드시 불변성`을 지켜서 코딩해야함 그렇지 않으면 인식하지 못함

# ! 
> action 자주 dispatch하면 안된다.
> 불변성을 지키자.

