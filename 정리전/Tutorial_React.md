# Tutorial React

## 컴포넌트 생성 및 사용
- 대문자 시작
- `expoert default` 파일의 주요 구성요소 지정
- 여러 개의 태그를 반환할 수 없어 
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

