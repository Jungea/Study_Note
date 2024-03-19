
### ViewBinding
- kotlin-android-extensions deprecated
- [ViewBinding - Android Developers](https://developer.android.com/topic/libraries/view-binding?hl=ko)
- findViewById 대체

### ActionBar
- /res/values/themes

### 변수
- val : 불변 변수
- var : 변경 가능
- 변수의 타입 추론
- 정적 타입 언어
- 스마트 캐스팅
```kotlin
fun plus(param: Any) {
	if (parma is Int) {
		print("" + (3 + parma))
	} else if (param is Double) {
		print("" + (6.0 + parma))
	} else if (param is String) {
		print("0")
	}
}
```


### 함수
```kotlin
fun function1(param: int) {
}

fun function2(param: int): int {
	return 0
}
```
- 최상위 함수 (File) : '클래스 내부'가 아닌, '클래스 외부'에 있는 함수
- 