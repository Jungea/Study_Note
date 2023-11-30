
https://dartpad.dev/


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

```Dart
void main() {
  
  print('===================================');
  
  String s1 = 'Hello';
  String s2 = 'Dart';
  print(s1 + s2);
  print('${s1} ${s2}');
  print('$s1 $s2');
  print('${s1.runtimeType} $s2');
  print('s2 = ${s2.runtimeType}');
  print('s2' + '${s2.runtimeType}');

  print('===================================');

  int age = 20;
  double score = 9.5;
  bool isValid = true;
  String name = 'Dart';

  var variable1 = 'Dart';
  print('[variable1 type] = ${variable1.runtimeType}');

  var variable2 = 20;
  print('[variable2 type] = ${variable2.runtimeType}');
}

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

