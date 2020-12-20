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
