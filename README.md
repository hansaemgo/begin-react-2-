## React 입문
### 01. 리액트 배경 

  - 기존 DOM변경을 위해 브라우저의 DOM Selector API를 사용, 특정 DOM선택 후 설정(복잡한 구조)
  - React : 가상의 DOM을 이용하여 실제 브라우저에 보여지는 DOM과 비교후 차이가 있는 곳을 감지하여 실제 DOM에 패치 시켜준다.
  
    ![Virtual DOM을 사용한 구현](../begin-react/src/image/virrualDom.png)

### 02. 작업환경 준비

  - 설치프로그램 : Node.js / yarn / 코드에디터(VSCode) 
  - 새 프로젝트 만들기 : `$ npx create-react-app begin-react`
  - 실행 : `$ yarn start`

### 03. 리액트 컴포넌트 만들기

  \*\* Hello.js \*\* 

  ```javascript
    import React from 'react'; // 리액트 불러오기
    function Hello() { // 함수형 컴포넌트 만들기
      return <div>안녕하세요</div>; // XML형식의 값 반환해주기 = JSX
    }
    export default Hello; // 컴포넌트 내보내기
  ```

  - 컴포넌트는 일종의 UI 조각이며 쉽게 재사용이 가능하다.
  ```javascript
   <Hello/>  // 재사용시 안녕하세요가 두번 화면에 출력된다.
   <hello/>
  ```
  
  ### ReactDOM.render(<App />, document.getElementById('root'));
  - ReactDOM.render의 역할은 실제 DOM내부에 리액트 컴포넌트를 `id`가 `root`인 DOM을 선택하여 렌더링 하겠다는 의미(index.html) 
  - `<div id="root"><div>` 
  
### 04. JSX의 기본규칙 알아보기

  1. 태그는 꼭 닫혀있어야 하며, 태그와 태그사이에 내용이 들어가지 않을때에는 Self Closing 사용. 
  2. Fragment(<></>) : 두개의 태그는 하나의 태그로 감싸져 있어야 한다. 
  ```javascript React
    <>  // <div>로감 싸는 것보다 Fragment 사용 권장 <></>
      <Hello />
      <Hello />
      <div>안녕히계세요</div>
    </>
  ```

  3. 괄호는 가독성을 위한것 이므로 필수적인 것은 아니다.
  4. Javascript 값을 보여줄때는 {name}중괄호 사용 
  ```javascript React
      const name = '고한샘';
      <div>{name}</div> // 고한샘
  ```

  5. {/* 주석은 이렇게 사용 한다 */}
  6. Style : 객체 형태로 작성을 해야 하며, `backgroundColor`처럼 camelCase로 네이밍 해야한다.
  ```javascript React
      const style = {
        backgroundColor: 'black',
        color: 'aqua',
        fontSize: 24, //기본단위 24px
        padding: '1rem' 
      };
  ```
  7. class : `className = `으로 설정 해주어야 한다.