# Tutorial React

## 컴포넌트 생성 및 사용
- 대문자 시작
- `expoert default` 파일의 주요 구성요소 지정
- 하나의 태그를 반환 (`<div> </div>` 나 `<> </>` 사용)
```js
function MyButton() {
  return (
    <button>
      I'm a button
    </button>
  );
}

export default function MyApp() {
  return (
    <div>
      <h1>Welcome to my app</h1>
      <MyButton />
    </div>
  );
}
```

## 데이터 표시
- `{ data }`
```js
const user = {
  name: '홍길동',
  description: '안녕하세요. 반갑습니다.',
};

export default function Profile() {
  return (
    <>
      <h1>{user.name}</h1>
      <div>{user.description}</div>
    </>
  );
}
```

## 조건문
```js
let content;  
let isLoggedIn = false;  
if (isLoggedIn) {  
    content = <MyButton1/>;  
} else {  
    content = <MyButton2/>;  
}

export default function Profile() {
	return (
		{content}
		
		<div>  
		    {isLoggedIn ? (<MyButton1/>) : (<MyButton2/>)}  
		</div>  
		<div>  
		    {isLoggedIn && <MyButton1/>}  
		</div>
	);
}
```

## 반복문
