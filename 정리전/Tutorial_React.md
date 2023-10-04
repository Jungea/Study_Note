# Tutorial React


## JSX
- _HTML과 같은_ 구문으로 UI를 설명할 수 있게 해주는 JavaScript용 구문 확장

## 컴포넌트 생성 및 사용
- 대문자 시작
- `expoert default` 파일의 주요 구성요소 지정
- 하나의 태그를 반환 (`<div> </div>` 나 `<> </>` 사용)
```jsx
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
```jsx
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
```jsx
let content;  
let isLoggedIn = false;  
if (isLoggedIn) {  
    content = <MyButton1/>;  
} else {  
    content = <MyButton2/>;  
}

export default function condition() {
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
```jsx
const products = [  
    {title: 'Cabbage', isFruit: false, id: 1},  
    {title: 'Garlic', isFruit: false, id: 2},  
    {title: 'Apple', isFruit: true, id: 3},  
];  
  
const listItems = products.map(product =>  
    <li key={product.id}>  
        {product.title}  
    </li>  
);

export default function foreach() {
	return (
		<ul>{listItems}</ul>
	);
}
```

## 이벤트 핸들러



---

https://nextjs.org/learn/foundations/how-nextjs-works/

## useState
- `const [likes, setLikes] = React.useState()`
- 첫 번째 항목은 value
- 두 번째 항목은 update 함수
- 