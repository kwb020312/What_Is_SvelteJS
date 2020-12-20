# SveltJS

## 구동방법

```javascript
npx degit sveltejs/template (폴더명)
cd (폴더명)
npm i
npm run dev
```

해당 커맨드를 입력시

<img src="./gitImages/Install.png"/>

localhost:5000 으로 연결되었다는 메시지가 출력된다.

## 변수사용

SvelteJS 는 크게 <main> , <script> , <style> 로 나뉘는데

<img src="./gitImages/Variable.png">

변수를 해당 부분처럼 사용할 수 있다.

태그의 속상 값 으로도 변수를 사용할 수 있는데

<img src="./gitImages/AttrVariable.png">

src 에 들어갈 값은 public 폴더를 기준으로 상대경로를 적어주어야 한다.

## 스타일링

<img src="./gitImages/Style.png">

스타일은 매우 간단하게 기존에 CSS 작업을 <style> 태그 안에서 해주면 정상 적용된다.

## 컴포넌트 분리

<img src="./gitImages/Other_Component.png">

이렇게 다른 컴포넌트를 src 에 위치시켜주고

<img src="./gitImages/Import.png"/>

이렇게 Import 해와서 재사용이 가능하다.

별도의 export 작업은 해주지않아도 된다.

## HTML 변수

<img src="./gitImages/JustStr.png">

만약 HTML 태그를 변수에 넣고 삽입하고싶다면 어떻게 해야할까?

위와같은 방법으로 하면 결과는

<img src="./gitImages/JustStr_result.png">

위와같이 된다 .그저 문자열로 인식하는 것 이다.

하지만

<img src="./gitImages/UsingHTML.png">

위와 같이

{@html (변수명)}

으로 삽입한다면

<img src="./gitImages/UsingHTML_result.png">

위와 같은 결과가 출력되는 것을 알 수 있다.

## 작동원리

<img src="./gitImages/WhiteBox.png">

해당 사진처럼 main.js 안에 있는 내용이 Build 과정을 거치며
우리가 사용할 수 있도록 컴파일 되는 것이다.

## 함수관리

<img src="./gitImages/onClick.png">

함수를 호출할 때 에는 on:click={함수명} 을 주어야 한다.

함수선언은 <script> 태그 안에서 자유롭게 하면 된다.

위와 같은 코드를 준다면 아래와 같이 출련된다.

<img src="./gitImages/onClick_result.png">

## 반응성 선언

만약 FirstName 이라는 변수와 SecondName 이라는 변수를 조합하여
FullName 을 갖는 변수는 어떻게 사용해야할까??

```javascript
const FirstName = 'Chobby';
const SecondName = 'Kim';
const FullName = FirstName + SecondName;
```

위와같이 입력될 것이지만 만약 이벤트로 FirstName 의 값이 변경된다면 FullName 의 값이 변경될까??

변경되지 않는다. 변경되게 하기 위해서는 변수를 참조하는 변수의 앞에 $: 를 넣어

```javascript
const FirstName = 'Chobby';
const SecondName = 'Kim';
$: FullName = FirstName + SecondName;
```

위와같이 입력해주어야 한다.

## $:

과연 $: 는 어떨때 사용해야할까??

```javascript
<script>$: {alert('hello')}</script>
```

위와 같은경우 컴포넌트가 마운트 될 때 , 스테이트의 값이 어떠한 값이든 변경되는 경우 모두 alert('hello') 가 실행된다.

만약 특정 상태가 변경되는 경우에만 실행하고 싶다면 조건식을 붙일 수 도있다.

```javascript
<script>$: if(value >= 10) {alert('Over 10')}</script>
```
