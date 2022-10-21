#웹게임을 만들며 배우는 리액트

<!-- 리액트를 사용하는 이유 -->
-복잡한 웹앱에서 데이터와 화면을 일치시켜줌.
-화면 깜빡임 없이 자연스럽게 넘어감.
-검색 엔진 노출이 중요하면 html,css,js로 만드는게 좋음.
-프론트엔드 개발자의 기본은 html,css,js임. 이것들의 기본기가 중요.
-자바스크립트 문법을 잘알고있어야 리액트도 잘할수 있음.

<!-- 첫 리액트 컴포넌트 -->
-class 컴포넌트는 지금은 거의 쓰이지않음.(1% 정도) 하지만 알고는 있어야함.
-컴포넌트 = 데이터(state) + 화면(return)
-리액트는 데이터 중심으로 움직임.
-데이터가 바뀌면 화면은 자동으로 바뀜. 화면이 바뀌는 부분은 state로 만듦.
-ReactDOM.render(<LikeButton />, document.querySelector("#root")); // React 17버전 코드
-ReactDOM.createRoot(document.querySelector("#root")).render(<LikeButton />); // React 18버전 코드
-return에는 태그가 하나만 있어야함. 태그가 두개 들어갈 시에는 <div>(부모요소)로 감싸줘야함.

<!-- 클래스 컴포넌트의 형태와 리액트 데브툴즈 -->
-객체를 함부로 바꾸지 말고, 복사할것 (불변성, 객체를 직접적으로 변경할 수 없음)
-pop, push, unshift, splice => 배열을 직접적으로 수정
-concat, slice => 새로운 배열을 만들어냄

<!-- 함수 컴포넌트 -->
-함수 컴포넌트를 쓰면 좋은점. this를 쓸일이 없음.
-뭔짓을 하든 결국 return한게 화면임.
-직접 만든 함수들은 화살표 함수를 써야함.

<!-- React Hooks 사용하기 -->
-어떤 작업에서 ref를 사용할까? => React에서 state로만 해결할 수 없고, DOM을 반드시 직접 건드려야 할 때 사용하게 됨.
예) 특정 input에 focus 주기, 스크롤 박스 조작, Canvas 요소에 그림 그리기 등…

<!-- Class와 Hooks 비교하기 -->
-React Hooks은 리액트의 새로운 기능으로 React 16.8버전에 새로 추가된 기능으로 state, component에 대한 것들을 바꿔놓았다. 만일 앱을 react hook을 사용하여 만든다면 class component, render 등을 안해도 된다는 뜻이다.
-class -> className
-for -> HTMLFor

<!-- 웹팩 설치하기 -->
-웹팩 : 여러개의 자바스크립트 파일을 하나의 자바스크립트 파일로 만들어줌.
-웹팩을 하려면 노드(Node.js)를 알아야함. 노드-> 자바스크립트 실행기
-리액트 할때 노드를 알아야 하는 이유: 웹팩을 돌리기 위한 자바스크립트를 실행해야한다.
-실제 서비스를 할때는 웹팩이 필요없음, 개발할때만 필요함.
-웹팩 설치하는 방법. 
1. node.js를 설치한다.
2. 터미널에 npm init이라고 입력한다.
3. package name을 마음대로 정해준다.
4. author는 본인 이름, license에는 ISC나 MIT를 입력해준다.
5. 마지막 yes 입력
6. 이렇게 하면 package.json이 생성됨. 여기에 리액트 개발에 필요한 모든것들을 넣어주면됌.
7. 제일 먼저 react & react-dom을 설치해준다. 터미널에 npm i react react-dom 입력.
8. 리액트 할때 필요한 웹팩을 설치해준다. 터미널에 npm i -D webpack webpack-cli 입력.
-실제 서비스에서 쓰이는 것들은 package.json의 dependencies에 기록되고, 개발에만 쓰이는 것들을 devDependencies에 기록된다.
-js 확장자를 쓰지 않고 jsx 확장자를 쓰는 이유: 파일 안에서 jsx 문법을 쓰면 확장자도 jsx를 쓰는것이 좋다. -> js"x" 한글자로 파일 안에 jsx 문법이 담겨있음(리액트 전용 파일)이겠구나를 알수있음.
-path.join (__dirname, "파일이름")-> "현재 폴더" 안의 파일을 의미한다.

<!-- 웹팩으로 빌드하기 -->
- 웹팩 
- babel/core -> 바벨의 기본적인것이 들어있음.
- babel/preset-env -> 이용자의 브라우저에 맞게 알아서 최신문법을 옛날 문법으로 바꿔줌.
- babel/preset-react -> jsx 바꿔줌.
- babel-loader -> 바벨과 웹팩을 연결해줌.
