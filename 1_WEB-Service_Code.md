# Code  
  1) HTML
  2) JAVASCRIPT
  3) CSS  
 
<br/></br> 

### 1. HTML  
- HTML연습
```html
<!DOCTYPE html>
<html lang="ko">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<link rel="stylesheet" href="./style.css">
	<title>사이트 제작 연습</title>
</head>
<body>
	<header>
		<h1>사이트</h1>
	</header>
	<main>
		<div class="container">
			<button id="generateBtn">랜덤 이미지 생성 버튼</button>
		</div>
		<div id="gridContainer"></div>
	</main>
	<script src="./script.js"></script>
</body>
</html>
```

<br/></br> 

### 2. JAVASCRIPT  
- JAVA연습
```JAVA
const generateBtn = document.querySelector('#generateBtn')

generateBtn.addEventListener('click',  () => {
    console.log('버튼을 누르면 함수 실행됨')
})
```  

- **이미지를 랜덤하게 출력하는 액션 코드**
```JAVA
const generateBtn = document.querySelector('#generateBtn'); // generateBtn이라는 이름의 아이디를 가진 변수는 generate변수에 넣고
const gridContainer = document.querySelector('#gridContainer');
              
generateBtn.addEventListener('click', ()=> {  // addEventListener : 'click'이라는 이벤트 발생시 어떤 행동을 하도록 정의
    const randomNumber = Math.floor(Math.random() * 1000)+1;  // 랜덤 정수 생성
    const imgUrl = `https://picsum.photos/500?random=${randomNumber}`;  // API요청시 사용하는 주소
                                                                        // ${} : 어떤 문자열 안에 동적인 값을 넣을 때 사용

    const img = document.createElement('img'); //이미지라는 태그를 생성
    img.src = imgUrl; //img 태그의 src 소스 속성 안에 외부 API요청의 이미지 결과를 넣어주고

    gridContainer.appendChild(img); // 해당 이미지 요소를 화면에 보여줄 대상을 선택해서 이 대상에 추가
});
```

<br/></br> 

### 3. CSS
