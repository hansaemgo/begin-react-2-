## React 입문
### 01. 리액트 배경 

  - 기존 DOM변경을 위해 브라우저의 DOM Selector API를 사용, 특정 DOM선택 후 설정(복잡한 구조)
  - React : 가상의 DOM을 이용하여 실제 브라우저에 보여지는 DOM과 비교후 차이가 있는 곳을 감지하여 실제 DOM에 패치 시켜준다.
  
    ![Virtual DOM을 사용한 구현](../begin-react/src/image/virrualDom.png)

### 02. 작업환경 준비

  - 설치프로그램 : Node.js / yarn / 코드에디터(VSCode) 
  - 새 프로젝트 만들기 : `$ npx create-react-app begin-react`
  - 실행 : `$ yarn start`
  