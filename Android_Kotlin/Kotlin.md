
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

### 클래스
1. 기본 getter/setter 자동 생성
	- val : getter
	- var : getter/setter
```kotlin
class Person(val name: String) {  
    var age: Int = 0  
    val nickname: String = ""  
}
```
2. 직접 구현한 getter/setter 사용
	- ※ field : this.nickname을 사용 할 경우 setter/getter가 자동 호출됨 (stackoverflow 발생)
```kotlin
var nickname: String = ""  
    set(value) {  
        field = value.lowercase()  
    }
```
3. 프로퍼티와 필드
	- 필드
		- 클래스에 선언되어 있는 인스턴스 변수 
		- 클래스 변수 / static 아님
	- 프로퍼티
		- 필드 + publid Getter 또는 Setter
		- val, var
	- 코틀린에서는 Field를 사용하지 않음
	- Backing Field : 클래스 내부의 접근자에서 field 키워드로 프로퍼티의 값에 접근
4. 상속
	- 기본적으로 상속이 불가
	- 
