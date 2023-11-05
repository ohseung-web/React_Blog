# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)

/////////////////////////////////////////
2023년 10월 31일 blog 설명
// document.querySelector('.post').innerHTML = post; 일반적 자바코드를 리액트 에서는 {post} 이런 형식으로 작성함을 주의하자.
// id={post} 모든곳에 { }중괄호를 이용하여 사용한다.
// 이를 데이터 바인딩이라 한다. => 데이터를 꽃아 넣는다는 의미이다.

/_eslint-disable_/ => warring 메시지 안나옴
//////////////////////////////////////////

// let [logo, setLogo]=useState('ReactBlog');
// state란 : 자료를 잠깐 보관하고 싶을때 사용
// state 문법
// 1. 반드시 import {useState} from 'react'한다.
// 2. let [a,b] = useState('남자 코드 추천');
// 3. a = '남자 코드 추천'이라는 의미의 변수
// 4. b 는 state 변경할 때 사용하는 변수
// useState[] => ['남자 코트 추천',함수] 남음
// 변수 대신 useState 사용하는 이유 -----
// 변수를 이용하면 데이터가 변경 되었을 경우 html을 다시 작성하여야 한다.
// useState 경우는 데이터가 변경되면 html전체가 재 랜더링이 되기때문에 훨씬 편리하다.
// 자주 변경될 것 같은 부분을 useState로 작성한다.

// state 변경은 따봉 =따봉+1로 할 수 없다
// 반드시 따봉변경() 함수를 이용하여야 한다. : 따봉변경(따봉+1)
// function 함수(){

// }

<button type='button' onClick={()=>{

        // 기존 state가 array나 object 이면 원본유지하며 copy본을 만들자
        // 이런 copy를 deepcopy 또는 깊은복사라 한다.
        // [...글제목] => 괄호를 벗겨주고 다시 씌어주세요
        // [state변경함수 특징] : 기존state == 신규state의 경우 변경안됨
        // console.log(copy == 글제목)은  무조건  true임 고로 변경되지 않음
        // [array/object 특징]

        let copy = [...글제목];
        copy[0] ='여자코트 추천'
        글제목변경(copy);


        }}>수정</button>
        <button type='button'  onClick={()=>{
            let copy = [...글제목];
            글제목변경(copy.sort());
        }}>가나순정렬</button>

/////////////////////////////////////
component(컴포넌트) 만드는 법

1. function 만들고
2. return()안에 html 담기
3. <함수명></함수명>쓰기

의미없는 <div> 대신 <></>빈 태그 사용가능
// 어떤걸 컴포넌트로 만들면 좋은가
// 1. 반복적인 html 축약할 때
// 2. 큰페이지들
// 3. 자주변경되는 것들

[동적인 UI만드는 step]
1.html.css로 미리 디자인 완성
2.UI의 현재 상태를 state로 저장
3.state에 따라 UI가 어떻게 보일지 작성

// html 작성 공간으로 if문사용 못함
// 삼항연산자 이용하여 사요한다.
modal === true ? <Modal /> : null

////////////////////////////////////////////
2023년 11월 1일
map()함수

1. 왼쪽 array 자료만큼 내부코드 실행해줌
2. return 오른쪽에 있는걸 array로 담아줌
3. 유요한 파라미터 2개 사용 가능
4. [1,2,3].map(function(a, i){})
5. 위에서 a는 array의 자료 대신 출력
6. i는 array의 index 번호 출력

props 사용방법
// 함수안의 state를 다른 함수안으로 가져다 사용할 수 없다.
// 부모 컴포넌트에서 자식 컴포넌트로 state를 전달 할 수 있다.
// 전달하는 명령어가 props이다.
// 1. <자식 컴포넌트 작명={state이름}>
// 2. 자식 컴포넌트에서 props파라미터 등록후 props.작명 사용한다.

//////////////////////////////////
[input]

1. input에 데이터 입력시 코드실행하고 싶으면 onChange/onInput 이벤트 핸들러 사용한다.
2. input에 입력한 값 가져오는 방법
   onChange={(e)=>{console.log(e)}}
3. e 파라미터 : 이벤트 객체라 부르면 지금 발생하는 이벤트에 관련한 여러 기능이 담겨 있다.

4. 이벤트 버블링 : 자식을 클릭하면 부모도 같이 클릭되어지는 현상을 말한다.
5. e.stopPropagation(); 함수를 사용하면 이벤트 버블링을 막을 수 있다.
