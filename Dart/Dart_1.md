
https://dartpad.dev/


- var vs dynamic
	- 변수의 값을 사용해서 변수의 타입을 유추
	- var : 한번 선언하면 타입이 고정 (변경 시 에러)
	- dynamic : 계속 다른 타입의 값을 저장 가능


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