
https://dartpad.dev/


- var vs dynamic
	- 변수의 값을 사용해서 변수의 타입을 유추
	- var : 한번 선언하면 타입이 고정 (변경 시 에러)
	- dynamic : 계속 다른 타입의 값을 저장 가능

- final vs const
	- 처음 선언 후 변경 불가
	- final : 런타임 (실행될 때 확정)
	- const : 빌드타임 (실행하지 않은 상태에서 값이 확정)
	- DateTime.now() : 런타임

## TYPE
```Dart
var variable1 = 'Dart';  // String variable1 = 'Dart'
print('[variable1 type]');
print(variable1.runtimeType);

var variable2 = 20;  // int variable2 = 20
print('[variable2 type]');
print(variable2.runtimeType);

=====================================
[variable1 type]
String

[variable2 type]
int
```

- var일 경우 오른쪽에 입력하는 값에 따라 해당 타입으로 선언 됨.
- 타입을 선언할 필요 없는 곳에서 var 사용
- 되도록 직접 타입을 선언해서 사용 권장!!

## Print
- print 매개변수는 문자열
```Dart
String s1 = 'Hello';
String s2 = 'Dart';
int i1 = 10;
print(s1 + s2);  // 문자열 + 문자열
print('${s1} ${s2}');  
print('$s1 $s2');
print('${s1.runtimeType} $s2');
print('s2 = ${s2.runtimeType}');
print('s2' + '${s2.runtimeType}');

====================================
HelloDart
Hello Dart
Hello Dart
String Dart
s2 = String
s2String
```


- List
	- 여러값을 순서대로 저장
```Dart
list[i]
list.length
list[i] = changeValue
list.add(addValue)
list.where((item) => bool)  : 필터 / Iterable
list.map((item) => newValue)  : 변경 / Iterable
list.reduce() : sum(첫번째값 + 두번쨰값) / 리스트와 같은 타입으로 반환
list.fold<int>(0, (value, element) => value + element.length)  : 리스트와 다른타입으로 반환 가능
```
	

- map
	- (key, value)
```Dart
Map<String, String> dictionary = {
	'Harry Potter': '해리 포터',
	'Ron Weasley': '론 위즐리',
	'Hermione Granger': '헤르미온느 그레인저',
};
print(dictionary['Harry Potter']);
print(dictionary['Hermione Granger']);
print(dictionary.keys);
print(dictionary.values);
```

- set
	- 중복제거


- var는 null 저장 가능
- 기본자료형은 ?를 붙여야 null 저장 가능
```Dart
  double? number3;  //기본 null
  print(number3);
  number3 ??= 3;  //null일 때만 값 저장
  print(number3);
  number3 ??= 4;
  print(number3);
```

- 타입비교연산자
```Dart
int number4 = 1;
print(number4 is int);
print(number4 is! int);
```


## 함수
- 포지셔널 파라미터 : 입력된 순서대로
- 네임드 파라미터 : 키
	- { required int a }
- 기본값
	- `[ int a= 2 ] `
- 포지셔널 파라미터 -> 네임드 파라미터

- 익명 함수
- 람다 함수
## typedef (시그니처 정의)
```Dart

typedef Operation = void Function(int x, int y);

void add(int x, int y) {
  print('결과값 : ${x + y}');
}

void sub(int x, int y) {
  print('결과값 : ${x - y}');
}

void calculate(int x, int y, Operation oper) {
  oper(x, y);
}

void main() {
  Operation oper = add;
  oper(1, 2);
  
  oper = sub;
  oper(1, 2);
  
  calculate(1, 2, add);
}
```

