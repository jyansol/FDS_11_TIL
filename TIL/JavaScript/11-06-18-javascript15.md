# JavaScript

## e.preventDefault();
01. 비관적 업데이트 : 사용자 입력이 일어난뒤에 수정요청을 보내고 성공 시 화면을 갱신
    - 프로그래머 입장에선 편하지만, 사용자입장에선 불-편
    - `loading indicator` 사용!
02. 낙관적 업데이트 : 사용자 입력이 일어난뒤에 바로 화면 갱신하고 수정요청을 보냄
    - 프로그래머 입장에선 불편하지만, 사용자입장에선 편함
    - 성공과 실패의 화면이 달라야함, 실패의 경우 갱신 취소가 필요함(원상복구)
    - 고난이도 작업 ...
> 기준은 사용자가 무엇을 원하는지에 따라   

## 비동기함수
- drawTodoList()는 비동기함수기 때문에 아래의 코드가 실행된 다음 실행됨
> `await` drawTodoList();
- 비동기함수를 호출했을때 반환되는 promise는 비동기함수 `내부에서 반환한 값`이 채워진다.
- return undifined
---


## 웹어플리케이션!
  * 데이터를 불러와서 html를 만듬
  * 변경사항을 데이터에 보내고 다시 그림
  * But 화면을 통째로 다시 그리고 있음 => 비효율적이지만, 코드가 간단해짐
  * 필요한 부분만 갱신 => 효율적이지만, 코드는 복잡해짐
  > `React` : 효율적이면서(라이브러리가 처리해줌) 코드는 간단하게! 
    >>화면을 통째로 그리는 것처럼 만듬! 
    >>리액트가 알아서 컴퓨터에게 효율적이게 바꿔쥼



# baseURL
- 개발용과 운영용이 달라야함.
- parcel에는 환경변수를 사용해서 설정(언어마다 방법이 다 다름)


# axios
- 순수객체를 이용하면 속성이 겹치기 때문에 다른 방법을 사용하는게 좋다
  * URLSearchParams : 같은 이름의 속성을 사용해야 하는 경우
    -  URLSearchParams.append() 


# parcel    
- rm -rf .cache
- rm -rf dist